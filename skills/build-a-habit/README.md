# build a habit

**Design one habit small enough to survive a bad week, instead of five big ones that die by Thursday.**

Most habit advice is a speech about discipline. This skill designs. It takes the habit you want and writes a one-page Habit Plan: the tiny version you can do on your worst day, an anchor in if-then wording ("After I pour my coffee, I will..."), a change to your environment so the cue is obvious and the start is easy, one thing to track, a miss rule (return without guilt, never miss twice), a day-14 review, and a rule for when to scale up.

It starts one habit at a time and tells you why. It does not claim a habit takes 21 or 66 days, because formation time varies widely between people and habits. It is not medical advice: for sleep, eating, exercise or substance changes tied to a health condition, it points you to a clinician for that part.

The failure this exists to prevent: **starting five ambitious habits at once on Monday and abandoning all of them by Thursday.**

**Reach for it:** when you want to start something daily, or you keep quitting something. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Examples

*Illustrative. The people are invented, and the exact output varies with what you give it.*

**A teacher who wants to read every night.** You type: `I want to read for an hour every night. I've tried and quit three times.`

You get (shortened):

```
Habit: read before sleep. Tiny version: one page, in bed.
Anchor: After I plug my phone in across the room, I read one page.
Environment: book on the pillow; phone charger in the hall.
Track: a tick on the wall calendar.
Miss rule: if I miss, one page the next night. Never twice.
Day-14 review: [date]. Scale-up: two pages once one feels easy, never
because I feel inspired.
Assumed: your phone currently charges by the bed; you do not work nights.
```

**A founder starting five things on Monday.** You type: `From Monday: gym daily, no sugar, meditate, 5am wake, journal.` You get a short, non-scolding explanation of why one at a time, a recommendation for which to start with (often the one the others depend on), the other four parked in order, and a plan for the first.

**A nurse on rotating shifts.** You get an anchor tied to getting home, not to a clock time, and a tiny version that fits a 12-hour shift. A note on sleep gets one line suggesting a clinician for any real sleep problem.

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Pin the behaviour | An outcome turned into something you can do and see |
| One at a time | Which habit starts first, and the others parked |
| The Habit Plan | Tiny version, anchor, environment, tracking, miss rule |
| Review | A day-14 check on whether the plan fits you |
| Scale-up | A rule for growing it on ease, not on a good mood |
| Boundary | A clinician for health-linked parts, said once |

---

## Who this is for

Anyone starting or restarting a regular behaviour: students, shift workers, parents, founders, writers, engineers. It works for habits to start (reading, stretching, a work review) and, with friction and a replacement, habits to do less of.

---

## What this needs

**Minimum:** the habit, in a sentence.

**Better with:** your usual day, and what happened the last time you tried.

**Best with:** a `my-system.md` profile, if you have one, for existing routines.

Missing context never blocks this skill. It marks what it assumed. Claude cannot remember across chats or send reminders, so the tracking is yours and you bring the log to the day-14 review.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the build-a-habit skill from https://github.com/theAnirudhKumar/work-design: copy its skills/build-a-habit folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/build-a-habit` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/habit-methods.md` lists the methods with evidence labels and when each backfires, and `assets/habit-plan.md` is a plan you can fill in alone.

---

## Where this comes from

Starting small is associated with BJ Fogg's Tiny Habits. If-then planning comes from research by Peter Gollwitzer. Temptation bundling is associated with Katy Milkman. "Never miss twice" is a popular rule of thumb with no single origin. A well-known real-world study found habit formation time varies widely, which is why the skill states no fixed number of days. Evidence labels are in the reference file: most of this is Practice only or Some.

---

## What this does not do

- **Not medical advice.** Sleep, eating, exercise with a condition, and substance changes go to a clinician for that part.
- **Not a planner.** `plan-my-day` and `plan-my-week` place a habit in a schedule.
- **Not a whole system.** `build-my-system` designs that.
- **Not a motivation speech.** It designs the plan and names the failure points.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
