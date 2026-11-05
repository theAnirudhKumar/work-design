# Evaluation: review-my-work

Routing cases for `review-my-work`, written alongside the skill.

**Run on:** 5 Nov 2026, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `c4b8a8cfab44`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 15. All three models matched on 14; Haiku 14, Sonnet 15, Opus 15. The protect-my-focus description was reworded after this run; see the targeted rerun in `evals/README.md`.

**Method (to follow).** Show each model only the skill descriptions in the repository and ask for one skill name or `none`, with a confidence and a one-line reason. Repeat on Haiku, Sonnet and Opus. Record disagreements, not averages.

**Siblings assumed present when run:** `plan-the-work`, `fit-to-deadline`, `get-unstuck`, `lessons-learned`, `what-could-go-wrong`, `scope-the-work`, `delegate`, `how-long-will-it-take`, `meeting-or-message`, `continue-in-new-chat`, `cut-token-cost`, and `meeting-design` from its own repository.

---

## Cases

| # | Kind | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Should fire | "Is this good enough to send? [pasted email to a client about a delay]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 2 | Should fire | "Would you put your name on this? [pasted grant narrative]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 3 | Should fire | "Be a harsh reader. This is my board update. [pasted update]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 4 | Should fire | "Sanity check this market summary Claude wrote for me before I forward it. [pasted summary]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 5 | Should fire | "Red team this draft. It's the abstract for our lab report. [pasted abstract]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 6 | Should fire | "Check my work: here is my summary of the changes in this pull request, will the reviewers understand it? [pasted summary]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 7 | Should not fire | "What could go wrong with this plan? We launch on 3 March." | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 8 | Should not fire | "Should I hand this report to an agent or write it myself? How would I check it?" | delegate | delegate | delegate | delegate |
| 9 | Should not fire | "Fix the typos and tighten the grammar in this paragraph." | none | none | none | none |
| 10 | Should not fire | "Here's a new project. Help me write down what it is, who it's for and what done means." | plan-the-work | **scope-the-work** | plan-the-work | plan-the-work |
| 11 | Should not fire | "I'm stuck on this analysis and can't see how to finish it." | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 12 | Should not fire | "The project is done. What went well and what should we change next time?" | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 13 | Should not fire | "Review this meeting invite and tighten the agenda." | meeting-design | meeting-design | meeting-design | meeting-design |
| 14 | Should not fire | "Write a cover letter for me from this job post." | none | none | none | none |
| 15 | Should not fire | "How long will this take? I think two weeks." | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 16 | Ambiguous | "Review this." with a pasted spec for a feature not yet built | review-my-work or what-could-go-wrong, see below | review-my-work | review-my-work | review-my-work |
| 17 | Ambiguous | "Does this make sense? [pasted two-line message]" | review-my-work or none, see below | review-my-work | review-my-work | review-my-work |
| 18 | Ambiguous | "The agent finished the competitor brief. Can you check it before I send it on?" | review-my-work or delegate, see below | review-my-work | review-my-work | review-my-work |

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

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| review-my-work#10 | "Here's a new project. Help me write down what it is, who it's for and what done " | plan-the-work | **scope-the-work** | plan-the-work | plan-the-work | A real plan-the-work vs scope-the-work overlap on Haiku ("what it is, who it is for, what done means"). |
