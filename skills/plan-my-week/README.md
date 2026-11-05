# plan my week

**Never plan a week as a longer to-do list.**

A weekly plan is usually last week's unfinished items plus this week's new ones. No one decided which three matter, and no hour is protected, so by Wednesday the calendar belongs to other people.

This skill runs a short review first: wins, slips, and every carry-over given a verdict (carry, delegate or drop, with no silent rollovers). It then picks at most three outcomes for the week, places them as protected focus blocks on an ideal-week skeleton, offers theme days only if your work allows holding them, names the one risk to the plan with an if-then, and adds one personal item so the week is not all work. You type what happened and what is coming; it does the rest.

The failure this exists to prevent: **a week that is a longer to-do list, with no outcomes and no protected time.**

**Reach for it:** Sunday evening, Monday at 8:55, or Friday at 4pm. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The person and school are invented. Output varies.*

You type: `Plan my week. I'm Tomas, a secondary maths teacher at Hollis Park School. Last week: marked the Year 9 tests, but didn't write the Year 11 revision pack or call the Okafor parents. This week: parents' evening Thursday 16:00 to 19:30, a Year 11 mock Friday, 5 lessons a day, sharpest early.`

You get (shortened):

```
Last week
  Wins: Year 9 tests marked; returned on time.
  Slips: revision pack (too big, guess); Okafor call (avoided, guess).
  Carry-overs: revision pack - CARRY, becomes outcome 1.
               Okafor call - CARRY, Monday 15:45, 10 minutes (second carry:
               do it or hand it to the head of year).
               Photocopying audit - DROP, nobody has asked since September.

Outcomes
  1. Year 11 revision pack printed and in pigeonholes by Thursday 15:00
  2. Parents' evening notes ready for the 12 families on your list, by Wed
  (Two outcomes. A teaching week is reactive; a third would be a wish.)

Skeleton (excerpt)
  Mon  07:30-08:30 FOCUS-1 pack, part A | 15:45 Okafor call
  Tue  07:30-08:30 FOCUS-1 pack, part B
  Wed  07:30-08:15 FOCUS-2 parents' evening notes | 15:45-16:30 SLACK
  Thu  07:30-08:00 print pack | 16:00-19:30 Parents' evening
  Fri  Mock | 15:30 CLOSE: next week's list
  Fri  19:00 PERSONAL: climbing wall with Jo

Themes: none. Lessons and pastoral calls arrive on their own schedule.
Risk: if the department photocopier is down on Wednesday morning, print
the pack at the library on the way in Thursday.
```

---

## What it actually does

| Section | What you get |
| :--- | :--- |
| Last week | Wins, slips with a guessed reason, and a verdict on every carry-over |
| Outcomes | Three at most, each a result you could point to on Friday |
| Skeleton | Days by blocks: fixed items, named focus blocks tied to outcomes, message windows, slack, close-out and planning slots |
| Themes | Offered only if your work lets you hold them; half-days or none otherwise |
| Not this week | Every cut item with a landing date or a drop |
| The one risk | One if-then, with a cue you will actually notice |
| One personal item | A real block with a day and time |
| What I had to assume | Every guess |

---

## Who this is for

Anyone who plans a week: students, nurses, founders, teachers, engineers, parents, freelancers, shift workers. The theme-day step asks whether your work allows it and says no when it does not. No calendar or tool is needed; typed lines are enough.

---

## What this needs

**Minimum:** a few lines on last week and what is coming.

**Better with:** fixed commitments, last week's plan, and when you think best.

**Best with:** a pasted `my-system.md` if you have one. Read it for peak hours, constraints and your chosen methods.

Nothing is a prerequisite. Claude cannot see your calendar, keep time or remember next week, so you put the blocks in your calendar and keep the plan.

---

## Where it hands off

- One day of the week: `plan-my-day`
- A list too long to plan from: `sort-my-tasks`
- The shape of your whole life: `balance-my-life`
- Setting up the tools and the review habit: `build-my-system`
- Stress-testing the plan: `what-could-go-wrong`
- A full retrospective on a finished piece of work: `lessons-learned`
- A deadline that does not fit: `fit-to-deadline`

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the plan-my-week skill from https://github.com/theAnirudhKumar/work-design: copy its skills/plan-my-week folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/plan-my-week` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `assets/week-plan.md` is the template, and `references/methods-cheatsheet.md` holds the methods it uses with notes on when each backfires.

---

## Where this comes from

The review, outcomes, ideal-week and protected-block ideas are widely used and little tested directly; `references/methods-cheatsheet.md` gives an honest evidence label for each. The risk line is an if-then plan, which has repeated support for helping people follow through when the cue is specific. The two-thirds planning rule is a rule of thumb. No figure for time saved is claimed.

---

## What this does not do

- **Not a calendar.** You place the blocks.
- **Not a life audit.** It adds one personal item; `balance-my-life` looks at the whole.
- **Not a day plan.** `plan-my-day` takes one day from the skeleton.
- **Not a retrospective.** The review is three short lists.
- **Not a promise that the week will hold.** It makes the plan honest, not the week predictable.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
