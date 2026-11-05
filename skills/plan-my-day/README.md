# plan my day

**Never plan a day as if it were empty.**

Most day plans are written for a day with nothing else in it. The meetings, the ten minutes each call overruns, the walk between rooms and the messages that land at 9:40 are missing, so by 11am the plan is wrong and gets abandoned.

This skill builds the plan from the real day. It takes a task dump, the fixed commitments, the hours available and, if known, when you think best and which method you use. It does the capacity sum in view, tells you plainly when the list is more than fits, and cuts instead of squeezing. The result is a Day Plan: one to three must-dos (the day is a success if only these happen), a time-blocked schedule with a buffer after each meeting and unscheduled slack, hard work in your peak time, shallow tasks batched, a not-today list with a landing place for each item, a slip rule and a one-line shutdown.

The failure this exists to prevent: **a plan that assumes an empty day, lists more than fits, and collapses by 11am.**

**Reach for it:** at 8:55 with a head full of tasks, or at 1pm when the morning went sideways. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The person and company are invented. Output varies.*

You type: `Plan my day. I'm Dana, a freelance designer at Larkfield Studio. 9 to 5:30. Client call 11:00 to 12:00, dentist 15:30 to 16:30. I'm sharpest before noon. I need to: finish the Orchard Row logo concepts, invoice two clients, reply to 20-odd emails, update my portfolio, book flights, research a new font library, review Sam's mockups.`

You get (shortened):

```
Capacity
  Available 9:00 to 17:30 = 8.5h. Taken: call 1h, dentist 1h + 30 min travel,
  lunch 45 min, buffer after the call 15 min = 3.5h. Left: 5h.
  Plannable: about two thirds = 3.3h. The rest is slack (rule of thumb).
  Your list adds up to about 8h. Roughly half of it is not happening today.

Must-dos
  1. Orchard Row: three logo concepts as a PDF to the client by 14:30
     (if it slips: the Thursday review slips)
  2. Invoice the two clients (20 min)

Schedule
  09:00-10:45  Peak: Orchard Row concepts
  10:45-11:00  Slack
  11:00-12:00  Client call
  12:00-12:15  Buffer: notes, next steps
  12:15-13:00  Lunch
  13:00-13:20  Invoices
  13:20-14:00  Batch: email (stop at 14:00)
  14:00-14:30  Orchard Row: export and send
  14:30-15:00  Slack
  15:00-16:30  Dentist (travel included)
  16:30-17:15  Review Sam's mockups, only if all above is done
  17:15        Shutdown

Slip rule: if you are behind by 14:00, drop Sam's mockups, then email.
Not today: portfolio (Friday), flights (Saturday morning), font research (drop).
Shutdown: 17:15, write tomorrow's first action on this sheet and close up.
```

---

## What it actually does

| Section | What you get |
| :--- | :--- |
| Capacity | Hours available, minus fixed items and buffers, about two thirds plannable. A rule of thumb, not a measured fact |
| Must-dos | One to three results. If only these happen, the day worked |
| Schedule | Fixed items first, a buffer after each meeting, hard work in peak time, shallow tasks batched, slack named as slack |
| Slip rule | What to drop, in order, if you are behind at a stated time |
| Not today | Every cut item with a place to land, so nothing rolls over silently |
| Shutdown | One sentence with a time |
| What I had to assume | Every guess, including no calendar given |

---

## Special days

- **No calendar given.** Blocks are marked floating and re-pinned once you give the fixed times.
- **Shift workers.** The day runs from waking to sleep, not nine to five. Sleep is a fixed commitment.
- **Caregivers and anyone interrupted.** Interruptible blocks of 15 to 25 minutes, each with a safe stopping point and a pick-up note, and about half the day left as slack.
- **A bad day.** A minimum viable day: three small wins and the commitments that cannot move.

---

## Who this is for

Anyone with more to do than a day holds: students, nurses between ward rounds, founders, teachers, engineers, parents, freelancers, shift workers. If you use Ivy Lee, 1-3-5, day theming or Pomodoro, say so and the plan takes that shape.

---

## What this needs

**Minimum:** what you have on for today, typed or pasted.

**Better with:** fixed commitments with times, the hours available, and when you think best.

**Best with:** your method, rough time per task, and a pasted `my-system.md` if you have one.

Nothing is a prerequisite. Claude cannot see your calendar, keep time or remember tomorrow, so you paste the calendar, set your own alarms and save the plan.

---

## Where it hands off

- A list too long to plan from: `sort-my-tasks`
- A whole week: `plan-my-week`
- One focus hour: `start-a-focus-session`
- One big piece of work with no plan: `plan-the-work`
- Too much for a deadline: `fit-to-deadline`
- Interruptions as the main problem: `protect-my-focus`
- An item you cannot start: `get-unstuck`

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the plan-my-day skill from https://github.com/theAnirudhKumar/work-design: copy its skills/plan-my-day folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/plan-my-day` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `assets/day-plan.md` is the template, and `references/methods-cheatsheet.md` holds the methods it uses with notes on when each backfires.

---

## Where this comes from

The default is most-important tasks plus time blocking, both widely used and little tested directly; the evidence labels in `references/methods-cheatsheet.md` say so for each method. The buffer and slack rule rests on the well-documented tendency to underestimate how long tasks take. The proportion (about two thirds plannable) is a rule of thumb, and the skill says so. No figure for how much time any of this saves is claimed.

---

## What this does not do

- **Not a calendar.** It writes the plan; you put it where you will see it.
- **Not a ranking of a long list.** `sort-my-tasks` does that.
- **Not a week plan.** `plan-my-week` does that.
- **Not a clock.** Claude cannot keep time. Set the alarms.
- **Not therapy or medical advice.** A bad-day plan is about work, and sleep or health matters belong with a professional.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
