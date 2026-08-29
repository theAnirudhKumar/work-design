# Evaluation: stack-audit

Routing cases for `stack-audit`, run against the five descriptions in this repository as they stand with this skill added. Written alongside the skill, per `CONTRIBUTING.md`.

**Run on:** 29 Aug 2026, against Haiku, Sonnet and Opus.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Can you audit our subscriptions and tell me what to cancel?" | fire | stack-audit | stack-audit | stack-audit |
| 2 | "What are we actually paying for across all these tools? Something feels bloated." | fire | stack-audit | stack-audit | stack-audit |
| 3 | "Should I sign up for Notion for the team?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 4 | "We have three note-taking apps and I don't know why. Can you sort this out?" | fire | stack-audit | stack-audit | stack-audit |
| 5 | "Can you help me negotiate a better rate with our CRM vendor before renewal?" | none | none | none | none |
| 6 | "I installed a clipboard manager last month. What did I actually agree to?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 7 | "Should I automate our quarterly subscription review?" | split, see below | none | delegate | delegate |
| 8 | "We are evaluating a document platform for the whole company, six figures, and procurement needs a recommendation from me." | none | none | none | none |

Six of eight agree across all three models. Cases 1, 2 and 4 fire cleanly. Case 7 splits.

---

## Case 3 and case 6, the nearest neighbour holds

`before-you-install` and `stack-audit` sit either side of the same line: whether a tool is already adopted. Case 3 is a single named tool not yet signed up for, and case 6 is a tool already installed where the user asks what they agreed to, which is `before-you-install`'s own after-the-fact clause, not this skill's territory. Both went to `before-you-install` on all three models, and neither pulled toward `stack-audit`. The boundary the description draws, tools already on the books versus a tool not yet adopted, is doing its job.

## Case 5, an honest gap

Vendor rate negotiation is not covered by any skill in this repository. `stack-audit` decides keep or cancel, explicitly not what to pay for a kept tool, and `before-you-install` is a pre-adoption decision. All three models declined every skill rather than forcing a fit. That is `stack-audit`'s own stated boundary working from the outside: the skill said in its own body it is not a negotiation skill, and no model tried to make it one.

## Case 7, a genuine split

"Should I automate our quarterly subscription review" sits at the same seam as `delegate`'s case 5 and case 13: a recurring task, described in the vocabulary of automation. Haiku declined everything. Sonnet and Opus sent it to `delegate`, both at medium confidence, both naming the automation-decision trigger.

**Left as is, deliberately, for the same reason `delegate`'s case 10 was left as is.** The two skills answer different halves of the question. `delegate` decides whether reviewing the stack quarterly should run without the user at all. `stack-audit` is the review itself, the thing that would get delegated or not. A user who asks this question is one step earlier than either skill's job starts, and the honest answer is that `delegate` is the nearer fit because the question is about who does the reviewing, not about what the review finds.

No fix attempted. Adding a recurring-review clause to `stack-audit` would very likely also pull `delegate`'s own case 5 and case 13 away from their exclusion, which is a worse trade than one unforced split.

## Cases 8 and rechecked neighbours

Case 8, the six-figure procurement case from `evals/before-you-install.md`, still declines on all three models with `stack-audit` in the mix. The buying-committee exclusion in `before-you-install`'s own description is what is doing this, unchanged by anything added here.

---

## Not tested here

Whether `chat-context` or `optimize-tokens` compete with `stack-audit`. Neither skill's trigger vocabulary overlaps with subscription or tool-spend language, and none of their own recorded cases mention tools, subscriptions or spend, so no case was constructed. Worth a check the day either of those descriptions changes again.

**Output behaviour.** Whether the skill actually groups by job rather than category, whether the total in Step 5 gets calculated correctly, and whether a card statement pasted in is read correctly. All output checks, not routing.

**Real sessions.** Every case here is constructed, same limitation as every other file in this directory.
