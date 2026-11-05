# Evaluation: plan-the-work

Routing cases for `plan-the-work`, written alongside the skill, per `CONTRIBUTING.md`.

**Status: not yet run.** The results columns below are empty on purpose. No model has been put through these cases, and nothing in this file is a result. Only the expected routing is filled in, and it is a prediction from reading the descriptions, not an observation. Run the procedure in `evals/README.md` on Haiku, Sonnet and Opus and fill the columns in from the real output, including any disagreement.

**Siblings named below.** `fit-to-deadline` is written alongside this skill. `what-could-go-wrong`, `get-unstuck`, `review-my-work` and `lessons-learned` are planned siblings that may not exist yet when this is run. Where a sibling is not installed, the expected routing for that case is `none`, not the sibling's name. Pin the exact description text of every skill shown to the model when recording a run.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I have to write the Q3 report for the board and I don't know where to start." | should fire | plan-the-work | not yet run | not yet run | not yet run |
| 2 | "Help me get started on my thesis chapter on migration data." | should fire | plan-the-work | not yet run | not yet run | not yet run |
| 3 | "I'm about to start planning our product launch. Can you turn this into a plan?" | should fire | plan-the-work | not yet run | not yet run | not yet run |
| 4 | "What should I do first on this lab protocol validation? Break it down for me." | should fire | plan-the-work | not yet run | not yet run | not yet run |
| 5 | "Make a work card for the new onboarding emails." | should fire | plan-the-work | not yet run | not yet run | not yet run |
| 6 | "I have until Friday to finish this deck and there's way too much in it. What can I drop?" | near miss | fit-to-deadline | not yet run | not yet run | not yet run |
| 7 | "My client keeps adding things to the website project. Help me write down what's in and what's out." | near miss | scope-the-work | not yet run | not yet run | not yet run |
| 8 | "Should I give the competitor research to Claude or do it myself?" | near miss | delegate | not yet run | not yet run | not yet run |
| 9 | "How long will this migration actually take? I've said three weeks." | near miss | how-long-will-it-take | not yet run | not yet run | not yet run |
| 10 | "Should this be a meeting or can I just send a message?" | near miss | meeting-or-message | not yet run | not yet run | not yet run |
| 11 | "Fix this meeting invite and tighten my agenda for the kickoff." | near miss | meeting-design | not yet run | not yet run | not yet run |
| 12 | "I've been stuck on this section for two days and can't move." | near miss | none (or `get-unstuck` if installed) | not yet run | not yet run | not yet run |
| 13 | "Here's my plan for the rollout. What could go wrong with it?" | near miss | none (or `what-could-go-wrong` if installed) | not yet run | not yet run | not yet run |
| 14 | "Rename this file to match the others." | near miss | none (task under 30 minutes) | not yet run | not yet run | not yet run |
| 15 | "I have to prepare the wedding seating plan, we have 12 days, and it's already too much." | conflict | plan-the-work or fit-to-deadline | not yet run | not yet run | not yet run |
| 16 | "I've got a proposal due Thursday for a client. Plan this out and tell me what to cut if I run short." | conflict | plan-the-work or fit-to-deadline | not yet run | not yet run | not yet run |

---

## Notes on what each case is testing

**Cases 1 to 5, should fire.** Each uses a literal trigger phrase from a different field (board report, thesis, launch, lab work, onboarding emails), because the skill claims to work in any domain. Case 5 uses the card's own name. Case 1 is the plainest "where do I start" shape.

**Case 6, `fit-to-deadline`.** The user has a fixed date and too much work, and asks what to drop. That is `fit-to-deadline`'s own territory. A pass here means `plan-the-work` does not claim "fit this in the time". A failure would show up as `plan-the-work` winning on the word "finish".

**Case 7, `scope-the-work`.** The person is in a dispute with a requester over what is included, and wants a written boundary. The `plan-the-work` description defers this explicitly. A pass means the deferral clause works.

**Case 8, `delegate`.** A hand-off question about one piece of work. `plan-the-work` includes a "who or what helps" line, so a model might claim it.

**Case 9, `how-long-will-it-take`.** A duration check against a claimed estimate. A card sets an appetite, which is a decision, not an estimate. A model that routes this to `plan-the-work` has missed the difference.

**Case 10, `meeting-or-message`.** A channel decision. Nothing in it should reach toward a card.

**Case 11, `meeting-design`.** A meeting that needs designing is not a piece of work needing a card. This is a boundary against the meeting-design repository, which may not be installed alongside. If it is not installed, the expected routing is `none`.

**Cases 12 and 13, planned siblings.** Being stuck, and stress-testing an existing plan. Both share vocabulary with a card ("plan", "stuck on"). These cases are the reason the description says the card is for work about to begin. If the sibling is absent, `plan-the-work` should still not fire: the user already has a plan, or has already started.

**Case 14, the too-small task.** The skill's own "when not to make a card" rule. A pass is `none`, or `plan-the-work` firing and answering with the first move only. A full card for a file rename is a failure. Record which happened.

**Cases 15 and 16, genuine conflicts.** Each could fairly start with either skill. Case 15 has a time limit ("12 days") and an overload ("already too much"), so `fit-to-deadline` is the stronger claim, but the user has also not said what the plan is. Case 16 asks for both a plan and cuts. There is no expected winner. Record what each model did and decide in writing whether the split is acceptable. One reasonable answer is that either order leads somewhere useful, since `plan-the-work` names `fit-to-deadline` as its hand-off for a time-box problem.

---

## To check by hand, after a routing pass

Routing cases cannot tell whether the skill then produces what it promises. On one case, read the output and check:

- All ten sections appear in the stated order, on one page.
- At most three questions, placed after the card, each naming the line it would change.
- The outcome is a result, not an activity.
- The tripwire has a date or time in it and a concrete action.
- "What I had to assume" is filled in and is not empty.
- For a task under about 30 minutes, the skill gives the first move and no card.

---

## Not tested here

- **Whether the description survives the listing budget** in a real installation. A new skill has no invocation history and is first to lose its description text when the listing overflows.
- **Real sessions.** Every case is a constructed message written by the author of the skill.
- **Wording stability.** A result holds for one rendering of the descriptions. Record the exact text next to any run.
