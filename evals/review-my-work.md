# Evaluation: review-my-work

Routing cases for `review-my-work`, written alongside the skill and not yet run.

**Status: the results columns are "not yet run".** No model has been put to these cases. Nothing below is a result. The "Expected" column is what the description is meant to do, written before any run, and it is a prediction, not an observation. Fill the model columns by following the procedure in `evals/README.md`, pinning the exact description text of every skill shown to the model.

**Method (to follow).** Show each model only the skill descriptions in the repository and ask for one skill name or `none`, with a confidence and a one-line reason. Repeat on Haiku, Sonnet and Opus. Record disagreements, not averages.

**Siblings assumed present when run:** `plan-the-work`, `fit-to-deadline`, `get-unstuck`, `lessons-learned`, `what-could-go-wrong`, `scope-the-work`, `delegate`, `how-long-will-it-take`, `meeting-or-message`, `continue-in-new-chat`, `cut-token-cost`, and `meeting-design` from its own repository.

---

## Cases

| # | Kind | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Should fire | "Is this good enough to send? [pasted email to a client about a delay]" | review-my-work | not yet run | not yet run | not yet run |
| 2 | Should fire | "Would you put your name on this? [pasted grant narrative]" | review-my-work | not yet run | not yet run | not yet run |
| 3 | Should fire | "Be a harsh reader. This is my board update. [pasted update]" | review-my-work | not yet run | not yet run | not yet run |
| 4 | Should fire | "Sanity check this market summary Claude wrote for me before I forward it. [pasted summary]" | review-my-work | not yet run | not yet run | not yet run |
| 5 | Should fire | "Red team this draft. It's the abstract for our lab report. [pasted abstract]" | review-my-work | not yet run | not yet run | not yet run |
| 6 | Should fire | "Check my work: here is my summary of the changes in this pull request, will the reviewers understand it? [pasted summary]" | review-my-work | not yet run | not yet run | not yet run |
| 7 | Should not fire | "What could go wrong with this plan? We launch on 3 March." | what-could-go-wrong | not yet run | not yet run | not yet run |
| 8 | Should not fire | "Should I hand this report to an agent or write it myself? How would I check it?" | delegate | not yet run | not yet run | not yet run |
| 9 | Should not fire | "Fix the typos and tighten the grammar in this paragraph." | none | not yet run | not yet run | not yet run |
| 10 | Should not fire | "Here's a new project. Help me write down what it is, who it's for and what done means." | plan-the-work | not yet run | not yet run | not yet run |
| 11 | Should not fire | "I'm stuck on this analysis and can't see how to finish it." | get-unstuck | not yet run | not yet run | not yet run |
| 12 | Should not fire | "The project is done. What went well and what should we change next time?" | lessons-learned | not yet run | not yet run | not yet run |
| 13 | Should not fire | "Review this meeting invite and tighten the agenda." | meeting-design | not yet run | not yet run | not yet run |
| 14 | Should not fire | "Write a cover letter for me from this job post." | none | not yet run | not yet run | not yet run |
| 15 | Should not fire | "How long will this take? I think two weeks." | how-long-will-it-take | not yet run | not yet run | not yet run |
| 16 | Ambiguous | "Review this." with a pasted spec for a feature not yet built | review-my-work or what-could-go-wrong, see below | not yet run | not yet run | not yet run |
| 17 | Ambiguous | "Does this make sense? [pasted two-line message]" | review-my-work or none, see below | not yet run | not yet run | not yet run |
| 18 | Ambiguous | "The agent finished the competitor brief. Can you check it before I send it on?" | review-my-work or delegate, see below | not yet run | not yet run | not yet run |

---

## Notes on the cases that need a decision

**Case 9 (typos and grammar).** An explicit copyedit request. The description says it is not a copyedit. Expected: none, or an ordinary editing request. A model that picks `review-my-work` is matching on "this paragraph" and ignoring the exclusion.

**Case 8 (delegate).** The message is about a decision not yet made and the design of a check. Expected: `delegate`. If a model picks `review-my-work` because of "check", the delegate deferral is not working.

**Case 13 (meeting invite).** "Review this invite" is a draft, but `meeting-design` owns invites. Expected: `meeting-design`. A split here would show `review-my-work`'s description is too broad for any pasted document.

**Case 16 (spec for something not built).** A spec is a document and also a plan. Expected winner: `review-my-work` if the user wants to know whether the spec reads well and is complete, `what-could-go-wrong` if they want to know whether the build will succeed. The message does not say. Record what each model does.

**Case 17 (very short input).** The skill is proportionate: a two-line message gets verdict, main problem and fix. Routing may reasonably fall to `none` for a trivial message. Record, and decide whether that is acceptable.

**Case 18 (delegated output comes back).** `delegate` designs the hand-off and its checks. Once the work is back, `review-my-work` is the natural reviewer. Expected: `review-my-work`. A split to `delegate` is plausible because of the agent mention, and is acceptable only if recorded.

## What a pass looks like for this file

- **Should fire (1 to 6):** all three models pick `review-my-work`. Two of three is a finding.
- **Should not fire (7 to 15):** no model picks `review-my-work`.
- **Ambiguous (16 to 18):** no pass or fail. Record each model's choice and decide in writing.
- **Output check, by hand, on case 1:** the skill returns a one-line verdict, a 30-second test, three ranked problems each quoting an exact passage, a Substance Test with filler and needs-support passages, a verification list that says which claims it could not check, a fix list ordered by value per minute, and a short keep list, without rewriting the whole draft. Not yet done.

## Not tested here

- Whether the description survives the listing budget in a real installation, which this harness cannot see.
- Output quality across models, beyond the one hand check above.
- Real sessions. Every case is a constructed message written by the same person who wrote the skill.
