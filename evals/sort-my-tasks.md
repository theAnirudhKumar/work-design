# Evaluation: sort-my-tasks

Routing cases for `sort-my-tasks`, written alongside the skill. **No results are recorded.** The Haiku, Sonnet and Opus columns read "not yet run" because these cases have not been put to any model. Only the expected routing is filled in, and it is a prediction from reading the descriptions, not a finding.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The near misses are only meaningful if the full description set is present, including `plan-my-day`, `plan-my-week`, `sort-my-tasks` and the other skills built alongside them: `find-my-method`, `explain-a-method`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life` and `build-my-system`.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I have too much to do. Here's my list, can you prioritize it?" | Should fire | sort-my-tasks | not yet run | not yet run | not yet run |
| 2 | "Brain dump incoming: invoices, call the school, fix the gutter, update CV, gym?, order labels, taxes, that email to Priya, the Priya invoice thing. What first?" | Should fire | sort-my-tasks | not yet run | not yet run | not yet run |
| 3 | "Everything feels urgent. Help me work out which of these actually matter." | Should fire | sort-my-tasks | not yet run | not yet run | not yet run |
| 4 | "I've got five possible projects for next quarter and I can only do two. Rank them." | Should fire | sort-my-tasks | not yet run | not yet run | not yet run |
| 5 | "Give me my top 6 for tomorrow from this list, Ivy Lee style." | Should fire | sort-my-tasks | not yet run | not yet run | not yet run |
| 6 | "Build my schedule for today. I've got meetings at 10 and 2." | Near miss | plan-my-day | not yet run | not yet run | not yet run |
| 7 | "What should this week look like? I want three outcomes and focus blocks." | Near miss | plan-my-week | not yet run | not yet run | not yet run |
| 8 | "I need to focus for an hour on one of these. Set me up." | Near miss | start-a-focus-session | not yet run | not yet run | not yet run |
| 9 | "People keep dropping tasks on me all day. How do I stop it?" | Near miss | protect-my-focus | not yet run | not yet run | not yet run |
| 10 | "Which prioritisation method should I be using in general?" | Near miss | find-my-method | not yet run | not yet run | not yet run |
| 11 | "What's the difference between Eisenhower and MoSCoW?" | Near miss | explain-a-method | not yet run | not yet run | not yet run |
| 12 | "I want to build a habit of clearing my inbox daily." | Near miss | build-a-habit | not yet run | not yet run | not yet run |
| 13 | "My to-do list is all work. I want a life too. Where does my time go?" | Near miss | balance-my-life | not yet run | not yet run | not yet run |
| 14 | "Set up a system for capturing and organising all my tasks." | Near miss | build-my-system | not yet run | not yet run | not yet run |
| 15 | "I have to organise the conference. Where do I start?" | Near miss | plan-the-work | not yet run | not yet run | not yet run |
| 16 | "I have to ship by the 20th and this list is double what fits. Cut the scope to fit." | Near miss | fit-to-deadline | not yet run | not yet run | not yet run |
| 17 | "One thing on my list has been there for six weeks. I can't start it." | Near miss | get-unstuck | not yet run | not yet run | not yet run |
| 18 | "Which of these tasks can I give to an AI?" | Near miss | delegate | not yet run | not yet run | not yet run |
| 19 | "How long will this whole list take?" | Near miss | how-long-will-it-take | not yet run | not yet run | not yet run |
| 20 | "What exactly is included in the migration project?" | Near miss | scope-the-work | not yet run | not yet run | not yet run |
| 21 | "What are the risks to this plan?" | Near miss | what-could-go-wrong | not yet run | not yet run | not yet run |
| 22 | "The release is done. What should we do differently next time?" | Near miss | lessons-learned | not yet run | not yet run | not yet run |
| 23 | "Check my analysis for holes." | Near miss | review-my-work | not yet run | not yet run | not yet run |
| 24 | "Should I handle this by email or set up a call?" | Near miss | meeting-or-message | not yet run | not yet run | not yet run |
| 25 | "Summarise this chat for a fresh one." | Near miss | continue-in-new-chat | not yet run | not yet run | not yet run |
| 26 | "Which of my tools do we pay for twice?" | Near miss | audit-my-tools | not yet run | not yet run | not yet run |
| 27 | "Is this to-do app safe to use?" | Near miss | before-you-install | not yet run | not yet run | not yet run |
| 28 | "What do I lose if I leave Todoist?" | Near miss | before-you-switch | not yet run | not yet run | not yet run |
| 29 | "How do I reduce the tokens in my prompts?" | Near miss | cut-token-cost | not yet run | not yet run | not yet run |
| 30 | "Which work-design skill should I start with?" | Near miss | work-design | not yet run | not yet run | not yet run |
| 31 | "Here's my list. Rank it and then lay out tomorrow around my meetings." | Ambiguous | sort-my-tasks first, then plan-my-day | not yet run | not yet run | not yet run |
| 32 | "My list is huge and the deadline is Friday. What do I do?" | Ambiguous | sort-my-tasks or fit-to-deadline | not yet run | not yet run | not yet run |
| 33 | "Should I say yes to these four invitations?" | Ambiguous | sort-my-tasks (Hell yeah or no) or meeting-or-message | not yet run | not yet run | not yet run |
| 34 | "I'm so overwhelmed I can't even look at the list. Not just this list, everything." | Ambiguous, boundary | sort-my-tasks, with the one-time referral | not yet run | not yet run | not yet run |

---

## What each case tests

**1 to 5, should fire.** A plain ask, a messy dump with duplicates (the Priya items), a "everything is urgent" ask, a projects ranking (which should use RICE or impact/effort, not Eisenhower) and an explicit Ivy Lee request.

**6, plan-my-day.** The ask is a schedule, not a rank.

**7, plan-my-week.** Outcomes and blocks for a week.

**8, start-a-focus-session.** One session.

**9, protect-my-focus.** Incoming demands as the problem.

**10, find-my-method.** Choosing a method in general. This skill chooses a ranking method for one list.

**11, explain-a-method.** Comparing two named methods. The names overlap with this skill's method table.

**12, build-a-habit.** A recurring behaviour.

**13, balance-my-life.** Life areas across the list, not a ranking.

**14, build-my-system.** The system for capture and organisation. This skill sorts one list.

**15, plan-the-work.** One project at its start.

**16, fit-to-deadline.** Scope against a date. The handoff in Step 6 exists for this boundary.

**17, get-unstuck.** One stalled item.

**18, delegate.** Allocation, though this skill's Delegate list overlaps.

**19, how-long-will-it-take.** An estimate.

**20, scope-the-work.** One project's boundary.

**21, what-could-go-wrong.** Plan risks.

**22, lessons-learned.** A retro.

**23, review-my-work.** Quality of a deliverable.

**24, meeting-or-message.** Channel choice.

**25, continue-in-new-chat.** Context carrying.

**26, audit-my-tools.** Subscriptions.

**27, before-you-install.** Vetting a tool.

**28, before-you-switch.** Exit cost.

**29, cut-token-cost.** Token economy.

**30, work-design.** The menu.

**31, ambiguous.** Two jobs in order; sort first is the likelier. They chain.

**32, ambiguous.** A list too big for a deadline. Sorting is the first move; fitting scope may be the real problem. Decide in writing after a run whether either routing is acceptable.

**33, ambiguous.** Invitations to accept or decline fit Hell yeah or no, which this skill applies, and also a channel decision. Either is defensible.

**34, boundary.** Overwhelm beyond one list. The skill should say once, kindly, that a person who can help is worth talking to, and continue the practical part only if wanted. It should not diagnose. Checked by reading the output.

---

## Output check

Two cases to be checked by hand once a model is available.

- **Case 2.** The output should merge the two Priya items, split anything compound, rewrite vague items such as "taxes" as actions, name one method with a one-line reason, produce a numbered list with no ties and a capped top tier, give a first physical action for the top 3, and sort the rest into Delete, Defer (with a date or trigger), Delegate and Not doing, each with a reason. It should not use high, medium and low labels.
- **Case 4.** The output should choose RICE or impact/effort (not Eisenhower) and say why in one line, and label any estimate as an assumption.

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.
