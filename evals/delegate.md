# Evaluation: delegate

Routing cases for `delegate`, run against the four descriptions in this repository as they stood on the day. The harness this belongs to is issue #5; this file is the first one and was written alongside the skill.

**Method.** Ten user messages put to three models, each shown only the four skill descriptions and asked which single skill should fire, or none. Judged on the description alone, which is how routing actually works, since the body of a skill is not loaded until after it is chosen.

**Run on:** 29 Aug 2026, against Haiku, Sonnet and Opus.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I've got to put together the quarterly board deck. How much of this should I just get you to do?" | delegate | delegate | delegate | delegate |
| 2 | "Should I automate my weekly invoice chasing or keep doing it myself?" | delegate | delegate | delegate | delegate |
| 3 | "What parts of writing this case study can I hand off?" | delegate | delegate | delegate | delegate |
| 4 | "I want to give this competitor research to an agent but I am nervous about it." | delegate | delegate | delegate | delegate |
| 5 | "Our sprint retro happens every two weeks and it is a mess. Can you help me redesign the ritual?" | none | none | none | none |
| 6 | "Should I pay for the Pro tier of that note-taking app?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 7 | "This chat is getting long. I am going to start a fresh one." | chat-context | chat-context | chat-context | chat-context |
| 8 | "Can you read these 40 PDFs and give me a full report on each?" | optimize-tokens | optimize-tokens | optimize-tokens | optimize-tokens |
| 9 | "Write me a prompt that gets Claude to draft LinkedIn posts in my voice." | none | none | none | none |
| 10 | "I am about to have Claude process 200 customer emails and pull out the themes. Is that a good idea?" | split, see below | optimize-tokens | delegate | delegate |

Nine of ten agree across all three models. Cases 1 to 4 fire, cases 5 to 9 route correctly to a neighbour or to none, and no case produced a false positive for `delegate` against another skill in this repository.

---

## Case 5, the exclusion clause works

The recurring team ritual is the nearest thing to a false positive available, since it uses the vocabulary of delegation and automation. All three models declined it. Opus named the reason directly: "recurring team ritual redesign, explicitly excluded from delegate."

That is the last sentence of the description doing its job, and it is the argument for keeping the deferral clause even though it costs characters in a listing that gets truncated.

---

## Case 10, a genuine split

Haiku routed it to `optimize-tokens`. Sonnet and Opus routed it to `delegate`. Both readings are defensible: the message is a bulk request, which is what `optimize-tokens` watches for, and it is also a person asking whether to hand something over, which is what `delegate` watches for.

**Left as is, deliberately.** The two skills answer different halves of that question. `delegate` decides whether the work should be handed over and what would catch it being wrong. `optimize-tokens` decides how to run it cheaply once it is. A session that opens with either one lands somewhere useful.

The available fix would be a clause in `delegate` about batch work put to a model, and it was rejected because it would very likely also pull case 8 away from `optimize-tokens`, converting one acceptable split into one clear regression.

**Recheck this case if** either description changes, or if a third skill lands in the same territory.

---

## Run 2, 29 Aug 2026

The delegate cases were rerun inside the full harness, alongside the cases for the other three skills.

| # in run 2 | Message | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- |
| 11 | "I've got to put together the quarterly board deck. How much of this should I just get you to do?" | delegate | delegate | delegate |
| 12 | "Should I automate my weekly invoice chasing or keep doing it myself?" | delegate | delegate | delegate |
| 13 | "Our sprint retro happens every two weeks and it is a mess. Help me redesign the ritual." | none | none | none |
| 14 | "I am about to have Claude process 200 customer emails and pull out the themes. Is that a good idea?" | delegate | delegate | delegate |
| 15 | "Should I pay for a tool that would do this whole task for me automatically?" | before-you-install | before-you-install | before-you-install |

**Case 14 did not reproduce its split.** In run 1 Haiku sent it to `optimize-tokens`; in run 2 all three sent it to `delegate`.

Do not read that as the split being fixed. The `optimize-tokens` description was rendered differently between the two runs, with run 2 including its clause about tasks that genuinely need full token usage. The runs are not comparable, and the honest conclusion is narrower and more useful than "resolved": **a routing result holds for one exact rendering of the descriptions and does not survive rewording them.** Anything compared across runs has to pin the description text.

The disposition of case 14 is unchanged. Left as is, for the reasons above.

**Case 15 is new** and was written as a contest between `delegate` and `before-you-install`. It is not one. All three picked `before-you-install`, which is correct: the purchase is the irreversible half of that question.

---

## Not tested here

- **Whether the description survives the listing budget.** Routing was tested with all four descriptions shown in full. In a real installation with many skills the listing is truncated, and a new skill with no invocation history loses its description first. That is a property of the installation, not of the skill, and this harness cannot see it.
- **Output quality.** These cases test which skill fires, not whether the skill then produces a filled allocation table rather than advice. The output check belongs in the harness under issue #5.
- **Real sessions.** Every case here is a constructed message. Nothing in this file is evidence that the skill fires in the wild.

---

## Run 3, 29 Aug 2026, rechecked for issues #9 and #10

`optimize-tokens` and `chat-context` both had their descriptions rewritten this run, and this skill sits between them, so its cases were put through the harness again rather than assumed stable.

No case here changed disposition. Cases 11 and 12 (board deck, invoice automation) still fire on all three. Case 13 (sprint retro) still declines on all three, the ritual exclusion still cited by name. Case 14 (200 customer emails) still fires delegate on all three, continuing not to reproduce the run 1 split, which run 2 already established is a property of the exact wording in play rather than a resolved question. Case 15 (pay for a tool that automates the whole task) still splits the same way it always has: two of three send it to `before-you-install`, one sends it to `delegate`. See `evals/optimize-tokens.md` for the full table.

Full detail on what changed and why is in `evals/optimize-tokens.md` and `evals/chat-context.md`. Nothing in this file needed to change.

---

## Note, 29 Aug 2026, stack-audit added

One new case was constructed to check for interference: "Should I automate our quarterly subscription review?" Haiku declined it, Sonnet and Opus sent it to `delegate`. Recorded and left as is in `evals/stack-audit.md`, for the same reason as case 5 and case 13 here: a recurring task described in the vocabulary of automation is this skill's territory, and `stack-audit` does not claim it.
