# Evaluation: sort-my-tasks

Routing cases for `sort-my-tasks`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 34. All three models matched on 31; Haiku 31, Sonnet 32, Opus 32.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The near misses are only meaningful if the full description set is present, including `plan-my-day`, `plan-my-week`, `sort-my-tasks` and the other skills built alongside them: `find-my-method`, `explain-a-method`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life` and `build-my-system`.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I have too much to do. Here's my list, can you prioritize it?" | Should fire | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 2 | "Brain dump incoming: invoices, call the school, fix the gutter, update CV, gym?, order labels, taxes, that email to Priya, the Priya invoice thing. What first?" | Should fire | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 3 | "Everything feels urgent. Help me work out which of these actually matter." | Should fire | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 4 | "I've got five possible projects for next quarter and I can only do two. Rank them." | Should fire | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 5 | "Give me my top 6 for tomorrow from this list, Ivy Lee style." | Should fire | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 6 | "Build my schedule for today. I've got meetings at 10 and 2." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 7 | "What should this week look like? I want three outcomes and focus blocks." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 8 | "I need to focus for an hour on one of these. Set me up." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 9 | "People keep dropping tasks on me all day. How do I stop it?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 10 | "Which prioritisation method should I be using in general?" | Near miss | find-my-method | **sort-my-tasks** | find-my-method | find-my-method |
| 11 | "What's the difference between Eisenhower and MoSCoW?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 12 | "I want to build a habit of clearing my inbox daily." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 13 | "My to-do list is all work. I want a life too. Where does my time go?" | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 14 | "Set up a system for capturing and organising all my tasks." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 15 | "I have to organise the conference. Where do I start?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 16 | "I have to ship by the 20th and this list is double what fits. Cut the scope to fit." | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 17 | "One thing on my list has been there for six weeks. I can't start it." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 18 | "Which of these tasks can I give to an AI?" | Near miss | delegate | delegate | delegate | delegate |
| 19 | "How long will this whole list take?" | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 20 | "What exactly is included in the migration project?" | Near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 21 | "What are the risks to this plan?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 22 | "The release is done. What should we do differently next time?" | Near miss | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 23 | "Check my analysis for holes." | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 24 | "Should I handle this by email or set up a call?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 25 | "Summarise this chat for a fresh one." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 26 | "Which of my tools do we pay for twice?" | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 27 | "Is this to-do app safe to use?" | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 28 | "What do I lose if I leave Todoist?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 29 | "How do I reduce the tokens in my prompts?" | Near miss | cut-token-cost | cut-token-cost | cut-token-cost | cut-token-cost |
| 30 | "Which work-design skill should I start with?" | Near miss | work-design | work-design | work-design | work-design |
| 31 | "Here's my list. Rank it and then lay out tomorrow around my meetings." | Ambiguous | sort-my-tasks first, then plan-my-day | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 32 | "My list is huge and the deadline is Friday. What do I do?" | Ambiguous | sort-my-tasks or fit-to-deadline | sort-my-tasks | sort-my-tasks | fit-to-deadline |
| 33 | "Should I say yes to these four invitations?" | Ambiguous | sort-my-tasks (Hell yeah or no) or meeting-or-message | **none** | **none** | **none** |
| 34 | "I'm so overwhelmed I can't even look at the list. Not just this list, everything." | Ambiguous, boundary | sort-my-tasks, with the one-time referral | **balance-my-life** | **build-my-system** | **get-unstuck** |

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

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| sort-my-tasks#34 | "I'm so overwhelmed I can't even look at the list. Not just this list, everything" | sort-my-tasks, with the one-time referra | **balance-my-life** | **build-my-system** | **get-unstuck** | Overwhelm boundary case. The models chose balance-my-life, build-my-system and get-unstuck; all defensible. |
| sort-my-tasks#10 | "Which prioritisation method should I be using in general?" | find-my-method | **sort-my-tasks** | find-my-method | find-my-method | Acceptable overlap. A general "which method" question belongs to find-my-method; Haiku chose sort-my-tasks. |
| sort-my-tasks#33 | "Should I say yes to these four invitations?" | sort-my-tasks (Hell yeah or no) or meeti | **none** | **none** | **none** | Acceptable. A yes/no on invitations needs no skill, or either planning skill. |
