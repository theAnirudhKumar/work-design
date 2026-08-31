# Evaluation: estimate-from-precedent

Routing cases for `estimate-from-precedent`, run against the nine descriptions in this repository as they stand with this skill added. Written alongside the skill, per `CONTRIBUTING.md`.

**Run on:** 31 Aug 2026, against Haiku, Sonnet and Opus.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "How long will this website redesign actually take? We always seem to run over on these." | fire | estimate-from-precedent | estimate-from-precedent | estimate-from-precedent |
| 2 | "I'm budgeting two weeks for this migration, is that realistic based on past projects?" | fire | estimate-from-precedent | estimate-from-precedent | estimate-from-precedent |
| 3 | "How much will this project cost us in total, including the contractor?" | none | none | none | none |
| 4 | "I've scoped this project out, now I need to know if the timeline I have in mind is realistic before I commit to it." | fire | estimate-from-precedent | estimate-from-precedent | estimate-from-precedent |
| 5 | "Should I sign up for Figma for the design team?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 6 | "We've never done anything like this before, how long do you think it'll take?" | split, see below | none | estimate-from-precedent | estimate-from-precedent |
| 7 | "What should I hand to Claude versus keep for myself on this migration?" | delegate | delegate | delegate | delegate |
| 8 | "How locked in are we to this vendor if we wanted to leave?" | switch-cost | switch-cost | switch-cost | switch-cost |
| 9 | "Sanity check my estimate: I think this will take about three days." | fire | estimate-from-precedent | estimate-from-precedent | estimate-from-precedent |

Eight of nine agree across all three models. Case 6 splits.

---

## Cases 1, 2, 4 and 9, the skill's own territory

Four shapes of the same request: a duration question with an admitted history of running over, a stated estimate checked against past projects, the explicit hand-off from a finished scope-the-work boundary note, and a bare "sanity check my estimate" with a number attached. All four fired `estimate-from-precedent` cleanly on every model, including case 4's chained hand-off, which the description names directly ("when a scope-the-work boundary note or a delegate allocation needs a time figure attached before anyone commits to it").

## Case 3, an explicit exclusion holding

Cost in money, not time, and the skill's own description excludes it by name ("Not for estimating cost in money"). All three models declined every skill, and none in this repository covers project costing as of this eval. A clean, deliberate boundary rather than a gap.

## Case 5, 7 and 8, the neighbours hold

Case 5 (adopting a new tool) went to `before-you-install`, case 7 (AI vs. self split) went to `delegate`, case 8 (vendor lock-in) went to `switch-cost`. None pulled toward `estimate-from-precedent` despite each being a decision with a time or effort dimension somewhere nearby. The boundary holds from the neighbouring skills' side with the ninth skill in the mix.

## Case 6, a genuine split

"We've never done anything like this before, how long do you think it'll take?" was built to test the skill's own stated limit: it does not work without a comparable past case, and this message says outright that no comparable case exists. Haiku declined everything, reading the message as ruling out the skill's precondition before it could fire. Sonnet and Opus, both at medium confidence, routed it to `estimate-from-precedent` anyway, reasoning that the skill's job includes discovering there is no reference class and saying so, which is explicitly Step 2's documented behavior ("If nothing comparable exists, say so plainly and stop here").

**Left as is, deliberately.** Both readings are defensible from the description as written: one treats "no comparable case exists" as excluding the skill before it starts, the other treats it as the exact situation Step 2 is built to handle and report on. The split is a genuine ambiguity in how explicitly a precondition has to be stated in the trigger language before a model will route to a skill whose own job includes checking that precondition. No fix attempted here; narrowing the description to force one reading would likely cost clarity on the more common case (an estimate exists and needs checking) to resolve an edge case this rare.

---

## Not tested here

Whether `chat-context`, `optimize-tokens` or `pick-the-medium` compete with `estimate-from-precedent`. None of their trigger vocabularies overlap with estimation, duration or precedent language, and none of their own recorded cases mention time estimates, so no case was constructed. Worth a check the day any of those descriptions change again.

**Output behaviour.** Whether the reference class actually gets checked for best-case bias, whether the adjusted estimate stays a range rather than false precision, and whether a forced or single-case reference class gets flagged rather than accepted. All output checks, not routing.

**Real sessions.** Every case here is constructed, same limitation as every other file in this directory.
