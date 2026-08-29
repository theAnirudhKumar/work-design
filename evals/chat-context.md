# Evaluation: chat-context

**Run 2, 29 Aug 2026.** Haiku, Sonnet and Opus, judged on the four descriptions in this repository, shown in full.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 5 | "Wrap this chat, I am moving to a new one." | fire, handoff | fire | fire | fire |
| 6 | "Pick up where we left off on the pricing page work." | fire, resume | fire | fire | fire |
| 7 | "Can you summarise what we talked about today so I can read it back?" | none | none | none | none |
| 16 | "This chat has got huge and it is costing me a fortune. What do I do?" | conflict with `optimize-tokens` | optimize-tokens | optimize-tokens | optimize-tokens |

Both modes fire. The exclusion holds. One finding on case 16.

---

## Case 7, the exclusion that matters most

"Summarise what we talked about" is the single most likely false positive for this skill, because it is superficially the same request and the skill's own rules say it is a different ask. All three models declined it. The sentence "do not use it when the user wants a summary to read rather than a handoff to reuse" is what produced that, and it should survive any future trim.

## Case 16, the gap

"This chat has got huge and it is costing me a fortune" went to `optimize-tokens` on all three models, unanimously and with no hesitation.

That is defensible, and it is also arguably the wrong skill. The actual remedy for a chat that has grown expensive is to close it and open a fresh one carrying a handoff, which is exactly what this skill does. `optimize-tokens` will produce a leaner prompt inside a context that is already the problem.

**Recorded as a gap, not fixed here.** The fix would be a clause in this skill's description about a chat that has become long or expensive, and that is a description change to a shipped skill, which needs its own issue. Two reasons to think before making it:

1. It would put this skill into direct competition with `optimize-tokens` on every cost-shaped message, and `optimize-tokens` is right for most of them.
2. The two are complementary in this case rather than exclusive. The best session opens with a handoff and then prompts the new chat leanly.

The honest version of the finding: a user who describes their problem in terms of cost will not reach this skill, and the skill that they do reach cannot solve the cost problem at its root.

---

## Not tested

- Whether handoff correctly detects that no file access exists and prints the block in chat instead. That is an output check.
- Whether resume states what was loaded before doing any work, which is the rule most likely to be skipped under load.
- The two-Active-rows case, where the skill is supposed to ask rather than guess.

---

## Run 3, 29 Aug 2026, fix for issue #10

**The decision.** Add the length-and-cost case to the HANDOFF trigger list, phrased around the chat being too long or too big to keep working in rather than around cost, so it does not compete with `optimize-tokens` on the word "expensive". This was the narrower option named in the issue, tried before considering anything broader.

The first attempt paired that addition with the existing final sentence unchanged ("Use this instead of summarising a chat back to the user in conversation"). Opus misread that sentence on case 7 and fired chat-context on a plain summary request, at medium confidence, something none of the three models had done in run 2. Rather than accept a new false positive on the exclusion the issue named as the one protecting this skill, the sentence was rewritten as an explicit negative: "Never fires for a request to summarise the chat back to the user in conversation; that gets a summary, not a handoff." Reran with that wording. Clean on all three.

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 5 | "Wrap this chat, I am moving to a new one." | fire, handoff | fire | fire | fire |
| 6 | "Pick up where we left off on the pricing page work." | fire, resume | fire | fire | fire |
| 7 | "Can you summarise what we talked about today so I can read it back?" | none | none | none | none |
| 16 | "This chat has got huge and it is costing me a fortune. What do I do?" | fire, see below | fire | fire | fire |

**Case 16 now fires here, cleanly, on all three models.** Not a conflict anymore. Confidence was high on two of three and medium on Opus, whose reasoning named the mechanism directly: "the cost framing is a symptom, not a request to prompt more efficiently." `optimize-tokens` was shown the same message in the same call and no model chose it.

This resolves further than the issue's own framing expected. The issue treated the two skills as complementary and worried that a cost clause would put them in direct competition on every cost-shaped message. That did not happen, because the added clause is not a cost clause. It names chat length, which `optimize-tokens` has never claimed, so the two skills stayed out of each other's way rather than trading false positives. The complementary case the issue described, a handoff followed by a lean prompt in the new chat, is still true and still not something a router choosing one skill can express. It just was not the thing that needed fixing here.

**Case 7 holds.** The rewrite from a comparative sentence to an explicit negative is the fix. Read this as a small addition to the house style: a sentence saying what a skill is *for* instead of what it *is not* is a softer guardrail than an explicit "never fires when", and the softer form failed once here.

All acceptance criteria for this issue are met: the reasoning above is recorded, the description is 1,004 characters, case 16 fires cleanly rather than the prior unanimous miss, `evals/optimize-tokens.md` was rerun and shows the same result from its side, and case 7 still declines on all three.
