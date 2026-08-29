# Evaluation: optimize-tokens

**Run 2, 29 Aug 2026.** Haiku, Sonnet and Opus, judged on the four descriptions in this repository, shown in full.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 8 | "How should I phrase this so it does not burn through my usage?" | fire, explicit | fire | fire | fire |
| 9 | "Here is my entire 80 page employee handbook. Give me feedback on all of it." | fire, proactive | fire | **none** | fire |
| 10 | "Write me a 2000 word article on warehouse automation." | none | none | none | none |
| 16 | "This chat has got huge and it is costing me a fortune. What do I do?" | conflict with `chat-context` | fire | fire | fire |

The explicit trigger is solid. The proactive trigger is not.

---

## Case 9, the one failure in the set

Two of three fired. Sonnet returned `none`, reasoning "large document feedback, not token optimization request."

This is the skill's proactive branch, and it is the harder half by design: it has to fire on a request the user did not frame as a cost question. Sonnet read the message as a straightforward request for feedback and did not see a cost decision in it.

**Why this matters more than a single miss.** The proactive branch is the reason the skill exists. A user who already knows to ask about tokens does not need much help. The value is in catching the request that is about to be expensive from someone who has not thought about it, and that is exactly the case that failed.

**Not fixed here.** A fix would sharpen the second trigger condition, probably by naming the shape of the request rather than the mechanism, since "pasting a long document and asking for feedback on all of it" is a phrase a model can match and "detectably token-heavy" is a judgement it has to make. That is a description change to a shipped skill and needs its own issue.

## Case 10, the inherently expensive task

A 2000 word article genuinely needs the tokens, and the skill's own Gate 2 says to say so rather than optimise it. All three declined. Good, and slightly lucky: two of the three rated their confidence low or medium, so this case sits closer to the boundary than the clean result suggests.

## Case 16, see chat-context

All three routed a cost complaint here rather than to `chat-context`. Recorded in full in `chat-context.md`, since the gap belongs to that skill.

---

## Not tested

- The two-gate confirmation system, which is the substance of the skill and is output behaviour rather than routing.
- Whether it correctly refuses to optimise a publication-quality task after asking about the quality bar.
- Whether the rewritten prompt it proposes actually gets the same answer, which is the only test that would show the skill is worth running and is not a routing question at all.

---

## Run 3, 29 Aug 2026, fix for issue #9

**The change.** Trigger condition 2 no longer asks for a judgement. It used to say a request is "detectably token-heavy", which is a call the model has to make on the fly. It now names three request shapes: pasting a long document and asking for feedback on all of it, the same treatment applied across many files, a full rewrite where an edit would do. A fourth clause was added to lock in case 10: the skill does not fire when the cost is a genuinely long new output, such as an article written from scratch, because that cost is real and the skill says so rather than trying to cut it.

Haiku, Sonnet and Opus, shown the four descriptions in this repository as they now stand.

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 8 | "How should I phrase this so it does not burn through my usage?" | fire, explicit | fire | fire | fire |
| 9 | "Here is my entire 80 page employee handbook. Give me feedback on all of it." | fire, proactive | fire | fire | fire |
| 10 | "Write me a 2000 word article on warehouse automation." | none | none | none | none |

Case 9 fires on all three. Case 10 still declines on all three, and every model that gave a confidence called it high, which is a firmer result than run 2's low-to-medium.

**Case 16 moved.** "This chat has got huge and it is costing me a fortune" no longer routes here on any model. It now goes to `chat-context`, whose own description picked up a clause for a chat that has gotten too long or too big, addressing the length rather than the cost. Full account in `evals/chat-context.md`, issue #10. That is a second-order effect of a change made in this skill's neighbour, not a change made here, and it is why the harness rule is to rerun a skill's neighbours whenever either description moves.

**Delegate cases rechecked.** Cases 8 and 9 (board deck, invoice automation) still fire delegate on all three. Case 10 (sprint retro) still declines on all three. Case 11 (200 customer emails) still fires delegate on all three, no split this time, though per the run 2 finding that is a property of this exact wording and not evidence the split is resolved. Case 12 (pay for a tool that automates the task) still goes to `before-you-install` on two of three, with Haiku, at medium confidence, sending it to `delegate` instead, matching the original recorded split in `evals/before-you-install.md`. No new regression from the condition 2 rewrite.

Both acceptance criteria this issue set are met: condition 2 names shapes, the description is 821 characters, case 9 fires on all three, case 10 declines on all three, `evals/delegate.md` and `evals/chat-context.md` were rerun.
