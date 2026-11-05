# Evaluation: what-could-go-wrong

Routing cases for `what-could-go-wrong`, written alongside the skill.

**Run on:** 5 Nov 2026, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `c4b8a8cfab44`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 15. All three models matched on 14; Haiku 14, Sonnet 15, Opus 15. The protect-my-focus description was reworded after this run; see the targeted rerun in `evals/README.md`.

**Method (to follow).** Show each model only the skill descriptions in the repository and ask for one skill name or `none`, with a confidence and a one-line reason. Repeat on Haiku, Sonnet and Opus. Record disagreements, not averages.

**Siblings assumed present when run:** `plan-the-work`, `fit-to-deadline`, `get-unstuck`, `lessons-learned`, `review-my-work`, `scope-the-work`, `delegate`, `how-long-will-it-take`, `meeting-or-message`, `continue-in-new-chat`, `cut-token-cost`, and `meeting-design` from its own repository.

---

## Cases

| # | Kind | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Should fire | "Stress test this plan: we launch the new booking system on 3 March, two people part-time, the old one switches off the same day." | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 2 | Should fire | "Pre-mortem our grant application timeline. Submission is 15 June and we still need two letters of support." | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 3 | Should fire | "What could go wrong with this plan? I'm moving our whole team's files to a new system over one weekend." | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 4 | Should fire | "Assume this fails in six months. Why? We're hiring a head of sales to open a new region." | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 5 | Should fire | "What am I missing? Here's my plan for the product launch: [plan]" | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 6 | Should not fire | "Is this good enough to send to the board? [pasted Q3 update]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 7 | Should not fire | "Poke holes in this draft memo before I send it. [pasted memo]" | review-my-work | review-my-work | review-my-work | review-my-work |
| 8 | Should not fire | "Here's a new project. Help me write down what it is, who it's for and what done means." | plan-the-work | **scope-the-work** | plan-the-work | plan-the-work |
| 9 | Should not fire | "I have two weeks for this. What should I cut so it fits?" | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 10 | Should not fire | "I'm halfway through this project and completely stuck. What do I do?" | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 11 | Should not fire | "How long will this realistically take? I think three weeks." | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 12 | Should not fire | "What's in and what's out for this redesign?" | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 13 | Should not fire | "This meeting keeps going in circles. What if the group can't agree on the vendor? Build me an agenda." | meeting-design | meeting-design | meeting-design | meeting-design |
| 14 | Should not fire | "The project just finished. What did we learn?" | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 15 | Should not fire | "Should I hand this report to an agent or write it myself?" | delegate | delegate | delegate | delegate |
| 16 | Ambiguous | "Is this plan realistic? We want to ship in six weeks." | what-could-go-wrong or how-long-will-it-take, see below | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 17 | Ambiguous | "Review my project plan." | what-could-go-wrong or review-my-work, see below | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 18 | Ambiguous | "Check my plan for the offsite and tell me what could go wrong." | what-could-go-wrong or meeting-design, see below | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |

---

## Notes on the cases that need a decision

**Case 8 (framing) and case 12 (scope).** `plan-the-work` frames the work and `scope-the-work` draws its boundary. Neither is a stress test. If a model sends either to `what-could-go-wrong` because the word "risk" appears in a description, the deferral clause in `what-could-go-wrong` is not working.

**Case 13 (deadlock in a meeting).** `meeting-design` has its own step for planning a deadlock. A model that sends this to `what-could-go-wrong` is matching on "what if". Expected: `meeting-design`.

**Case 16 (is this plan realistic).** "Is this plan realistic" is a literal trigger for `what-could-go-wrong` and "is this timeline realistic" is a trigger for `how-long-will-it-take`. Expected winner: `what-could-go-wrong`, because the message asks about a plan and not a number, but both are acceptable. Decide in writing after the run whether a split is acceptable. Both lead somewhere useful: one finds failure causes and the other corrects the six-week figure.

**Case 17 (review a plan).** "Review" pulls toward `review-my-work`, and "plan" pulls toward `what-could-go-wrong`. Expected: `what-could-go-wrong`, since the object is a plan and not a draft. If a model chooses `review-my-work`, record whether the user's wording suggested a written document. Ambiguity here is real: a written project plan can be read by either.

**Case 18 (offsite).** Planning the offsite itself is `meeting-design`'s territory. A request for what could go wrong with a plan fits `what-could-go-wrong`. No expected winner. Record what each model does.

## What a pass looks like for this file

- **Should fire (1 to 5):** all three models pick `what-could-go-wrong`. Two of three is a finding.
- **Should not fire (6 to 15):** no model picks `what-could-go-wrong`.
- **Ambiguous (16 to 18):** no pass or fail. Record each model's choice and decide in writing.
- **Output check, by hand, on case 1:** the skill produces 5 to 7 plan-specific causes, each with a dated signal, an if-then response and a prevention, one named key assumption with a test that can run this week, a verdict and an assumptions block, and uses no numeric probabilities. Not yet done.

## Not tested here

- Whether the description survives the listing budget in a real installation, which this harness cannot see.
- Output quality across models, beyond the one hand check above.
- Real sessions. Every case is a constructed message written by the same person who wrote the skill.

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| what-could-go-wrong#8 | "Here's a new project. Help me write down what it is, who it's for and what done " | plan-the-work | **scope-the-work** | plan-the-work | plan-the-work | A real plan-the-work vs scope-the-work overlap on Haiku ("what it is, who it is for, what done means"). |
