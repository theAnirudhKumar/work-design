# Evaluation: fit-to-deadline

Routing cases for `fit-to-deadline`, written alongside the skill, per `CONTRIBUTING.md`.

**Run on:** 5 Nov 2026, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `c4b8a8cfab44`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 16. All three models matched on 16; Haiku 16, Sonnet 16, Opus 16. The protect-my-focus description was reworded after this run; see the targeted rerun in `evals/README.md`.

**Siblings named below.** `plan-the-work` is written alongside this skill. `what-could-go-wrong`, `get-unstuck`, `review-my-work` and `lessons-learned` are planned siblings that may not exist yet when this is run. Where a sibling is not installed, the expected routing for that case is `none`, not the sibling's name. Pin the exact description text of every skill shown to the model when recording a run.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I only have two days to get this client deck done and there's way too much in it. What can I drop?" | should fire | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 2 | "What's the minimum version of this grant application that still counts? It's due Friday." | should fire | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 3 | "I'm running out of time on the conference talk. Help me cut it down." | should fire | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 4 | "How do I fit a full literature review into the three weeks I have left?" | should fire | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 5 | "I've got a whole afternoon for a task that should only take an hour. What should I do with the rest?" | should fire (inverse) | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 6 | "I have to build the new pricing page. Where do I start?" | near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 7 | "My stakeholder keeps adding requirements. Help me write down what's in scope and what's out." | near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 8 | "I think this will take two weeks. Is that realistic given how long the last one took?" | near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 9 | "Which parts of this analysis should I give to Claude and which should I keep?" | near miss | delegate | delegate | delegate | delegate |
| 10 | "This meeting is 90 minutes and we only have 30. Fix the agenda." | near miss | meeting-design | meeting-design | meeting-design | meeting-design |
| 11 | "Should I send a message or call a meeting about the deadline change?" | near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 12 | "I've been stuck on the same chapter for a week." | near miss | none (or `get-unstuck` if installed) | get-unstuck | get-unstuck | get-unstuck |
| 13 | "Here's my launch plan. What are the ways it could fail?" | near miss | none (or `what-could-go-wrong` if installed) | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 14 | "Make the deadline Friday instead of Wednesday, there's too much to do." | near miss / trap | fit-to-deadline, but it should push back | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 15 | "The report is due Thursday and I haven't decided what it's even for. Plan this and tell me what to cut." | conflict | plan-the-work or fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 16 | "I have 10 hours for the product demo. Is that enough or too much?" | conflict | fit-to-deadline or how-long-will-it-take | fit-to-deadline | fit-to-deadline | fit-to-deadline |

---

## Notes on what each case is testing

**Cases 1 to 4, should fire.** Four fields (a client deck, a grant application, a conference talk, a literature review), each with a fixed time and more work than fits. Case 2 uses "minimum version", the skill's own term.

**Case 5, the inverse.** The work is smaller than the time. The description says the skill handles this. A model that sees no "too much" may not route here. A pass is `fit-to-deadline` firing and answering with raise-the-bar, stop-early, or add-one-named-part. Check the output, not just the routing.

**Case 6, `plan-the-work`.** The user has not started and has no outcome or deadline. This is the start-of-work card, not a time-box fix. A pass means `fit-to-deadline` does not claim every task.

**Case 7, `scope-the-work`.** A boundary dispute with a requester. `fit-to-deadline` says in its description that it is not a boundary note.

**Case 8, `how-long-will-it-take`.** A duration check against past work. `fit-to-deadline` starts from a time budget, not a guess about duration. The nearest case in the set, and the most likely to split.

**Case 9, `delegate`.** Allocation of parts. No time budget is the question.

**Case 10, `meeting-design`.** A meeting that is too long for its slot has the vocabulary of fitting (90 minutes in 30), but is a meeting problem. If `meeting-design` is not installed, the expected routing is `none`. A model that routes this to `fit-to-deadline` has pattern-matched on "too long".

**Case 11, `meeting-or-message`.** A channel decision about a deadline change, with the word "deadline" in it.

**Cases 12 and 13, planned siblings.** Being stuck, and stress-testing a plan. Neither has a time budget to shrink to. If the sibling is absent, `fit-to-deadline` should still not fire.

**Case 14, the deadline trap.** The user asks to lengthen the deadline. The skill's rule is that it never lengthens the deadline unless it says plainly that the Minimum cannot fit and why. The correct behaviour is to fire and push back: ask for the original time, build the ladder against it, and offer more time only as a stated option if the Minimum does not fit. Record whether the model complied by moving the date. That would be a failure of the skill's own rule, not a routing failure.

**Case 15, a genuine conflict.** No outcome has been decided (`plan-the-work`'s territory) and a cut list is requested (`fit-to-deadline`'s). There is no expected winner. Either order is defensible: `plan-the-work` first, then `fit-to-deadline` when a time-box problem shows up. Record what each model did and decide in writing whether the split is acceptable.

**Case 16, a genuine conflict.** "Is that enough or too much" is a sizing question, and also a duration question. `fit-to-deadline` can answer by building a ladder and checking whether the Minimum fits. `how-long-will-it-take` would ask for past cases. No expected winner. Record the split.

---

## To check by hand, after a routing pass

Routing cases cannot tell whether the skill then produces what it promises. On one case, read the output and check:

- Time was converted to working hours and the conversion is shown as an assumption.
- If no time was given, the skill asked once and did not draft before the answer.
- Minimum, Target and Stretch are all present, and the Minimum is tested against the stated outcome.
- The cut list is ranked by outcome lost per hour saved, and each cut has a cost in plain words.
- The midpoint rule names a calendar point and an observable thing.
- The deadline was not extended unless the Minimum was shown not to fit, and the reason was given.
- Every hours figure the user did not supply is marked as a guess.

---

## Not tested here

- **Whether the description survives the listing budget** in a real installation. A new skill has no invocation history and is first to lose its description text when the listing overflows.
- **Real sessions.** Every case is a constructed message written by the author of the skill.
- **Wording stability.** A result holds for one rendering of the descriptions. Record the exact text next to any run.

## Misses and how to read them

No misses on cases with a single expected answer.
