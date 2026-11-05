# Evaluation: balance-my-life

Routing cases for `balance-my-life`, written alongside the skill. **No results are recorded.** The Haiku, Sonnet and Opus columns read "not yet run" because these cases have not been put to any model. Only the expected routing is filled in, and it is a prediction from reading the descriptions, not a finding.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used. Skills named below that are not in the repository must be present in the description set. Near misses name skills that are being added alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`); their descriptions must be in the set.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I work 60 hours a week and I never see my friends or family. Where does my time go?" | Should fire | balance-my-life | not yet run | not yet run | not yet run |
| 2 | "I feel completely out of balance. Work eats everything and I've stopped exercising." | Should fire | balance-my-life | not yet run | not yet run | not yet run |
| 3 | "Help me say no to my boss when he messages me at 10pm. I want my evenings back." | Should fire | balance-my-life | not yet run | not yet run | not yet run |
| 4 | "I'm a new parent going back to work in March. How do I fit in sleep, my partner and my job?" | Should fire | balance-my-life | not yet run | not yet run | not yet run |
| 5 | "Plan my week: I have a launch on Thursday and three client calls." | Near miss | plan-my-week | not yet run | not yet run | not yet run |
| 6 | "I want to start running every morning but I keep skipping it." | Near miss | build-a-habit | not yet run | not yet run | not yet run |
| 7 | "Slack pings constantly and I can't get any real work done." | Near miss | protect-my-focus | not yet run | not yet run | not yet run |
| 8 | "Which productivity method should I use? I'm always behind." | Near miss | find-my-method | not yet run | not yet run | not yet run |
| 9 | "Set up my whole productivity system: inbox, tasks, weekly review." | Near miss | build-my-system | not yet run | not yet run | not yet run |
| 10 | "Plan my day: dentist at 2, report due, school pickup at 4." | Near miss | plan-my-day | not yet run | not yet run | not yet run |
| 11 | "I have too much on my list, help me prioritise it." | Near miss | sort-my-tasks | not yet run | not yet run | not yet run |
| 12 | "Help me focus for the next hour on my essay." | Near miss | start-a-focus-session | not yet run | not yet run | not yet run |
| 13 | "How does time blocking work, and is it worth it?" | Near miss | explain-a-method | not yet run | not yet run | not yet run |
| 14 | "I have to get this proposal out by Friday and only have two days." | Near miss | fit-to-deadline | not yet run | not yet run | not yet run |
| 15 | "I'm stuck on the thesis and can't get started." | Near miss | get-unstuck | not yet run | not yet run | not yet run |
| 16 | "Our weekly sync is useless, how do I fix it?" | Near miss | none (meeting-design, sibling repo) | not yet run | not yet run | not yet run |
| 17 | "What should I do first on the wedding planning?" | Near miss | plan-the-work | not yet run | not yet run | not yet run |
| 18 | "I'm too busy to see my friends and I feel like I do nothing but work, and I'm so low I can't sleep." | Ambiguous, boundary | balance-my-life, with the one-time referral and a practical-only offer | not yet run | not yet run | not yet run |
| 19 | "I want more time for my kids, so how should I organise my week?" | Ambiguous | balance-my-life or plan-my-week | not yet run | not yet run | not yet run |
| 20 | "I'm drowning, I need a system for work and home." | Ambiguous | balance-my-life or build-my-system | not yet run | not yet run | not yet run |

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
