---
name: build-my-system
description: >
  Trigger on "set up my productivity system", "organise my life", "make me hyper-productive", "I need a system", "I use five apps and still drop things", "where should my tasks and notes live", "build me a workflow", "I keep starting new systems", "create my my-system.md". Designs the smallest complete system in whatever the user already has (paper, phone notes, calendar, task app, spreadsheet): one inbox, a home for tasks and projects, a daily and weekly plan, a weekly review, focus rules and a place for personal commitments. Audits an existing setup and keeps what works. Caps new methods at three. Produces the filled my-system.md profile, a rhythm table with minutes and a day 1 to 7 setup checklist. Not for picking one method to trial, which is find-my-method, planning today, which is plan-my-day, or this week, which is plan-my-week.
---

# Build My System

A system is a few places and a few habits that stop things being dropped. The usual failure is building too much of it.

The failure this exists to prevent: **building an elaborate system that takes longer to maintain than the work it organises.**

The target is the smallest complete system: six parts, each as small as it can be, in tools the user already owns.

---

## What this needs

**Minimum: the user saying what they do, what they use now and what keeps going wrong.** "Nurse on rotating shifts, notes app and a wall calendar, I forget follow-ups" is enough. Design the whole system from that and label every guess.

**Better with** their fixed constraints (shifts, caregiving, a commute), when they have energy for hard work, and whether the current setup is a list of what they actually use.

**Best with** an existing `my-system.md` pasted in, which turns this into an audit and update.

Never require buying anything. Claude cannot see the user's calendar or tools and does not remember between conversations unless their tool provides memory, so the user saves the output and pastes it later. If the method library from `find-my-method` is not available, use the cheat-sheet in `references/system-parts.md`. Nothing here is a prerequisite.

---

## When this runs

Runs when the user wants the whole structure: where things are captured, where they live, how the day and week are planned, and how it is kept up.

**Does not run for:**

- Choosing and trialling one method such as Pomodoro or time blocking. That is `find-my-method`; how a named method works is `explain-a-method`.
- Planning today. That is `plan-my-day`. Planning this week is `plan-my-week`.
- Ranking an overloaded list. That is `sort-my-tasks`.
- Interruptions and meetings. That is `protect-my-focus`.
- One habit. That is `build-a-habit`. Where time goes across life is `balance-my-life`.

---

## Step 1: Draft first, ask later

Read what the user gave. Write a first design straight away, labelling guesses. Ask at most three questions afterwards, each naming the line it would change. If nothing at all is known ("make me productive"), ask one: "What do you do most days, and what do you use now to keep track?"

## Step 2: Audit before building

If the user already runs a system, list what is there in a table: tool or habit, what it is for, used or not. Use these verdicts: **keep**, **merge** (two things doing one job), **drop**, **gap** (a part with nothing). Prefer keeping. Replacing a working system with a better-looking one is the most common way this goes wrong. If it is working, the answer may be "change nothing but the weekly review".

## Step 3: Find the one friction

Name the single biggest friction (things dropped, no time for what matters, overwhelm, too many places, starting late, no end to the day). The design is judged on that. Everything else is secondary.

## Step 4: Design the six parts

Keep each to a sentence or two. Use the user's own tools; options by tool are in `references/system-parts.md`.

1. **Capture:** one inbox. A single place everything goes first, whatever its size. Name it concretely ("the Notes app, note called Inbox").
2. **Organise:** where tasks and projects live. One list of next actions and one short list of projects, no more folders than the user can name.
3. **Plan:** a daily plan (pick up to three must-dos) and a weekly plan (a few outcomes placed on the calendar).
4. **Review:** a weekly review at minimum. Empty the inbox, check the calendar and the lists, pick next week's outcomes.
5. **Focus:** two or three rules (phone away during a work block, notifications off, one thing at a time). Only rules the user can keep.
6. **Life:** a named place for personal commitments, held to the same standard as work: appointments, family events, health, one anchor a week.

## Step 5: Pick methods deliberately, cap at three

Choose by name from the cheat-sheet or from the library if present. State for each: what it does here, and the evidence label. Cap **new** methods at three to start; methods the user already uses do not count. Say which were deliberately left out, and "not yet" is a reason. Be honest: most are practice only, little direct testing. Do not claim a percentage or a fixed time to results.

## Step 6: Build the rhythm table

Give daily, weekly and monthly routines with minutes. Add them up. The whole upkeep must fit the budget the user states, or default to about 15 minutes a day, 45 to 60 a week, 20 a month. If it does not fit, cut methods, not minutes. Show the total, and tell the user: if it takes longer than the work it organises, delete a part.

## Step 7: Write my-system.md and the day 1 to 7 checklist

Fill the profile from `assets/my-system.md` exactly in schema, keeping its headings. Mark guessed fields "(assumed)". Every method starts with status "trying". Then fill the checklist from `assets/setup-checklist.md`: one small job a day, none over 30 minutes, with a day-7 review and a rule for what to drop.

Say plainly: **save this file and paste it into future chats.** Claude does not remember between conversations unless the user's tool provides memory. Other skills can read it if pasted.

## Step 8: Offer next steps by name, once

One or two, matched to the friction: `find-my-method` to test a method properly, `plan-my-day` or `plan-my-week` to use the system now, `build-a-habit` for one behaviour that keeps slipping, `balance-my-life` if the Life part is thin. If a named skill is not installed, say what the step would be in a sentence and carry on.

---

## Output

In this order, as plain text the user can save:

1. One-line summary: the friction and the design in a sentence
2. Audit table (only if a system exists)
3. The six parts
4. Methods chosen (max three new), and what was left out
5. Rhythm table with minutes and total
6. The filled `my-system.md`
7. Day 1 to 7 checklist
8. Save-and-paste reminder, next step, What I had to assume

Layouts in `assets/my-system.md` and `assets/setup-checklist.md`.

---

## Failure modes

**Too much.** Seven folders, four apps, a colour code. Cut to one inbox, one list, one calendar.

**Replacing a working system.** Audit first. Keep what the user actually uses.

**Buying something.** Never recommend a purchase as a first step. Name free options on the tool they have.

**More than three new methods.** Park the rest as "later".

**A rhythm that does not add up.** Show the minutes and the total; cut when over budget.

**Ignoring constraints.** A 6am routine for someone on night shifts. Build around fixed hours.

**Work only.** The Life part must name something real, not just a heading.

**Promising results.** No claim of hours saved or a number of days to stick. It is a trial; day 7 decides.

**No save instruction.** Without it the profile is lost at the end of the chat.

**Inventing facts.** Tools, hours and energy are guessed and labelled (assumed).

A finished system means a design was chosen on purpose. It does not mean it will fit; the day-7 review is where that is found out.

---

## Supporting files

- `assets/my-system.md` - the profile template with fill-in prompts, in the exact schema
- `assets/setup-checklist.md` - the day 1 to 7 checklist
- `references/system-parts.md` - the six parts by tool, and a short cheat-sheet of methods with evidence labels

## What I had to assume

End every reply with this section, never empty. List each guessed tool, hour, constraint and energy pattern, with the line it would change if wrong. Include anything that could not be checked: the user's calendar, how reliably they used past systems, shared systems with a team or family.
