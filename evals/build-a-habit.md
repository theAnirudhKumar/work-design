# Evaluation: build-a-habit

Routing cases for `build-a-habit`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 41. All three models matched on 40; Haiku 41, Sonnet 40, Opus 41.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The set must include the skills built alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `balance-my-life`, `build-my-system`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`) and, for the meeting cases, `meeting-audit` from the sibling meeting-design repository, or the near misses are not meaningful. `meeting-design` is the set that contains `meeting-audit`. An Expected value written as A or B means either routing is defensible.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I want to start exercising every day. I've failed at this about ten times." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 2 | "I can't stick to journaling. I do it for three days and then stop." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 3 | "Help me build a habit of reading before bed." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 4 | "From Monday I'm doing gym daily, no sugar, meditation, 5am wake-ups and journaling." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 5 | "How long does it take to form a habit? 21 days, right?" | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 6 | "I want to start running but I have asthma and a heart murmur. Make me a plan." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 7 | "I want to fix my sleep. Give me a schedule, I have insomnia." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 8 | "I'm a night-shift nurse. How do I build a stretching habit when my schedule changes every week?" | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 9 | "I want to cut down on scrolling my phone in the evening." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 10 | "I want to make a daily shutdown routine at the end of my workday and stick to it." | Should fire | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 11 | "Help me focus for an hour on my taxes." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 12 | "Start a Pomodoro for me." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 13 | "I'm interrupted all day and can't concentrate. What do I do?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 14 | "Slack and meetings are eating my focus. How do I ask my manager for time?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 15 | "Plan my day. Include the gym and a call at 3." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 16 | "Plan my week. I want to work out three times and finish the launch." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 17 | "I've got too many tasks. Sort them out." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 18 | "I can't start my thesis and I've been putting it off for weeks." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 19 | "I neglect my friends and my health because I work too much." | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 20 | "What productivity method fits me? I've tried many." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 21 | "Explain how habit stacking works and whether it's worth trying." | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 22 | "Set up my whole system: tasks, calendar, notes, daily and weekly review." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 23 | "Which tasks should I hand to an AI agent?" | Near miss | delegate | delegate | delegate | delegate |
| 24 | "The report is due Friday and I only have two days. Cut it down." | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 25 | "What is in scope for this project and what is not?" | Near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 26 | "I have to write a business plan. Where do I begin?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 27 | "How long will it take to learn Spanish to a conversational level?" | Near miss | how-long-will-it-take | how-long-will-it-take | **none** | how-long-will-it-take |
| 28 | "Should we have a meeting or send an email about the habit tracker rollout?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 29 | "Our weekly all-hands is a waste of time. Fix it." | Near miss | meeting-audit (meeting-design set) | meeting-audit | meeting-design | meeting-design |
| 30 | "What could go wrong with my plan to wake up at 5am?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 31 | "Review my habit plan and tell me if it's any good." | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 32 | "That experiment is over. What did I learn about my morning routine?" | Near miss | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 33 | "Save the context of this chat so I can pick it up later." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 34 | "Cut my token spend on this chat." | Near miss | cut-token-cost | cut-token-cost | cut-token-cost | cut-token-cost |
| 35 | "Audit my subscriptions, I'm paying for three habit-tracking apps." | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 36 | "Is this habit app safe? Read the privacy policy." | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 37 | "What breaks if I move my habit data from one tracker to another?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 38 | "What can work-design help me with?" | Near miss | work-design | work-design | work-design | work-design |
| 39 | "I want to get fit, lose weight, sleep more and read more this year." | Ambiguous | build-a-habit or balance-my-life | build-a-habit | build-a-habit | build-a-habit |
| 40 | "I want to stop working late. Help me make it a routine." | Ambiguous | build-a-habit or balance-my-life | build-a-habit | build-a-habit | build-a-habit |
| 41 | "I want to focus better, it's a habit I need to build." | Ambiguous | build-a-habit or start-a-focus-session or protect-my-focus | build-a-habit | build-a-habit | build-a-habit |

---

## What each case tests

**1, should fire.** The core trigger with prior failure. Expects a tiny version, an anchor and a miss rule. Exercise is also health-adjacent; with no condition mentioned, no clinician referral is needed beyond a one-line note.

**2, should fire.** 'Can't stick to' trigger. Expects diagnosis of why it stopped (size, cue, break) in the plan.

**3, should fire.** Literal 'build a habit'. Expects the Habit Plan.

**4, should fire.** The failure the skill names. Expects a short explanation of why one at a time, a recommendation of which one, and the others parked.

**5, should fire.** Tests the hard rule. The output must not give 21 or 66 days or any fixed number; it should say formation time varies widely.

**6, should fire.** Health condition. Expects the behaviour side (tiny version, anchor) with a clear one-time referral to a clinician for the exercise load, and no training prescription.

**7, should fire.** Sleep tied to a condition. The output must say a clinician is the right person for the insomnia part, and offer only the behaviour-design side if wanted.

**8, should fire.** Variable schedule. Expects an event anchor, not a clock-time anchor.

**9, should fire.** A habit to do less of. Expects a replacement at the cue and friction in the environment.

**10, should fire.** A work habit. Overlaps with plan-my-day's shutdown line; the request is to make a routine stick, so it fits here.

**11, near miss.** A single session.

**12, near miss.** A named format.

**13, near miss.** A workplace interruption pattern.

**14, near miss.** A negotiation, with a message. Not about personal behaviour.

**15, near miss.** Placing items in one day. The gym is a given.

**16, near miss.** Weekly planning. Exercise is an item, not a habit design.

**17, near miss.** A list to prioritise.

**18, near miss.** A single stalled piece of work, not a recurring behaviour. 'Putting it off' is the overlap risk.

**19, near miss.** Life-area imbalance and boundary scripts. If this leads to 'start a weekly call with friends', a hand-off to build-a-habit is reasonable.

**20, near miss.** Method selection.

**21, near miss.** A question about a method. Habit stacking is used inside build-a-habit, but the user wants an explanation.

**22, near miss.** Full system design.

**23, near miss.** Allocation.

**24, near miss.** Scope against time.

**25, near miss.** Boundaries.

**26, near miss.** Framing a task.

**27, near miss.** An estimate request. This invites a fixed-duration answer, which build-a-habit would refuse for habit formation; here the question is about a skill, and the skill needs a comparable past case, not a habit plan.

**28, near miss.** Channel choice.

**29, near miss.** A meeting problem for the sibling set.

**30, near miss.** Stress-testing a plan. If the user then asks to make it stick, a hand-off is expected.

**31, near miss.** A finished document needs review. Tests that the word 'habit' does not outweigh 'review'.

**32, near miss.** A retro on finished work. The day-14 review inside a Habit Plan is this skill's job; a general retro is not.

**33, near miss.** Chat handoff.

**34, near miss.** Token economy.

**35, near miss.** Spend review. 'Habit' is the overlap risk.

**36, near miss.** Vetting an app.

**37, near miss.** Exit cost of a tool.

**38, near miss.** The menu.

**39, ambiguous.** Many goals. Expected: build-a-habit picks one and parks the rest; balance-my-life is defensible if the user frames it as life areas.

**40, ambiguous.** A boundary habit. Either routing is defensible: balance-my-life writes the boundary script; build-a-habit builds the routine.

**41, ambiguous.** 'Focus' as a habit. Three skills have a claim. A clarifying question about the real friction is the best behaviour.

---

## Output check

Three cases to be checked by hand once a model is available.

**Case 5 (21 days).** The output must not state 21 days, 66 days or any fixed number of days to form a habit. It should say formation time varies widely and that the day-14 review checks whether the plan fits, not whether the habit is built.

**Case 4 (five habits).** The output should explain in two or three sentences, without scolding, why one at a time, recommend one, and park the others in order. It should not build all five plans. If the user insists in the next turn, it should build at most two and say which drops first.

**Cases 6 and 7 (health).** The output should say once that a clinician is the right person for the medical part (exercise with a cardiac or respiratory condition; insomnia), give no training load, schedule or treatment, and continue only with behaviour design if the user wants it.


---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| build-a-habit#27 | "How long will it take to learn Spanish to a conversational level?" | how-long-will-it-take | how-long-will-it-take | **none** | how-long-will-it-take | Sonnet answered none for "how long to learn Spanish"; how-long-will-it-take is intended. Borderline. |
