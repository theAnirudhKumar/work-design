# Evaluation: find-my-method

Routing cases for `find-my-method`, written alongside the skill.

**Run on:** 5 Nov 2026, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `c4b8a8cfab44`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 20. All three models matched on 18; Haiku 18, Sonnet 18, Opus 18. The protect-my-focus description was reworded after this run; see the targeted rerun in `evals/README.md`.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used. Skills named below that are written concurrently (`explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life`, `build-my-system`) must be present in the description set for the near misses to be meaningful.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "What productivity method should I use? I never seem to finish anything." | Should fire | find-my-method | find-my-method | find-my-method | find-my-method |
| 2 | "I want to get more done in less time, but nothing I've tried sticks." | Should fire | find-my-method | find-my-method | find-my-method | find-my-method |
| 3 | "I'm a night-shift nurse and every system I try falls apart when my rota changes. What would actually suit me?" | Should fire | find-my-method | find-my-method | find-my-method | find-my-method |
| 4 | "Should I use Pomodoro or time blocking? I work from home and get interrupted a lot." | Should fire | find-my-method | find-my-method | find-my-method | find-my-method |
| 5 | "How does time blocking actually work?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 6 | "Plan my day. I have a 10am meeting, a report to write and the school run at 3." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 7 | "Help me plan my week and do a review of last week." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 8 | "Here is my list of 40 things. Which should I do first?" | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 9 | "Help me focus for the next hour. I need to write a chapter." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 10 | "Slack and meetings are killing my day. How do I get my afternoons back?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 11 | "I want to start running every morning but I keep quitting after a week." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 12 | "I neglect my family and friends because of work. Where does my time go?" | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 13 | "Set up my whole productivity system: inbox, calendar, reviews, all of it." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 14 | "I'm stuck on this one proposal and I don't know why." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 15 | "I have to write the Q3 report. Where do I start?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 16 | "I need this done by Friday but I only have two days." | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 17 | "Is this weekly status meeting worth having, or should it be an email?" | Near miss | meeting-or-message | **meeting-audit** | **meeting-audit** | **meeting-audit** |
| 18 | "Which of these tasks should I give to an AI?" | Near miss | delegate | delegate | delegate | delegate |
| 19 | "I'm exhausted all the time and nothing helps. What system should I use?" | Ambiguous | find-my-method | find-my-method | find-my-method | find-my-method |
| 20 | "I'm always distracted. What should I do?" | Ambiguous | find-my-method | **protect-my-focus** | **protect-my-focus** | **protect-my-focus** |

---

## Notes on the cases

**1 to 4, should fire.** All ask for a recommendation. Case 4 names two methods but asks which to use, so it is a recommendation, not an explanation.

**5, explain-a-method.** One named method, "how does it work". The overlap is the word "method".

**6 and 7, plan-my-day and plan-my-week.** A concrete day or week to plan. No question about which method.

**8, sort-my-tasks.** A pasted list to rank. No friction diagnosis.

**9, start-a-focus-session.** A session starting now.

**10, protect-my-focus.** The named friction is interruption by others. `find-my-method` lists this as a friction but defers the full audit.

**11, build-a-habit.** One habit. "I keep quitting" is close to "nothing sticks" in case 2.

**12, balance-my-life.** Time across life areas, not a method choice.

**13, build-my-system.** A full setup request, not a pick.

**14 to 18, existing neighbours.** Each belongs to a different job: a stalled task, a start, a deadline squeeze, a channel choice, an allocation.

**19, ambiguous.** Exhaustion could go to `balance-my-life`, and the body of the skill says to avoid adding systems to someone who needs rest and to mention a professional once. Either routing is defensible. Decide in writing after a run.

**20, ambiguous.** "Always distracted" could be `find-my-method` (a diagnosis) or `start-a-focus-session` or `protect-my-focus`. The friction guide routes it by cause. A split is probably acceptable.

---

## Output check

One case to be checked by hand once a model is available: case 3. The output should contain a friction read quoting the user, exactly one primary, one backup and one avoid-for-now method, evidence labels from {Strong, Some, Mixed, Practice only}, no study or percentage, at most two changes, a 7-day trial, a scorecard with keep and drop-without-guilt rules, a hand-off line naming `build-my-system` and `plan-my-day`, and What I had to assume. It should not recommend time blocking as primary to someone with no control of their hours.

A second check without the library: every evidence label reads "general knowledge".

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| find-my-method#20 | "I'm always distracted. What should I do?" | find-my-method | **protect-my-focus** | **protect-my-focus** | **protect-my-focus** | Expectation arguably wrong: self-distraction is within protect-my-focus. Kept as a known overlap. |
| find-my-method#17 | "Is this weekly status meeting worth having, or should it be an email?" | meeting-or-message | **meeting-audit** | **meeting-audit** | **meeting-audit** | meeting-audit claims "should we still have this weekly". Acceptable overlap; both lead to a verdict. |
