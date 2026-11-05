# Evaluation: plan-my-day

Routing cases for `plan-my-day`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 34. All three models matched on 34; Haiku 34, Sonnet 34, Opus 34.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The near misses are only meaningful if the full description set is present, including `plan-my-day`, `plan-my-week`, `sort-my-tasks` and the other skills built alongside them: `find-my-method`, `explain-a-method`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life` and `build-my-system`.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Plan my day. I've got a client call at 11, a dentist at 3:30 and about 14 things I want to get done." | Should fire | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 2 | "I have six hours today and way too many tasks. Can you time block it for me?" | Should fire | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 3 | "It's 1pm, the morning got away from me. Reset my day." | Should fire | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 4 | "Bad day, barely slept. What's the minimum I should get done?" | Should fire | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 5 | "I'm on nights this week and wake at 4pm. Plan my day around that." | Should fire | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 6 | "Plan my week. I've got a conference Wednesday and a launch on Friday." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 7 | "Here's my brain dump of 40 things. Which ones actually matter?" | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 8 | "Help me focus for the next hour. I need to finish one section of my report." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 9 | "I'm interrupted every ten minutes at work. Slack and meetings eat my whole day." | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 10 | "What productivity method should I use? I've tried five and none stuck." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 11 | "How does time blocking actually work? Is it worth it?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 12 | "I want to start journaling every morning but I keep forgetting." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 13 | "I work all the time and never see my friends. Where does my time go?" | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 14 | "Set up my whole productivity system: inbox, review, planning, all of it." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 15 | "I have to write the grant application. Where do I start?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 16 | "I have to finish this by Friday but I only have two days. What can I cut?" | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 17 | "I've been putting off the tax paperwork for weeks and can't start." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 18 | "Should I give the data cleanup to an agent or do it myself?" | Near miss | delegate | delegate | delegate | delegate |
| 19 | "How long will the report really take? I think four hours." | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 20 | "What counts as done for the website project, and what's out of scope?" | Near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 21 | "What could go wrong with my plan for Thursday's product launch?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 22 | "The project's finished. What did we learn?" | Near miss | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 23 | "Is this email good enough to send to the board?" | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 24 | "Should I send a message or call a meeting about the budget change?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 25 | "This chat is huge. Write a handoff so I can continue in a fresh one." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 26 | "Which of my subscriptions should I cancel?" | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 27 | "Is this new calendar app safe to sign up for?" | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 28 | "What breaks if I move off Notion to Obsidian?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 29 | "How do I cut the token cost of this long prompt?" | Near miss | cut-token-cost | cut-token-cost | cut-token-cost | cut-token-cost |
| 30 | "Which work-design skill should I use for my work?" | Near miss | work-design | work-design | work-design | work-design |
| 31 | "I use Ivy Lee. Here are my six for tomorrow and my calendar. Lay out the day." | Ambiguous | plan-my-day (method named, but the job is the day) | plan-my-day | plan-my-day | plan-my-day |
| 32 | "I have too much to do today and don't know where to start." | Ambiguous | plan-my-day or sort-my-tasks | sort-my-tasks | plan-my-day | plan-my-day |
| 33 | "Plan my Monday. And honestly the whole week is a mess." | Ambiguous | plan-my-day or plan-my-week | plan-my-week | plan-my-week | plan-my-day |
| 34 | "I'm exhausted and overwhelmed. Not just today, it's been months. Can you plan my day?" | Ambiguous, boundary | plan-my-day, with the one-time referral | plan-my-day | plan-my-day | plan-my-day |

---

## What each case tests

**1 to 5, should fire.** Literal phrases and close paraphrases across a freelancer, a person with a time budget, a mid-day reset, a bad day and a night-shift worker. Case 5 tests that irregular hours are handled, not assumed away.

**6, plan-my-week.** The unit is the week and the ask is about outcomes and protected time. The day planner takes one day from the week skeleton.

**7, sort-my-tasks.** A big dump where the question is what matters, not when. "Which ones actually matter" is ranking.

**8, start-a-focus-session.** One hour on one task. No schedule is wanted.

**9, protect-my-focus.** Interruptions are the problem; a plan will not fix them.

**10, find-my-method and 11, explain-a-method.** Method choice and method explanation. Case 11 names time blocking, which plan-my-day also applies; the question is how it works, not to build a day.

**12, build-a-habit.** A daily behaviour to start, not a day to plan.

**13, balance-my-life.** Where time goes across life areas. The word "time" is the risk.

**14, build-my-system.** A whole system, not one day.

**15, plan-the-work.** One piece of work at the start. Here it would be a block in a day, but the request is framing the work.

**16, fit-to-deadline.** A fixed deadline with too much scope. The day planner cuts for a day; this one cuts scope for a date.

**17, get-unstuck.** One stalled item.

**18, delegate.** Allocation of one piece of work.

**19, how-long-will-it-take.** An estimate check. The day planner uses estimates but does not correct them.

**20, scope-the-work.** Boundaries of one piece of work.

**21, what-could-go-wrong.** Stress-testing a plan for an event. "Plan" and "Thursday" are the overlap risk.

**22, lessons-learned.** A retro on finished work.

**23, review-my-work.** Quality of a draft.

**24, meeting-or-message.** A communication channel choice.

**25, continue-in-new-chat.** Carrying chat context.

**26, audit-my-tools.** Subscription clean-up.

**27, before-you-install.** Vetting one tool.

**28, before-you-switch.** Exit cost of a tool.

**29, cut-token-cost.** Token economy.

**30, work-design.** The menu skill.

**31, ambiguous.** A method named but the job is a day. Plan-my-day should take it and use the method.

**32, ambiguous.** "Too much to do today" fits ranking and scheduling. Either is defensible. Decide in writing after a run whether the split is acceptable; the skills chain.

**33, ambiguous.** A day and a week in one message. Either first is defensible.

**34, boundary.** Sustained distress beyond a hard day. The skill should say once, kindly, that a person who can help is worth talking to, continue the practical part only if wanted, and not diagnose. Checked by reading the output.

---

## Output check

Two cases to be checked by hand once a model is available.

- **Case 1.** The output should show a capacity sum, say plainly if the list is more than fits and cut it, give one to three must-dos, a schedule with a buffer after the call and a named slack block, a not-today list with a landing place for each item, a slip rule and a one-line shutdown. It should not assume an empty day.
- **Case 4.** The output should be a minimum viable day: three small wins, not a block schedule.

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

No misses on cases with a single expected answer.
