# Evaluation: plan-my-week

Routing cases for `plan-my-week`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 33. All three models matched on 33; Haiku 33, Sonnet 33, Opus 33.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The near misses are only meaningful if the full description set is present, including `plan-my-day`, `plan-my-week`, `sort-my-tasks` and the other skills built alongside them: `find-my-method`, `explain-a-method`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life` and `build-my-system`.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Plan my week." | Should fire | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 2 | "Weekly review time. Last week I finished the deck but never got to the budget." | Should fire | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 3 | "It's Monday 8:55. What should this week look like? I've got three big meetings and a deadline Thursday." | Should fire | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 4 | "Set up an ideal week for me. I'm a nurse on three long shifts a week." | Should fire | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 5 | "Plan today. Meeting at 10, school pick-up at 3, and a list of 12 things." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 6 | "Here's everything I need to do this quarter, all 60 items. What first?" | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 7 | "Help me stay focused for the next 90 minutes." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 8 | "My calendar is full of meetings that eat my focus time. What do I do?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 9 | "Which method suits me, weekly reviews or GTD?" | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 10 | "Explain how a weekly review works and whether it's worth it." | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 11 | "I want to make a Sunday planning habit stick." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 12 | "I never see my family and I'm always working. Help me rebalance." | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 13 | "Design my whole productivity system including daily, weekly and monthly reviews." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 14 | "I've got to launch the new pricing page. Where do I start?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 15 | "I only have two weeks to do four weeks of work. What do I cut?" | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 16 | "I keep carrying the same task over every week and can't start it." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 17 | "Should I hand the weekly report to an agent?" | Near miss | delegate | delegate | delegate | delegate |
| 18 | "How long will the migration take, realistically?" | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 19 | "What's in scope for the redesign, and what isn't?" | Near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 20 | "Pre-mortem my plan for next week's conference." | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 21 | "The campaign wrapped up. Run a retro on it." | Near miss | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 22 | "Poke holes in this proposal draft before I send it." | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 23 | "Should I run a weekly team meeting or use a written update?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 24 | "Summarise this chat so I can carry on in a new one." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 25 | "What subscriptions am I paying for that I don't use?" | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 26 | "Is this planner app any good? Check the privacy policy." | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 27 | "What do I lose if I leave my current planner app?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 28 | "How do I cut the token cost of my long planning prompt?" | Near miss | cut-token-cost | cut-token-cost | cut-token-cost | cut-token-cost |
| 29 | "What can work-design do for me?" | Near miss | work-design | work-design | work-design | work-design |
| 30 | "Here's last week's notes and what's due. I want three outcomes for the week and my focus blocks." | Ambiguous | plan-my-week (outcomes and blocks are its job) | plan-my-week | plan-my-week | plan-my-week |
| 31 | "Plan my week and also rank my backlog of 50 things." | Ambiguous | plan-my-week or sort-my-tasks | plan-my-week | plan-my-week | plan-my-week |
| 32 | "Do a weekly review and tell me if I'm balancing work and life." | Ambiguous | plan-my-week or balance-my-life | plan-my-week | plan-my-week | plan-my-week |
| 33 | "I'm burned out and can't face the week. Can you plan it?" | Ambiguous, boundary | plan-my-week, with the one-time referral | plan-my-week | plan-my-week | plan-my-week |

---

## What each case tests

**1 to 4, should fire.** A bare request, a review-first request, a Monday-morning request with fixed items, and a shift worker asking for an ideal week. Case 4 tests that a skeleton is built without theme days that the work does not allow.

**5, plan-my-day.** One day with fixed times.

**6, sort-my-tasks.** A long quarterly list needing a rank, not a week.

**7, start-a-focus-session.** One session.

**8, protect-my-focus.** Calendar interruptions as the problem, with negotiation and an experiment. The plan-my-week step on protected blocks overlaps in vocabulary.

**9, find-my-method and 10, explain-a-method.** Choosing a method and explaining one. Both name the weekly review.

**11, build-a-habit.** A recurring behaviour to start. The Sunday planning habit is the overlap risk.

**12, balance-my-life.** The whole life, not one week.

**13, build-my-system.** A full system with reviews built in. This is where the review habit and tools belong.

**14, plan-the-work.** One piece of work at its start.

**15, fit-to-deadline.** Scope against a fixed date.

**16, get-unstuck.** A repeated carry-over with a stall. The skill's own carry-twice rule hands this off, but a message that is only about the stall goes to `get-unstuck`.

**17, delegate.** Allocating one piece of work.

**18, how-long-will-it-take.** An estimate check.

**19, scope-the-work.** Boundaries of one piece of work.

**20, what-could-go-wrong.** Pre-mortem of a plan. The week plan has one risk with an if-then; this is the full stress test.

**21, lessons-learned.** A retro on finished work, not a weekly look back.

**22, review-my-work.** Quality of a draft.

**23, meeting-or-message.** Channel choice.

**24, continue-in-new-chat.** Carrying context.

**25, audit-my-tools.** Subscriptions.

**26, before-you-install.** Vetting one tool.

**27, before-you-switch.** Exit cost.

**28, cut-token-cost.** Token economy.

**29, work-design.** The menu.

**30, ambiguous, should lean plan-my-week.** Outcomes and blocks are explicitly named.

**31, ambiguous.** Two jobs in one message. Either first is defensible, and they chain.

**32, ambiguous.** A weekly review with a balance question. The week skeleton has one personal item; the balance check is another skill. A split is probably acceptable.

**33, boundary.** Burnout language. The skill should say once, kindly, that a person who can help is worth talking to, and continue the practical part only if wanted, with a smaller plan if so. It should not diagnose. Checked by reading the output.

---

## Output check

Two cases to be checked by hand once a model is available.

- **Case 2.** The output should contain wins, slips and a carry/delegate/drop verdict on the budget (not a silent rollover), then no more than three outcomes, a skeleton with named focus blocks, one risk with an if-then, and one personal item placed on the calendar. It should not be a list of tasks sorted by day.
- **Case 4.** The output should avoid theme days that shift work would break, offer half-days or none, and say why.

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

No misses on cases with a single expected answer.
