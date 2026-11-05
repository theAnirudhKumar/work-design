# Evaluation: before-you-switch

Routing cases for `before-you-switch`, run against the six descriptions in this repository as they stand with this skill added. Written alongside the skill, per `CONTRIBUTING.md`.

**Run on:** 31 Aug 2026, against Haiku, Sonnet and Opus.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "What happens if I cancel this and switch to something else? Can I even get my data out?" | fire | before-you-switch | before-you-switch | before-you-switch |
| 2 | "Should I sign up for Linear for our team?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 3 | "We're paying for four project tools nobody's opened in months, help me figure out what to cut." | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 4 | "I want to leave Notion for Obsidian. What am I going to lose in the move?" | fire | before-you-switch | before-you-switch | before-you-switch |
| 5 | "How many hours will it realistically take to migrate our CRM data before I decide whether to switch providers?" | fire | before-you-switch | before-you-switch | before-you-switch |
| 6 | "Can you help me negotiate a better contract with our CRM vendor before renewal?" | none | none | none | none |
| 7 | "audit-my-tools says I should cancel this subscription. Before I actually pull the trigger, what would I lose?" | fire | before-you-switch | before-you-switch | before-you-switch |
| 8 | "Should I automate checking whether we're locked into any of our vendors?" | delegate | delegate | delegate | delegate |

Eight of eight agree across all three models. No split, no disagreement.

---

## Cases 1, 4, 5 and 7, the skill's own territory

Four different phrasings of the same job: what breaks, what is lost, what it costs in hours, and what happens after a cancel verdict is already made. All four fired `before-you-switch` cleanly on every model, including case 7's explicit hand-off from a `audit-my-tools` verdict, which the description names directly ("a audit-my-tools verdict of cancel... needs the actual exit cost checked before anyone acts on it"). That chaining language appears to be doing real work: no model tried to re-run `audit-my-tools` itself or stop at "none" for a case that names another skill by its output.

## Case 2 and case 3, the neighbours hold

Case 2 is a tool not yet adopted, which is `before-you-install`'s territory by the same not-yet-adopted line drawn in `evals/audit-my-tools.md`. Case 3 is existing paid tools nobody uses, which is `audit-my-tools`'s territory. Neither pulled toward `before-you-switch` on any model. `before-you-switch`'s own description states the same boundary from its side ("Use before-you-install for a tool not yet adopted, and audit-my-tools to decide whether a tool should be cancelled in the first place; this one is for what happens after that decision, on the way out"), and the eval confirms the three-way boundary holds from all three directions now that a skill sits on each side of it.

## Case 5, a closer look

Case 5 was written to test whether "before I decide whether to switch" would pull the message toward a bare decision skill instead of the exit-cost skill, since the sentence names a decision that has not been made yet. All three models still routed it to `before-you-switch`, reading "how many hours will it realistically take to migrate" as the operative ask rather than the still-open switch decision. Consistent with the description's own framing: the hours estimate is meant to be an input to the decision, not something that waits for the decision to be made first.

## Case 6, an honest gap

Vendor contract negotiation is not covered by any skill in this repository, same finding as case 5 in `evals/audit-my-tools.md`. All three models declined every skill. `before-you-switch` checks what breaks and what a move costs, not what a renewal costs to negotiate down; nothing in its description reaches toward contract terms as a lever to pull, only as a fact to check (Step 5, exit terms in the notice period and any early-termination fee).

## Case 8, resolved rather than split

This case was built expecting a possible split with `audit-my-tools`, on the same seam as `audit-my-tools`'s own case 7 ("Should I automate our quarterly subscription review"). It did not split. All three models sent it to `delegate` at consistent confidence, reading "should I automate checking" as a delegation decision about a recurring task, not a lock-in check to run once. `before-you-switch` never entered any model's answer for this case, unlike audit-my-tools's case 7 where Sonnet and Opus split between "none" and `delegate`. The extra distance may come from `before-you-switch` describing a per-tool exit decision that ends on a one-time verdict, which reads less like a "recurring review" than `audit-my-tools`'s inventory framing does.

---

## Not tested here

Whether `continue-in-new-chat` or `cut-token-cost` compete with `before-you-switch`. Neither skill's trigger vocabulary overlaps with switching, migration or lock-in language, and none of their own recorded cases mention leaving a tool, so no case was constructed. Worth a check the day either of those descriptions changes again.

**Output behaviour.** Whether the skill actually checks export format before assuming data portability, whether the hours estimate in Step 4 stays in hours rather than drifting into a dollar figure, and whether the verdict in Step 6 names what makes it so rather than just stating a label. All output checks, not routing.

**Real sessions.** Every case here is constructed, same limitation as every other file in this directory.
