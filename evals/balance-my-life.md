# Evaluation: balance-my-life

Routing cases for `balance-my-life`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 20. All three models matched on 19; Haiku 19, Sonnet 20, Opus 20.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used. Skills named below that are not in the repository must be present in the description set. Near misses name skills that are being added alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`); their descriptions must be in the set.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I work 60 hours a week and I never see my friends or family. Where does my time go?" | Should fire | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 2 | "I feel completely out of balance. Work eats everything and I've stopped exercising." | Should fire | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 3 | "Help me say no to my boss when he messages me at 10pm. I want my evenings back." | Should fire | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 4 | "I'm a new parent going back to work in March. How do I fit in sleep, my partner and my job?" | Should fire | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 5 | "Plan my week: I have a launch on Thursday and three client calls." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 6 | "I want to start running every morning but I keep skipping it." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 7 | "Slack pings constantly and I can't get any real work done." | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 8 | "Which productivity method should I use? I'm always behind." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 9 | "Set up my whole productivity system: inbox, tasks, weekly review." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 10 | "Plan my day: dentist at 2, report due, school pickup at 4." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 11 | "I have too much on my list, help me prioritise it." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 12 | "Help me focus for the next hour on my essay." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 13 | "How does time blocking work, and is it worth it?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 14 | "I have to get this proposal out by Friday and only have two days." | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 15 | "I'm stuck on the thesis and can't get started." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 16 | "Our weekly sync is useless, how do I fix it?" | Near miss | none (meeting-design, sibling repo) | **meeting-audit** | meeting-design | meeting-design |
| 17 | "What should I do first on the wedding planning?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 18 | "I'm too busy to see my friends and I feel like I do nothing but work, and I'm so low I can't sleep." | Ambiguous, boundary | balance-my-life, with the one-time referral and a practical-only offer | balance-my-life | balance-my-life | balance-my-life |
| 19 | "I want more time for my kids, so how should I organise my week?" | Ambiguous | balance-my-life or plan-my-week | balance-my-life | balance-my-life | balance-my-life |
| 20 | "I'm drowning, I need a system for work and home." | Ambiguous | balance-my-life or build-my-system | build-my-system | build-my-system | build-my-system |

---

## What each case tests

**1 to 4, should fire.** Literal and paraphrased triggers across a long-hours professional, a person with no exercise, a boss boundary and a life transition. Case 4 tests that personal and professional both count.

**5, plan-my-week.** Names tasks and a launch. The user wants outcomes placed on a week, not a check of life areas.

**6, build-a-habit.** One behaviour to start. Balance mentions health only as one area, so the word "exercise" is the risk.

**7, protect-my-focus.** Work interruptions. "Can't get real work done" has no other life area in it.

**8, find-my-method.** "Always behind" with a request for a method. No life areas involved.

**9, build-my-system.** The whole organising structure, not the time split across life.

**10, plan-my-day and 11, sort-my-tasks and 12, start-a-focus-session and 13, explain-a-method.** Single-day, list, one-hour and method-lookup requests. None asks about the balance across life.

**14 to 17, fit-to-deadline, get-unstuck, meeting-design and plan-the-work.** Existing neighbours. Case 16 is outside this repository and expects no skill.

**18, boundary.** Balance request with low mood and poor sleep. Check by reading the output: one kind, brief referral to a professional, no diagnosis, no repeat, practical part only if the user wants it.

**19, ambiguous.** Time for kids as a week-planning request or a balance one. Decide in writing after a run whether a split is acceptable.

**20, ambiguous.** "Work and home" overlaps the Life part of build-my-system. Either is defensible; balance-my-life should win if the question is about time across areas, build-my-system if about tools and routines.

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| balance-my-life#16 | "Our weekly sync is useless, how do I fix it?" | none (meeting-design, sibling repo) | **meeting-audit** | meeting-design | meeting-design | Haiku chose meeting-audit for a weekly-sync complaint; meeting-design is intended. Overlap among the three meeting skills. |
