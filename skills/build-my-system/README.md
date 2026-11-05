# build my system

**Build the smallest complete system out of tools you already have, and write it down in one file.**

Most systems fail by growing. Five apps, a colour code and a nightly ritual take longer to keep up than the work they organise, and get abandoned. Then comes the next system.

This skill designs six small parts: one inbox to capture into, a home for tasks and projects, a daily and weekly plan, a weekly review, a few focus rules, and a place for personal commitments so life is held to the same standard as work. It works on paper, phone notes, a calendar, a task app or a spreadsheet, and never needs you to buy anything. If you already run a system, it audits first: keep, merge, drop or gap. It names each method it picks, caps new ones at three, and labels the evidence honestly (most are practice only, little direct testing).

You get a filled `my-system.md` profile, a rhythm table with minutes that has to add up, and a day 1 to 7 setup checklist with a day-7 review rule.

The failure this exists to prevent: **building an elaborate system that takes longer to maintain than the work it organises.**

**Reach for it:** when you are starting over, or when things keep falling through. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. Output varies with what you give it. The person is invented.*

You type: `I teach full time and have a toddler. I keep forgetting marking and school forms. I use a paper planner and my phone notes. Set me up.`

You get (shortened):

```
Friction: things you promise in passing never reach the planner.
Keep: paper planner for the timetable. Merge: three phone notes into one.

Capture: one phone note called Inbox. Organise: a "Next actions" page at the
back of the planner. Plan: three must-dos written each morning (3 min).
Review: Friday 3:45, 20 minutes. Focus: phone in the bag during marking.
Life: planner page "Home", one protected evening.

New methods (3 max): single inbox, weekly review, Most Important Tasks.
Not yet: time blocking (your days are interrupted).

Rhythm: daily 8 min, weekly 20 min, monthly 15 min.

my-system.md is written below. Save it, and paste it into future chats:
Claude does not remember between conversations.
```

Templates: [`assets/my-system.md`](assets/my-system.md) and [`assets/setup-checklist.md`](assets/setup-checklist.md).

---

## What it does not do

- **Not a method trial.** Testing one method for a week is `find-my-method`.
- **Not a day or week plan.** Those are `plan-my-day` and `plan-my-week`.
- **Not a habit builder.** One slipping behaviour is `build-a-habit`.
- **Not a promise.** It makes no claim about hours saved. The day-7 review decides what stays.

---

## What this needs

**Minimum:** what you do, what you use now and what keeps going wrong.

**Better with:** fixed constraints and when you do your best thinking.

**Best with:** an existing `my-system.md`, which makes it an audit and update.

Claude cannot see your calendar or tools and does not remember between conversations unless your tool provides memory. Save the file and paste it back. Nothing is a prerequisite.

---

## Install

As a plugin in Claude Code or Cowork:

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the build-my-system skill from https://github.com/theAnirudhKumar/work-design: copy its skills/build-my-system folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/build-my-system` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill.

**Or just read it.** `SKILL.md` is the method, `assets/` has the profile and checklist, `references/system-parts.md` is the cheat-sheet.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
