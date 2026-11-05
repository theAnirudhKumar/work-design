---
name: plan-my-day
description: >
  "plan my day", "what should I do today", "I have 6 hours and 14 things", "time block my day", "build my schedule around my meetings", "I'm behind already, reset my day", "I'm having a bad day, what's the minimum". Turns a task dump, today's fixed commitments and the hours available into a Day Plan: 1 to 3 must-dos, a time-blocked schedule with buffers and slack, hard work in peak time, shallow tasks batched, a not-today list and a one-line shutdown. Uses the user's chosen method (Ivy Lee, 1-3-5, day theming, Pomodoro) if known, and cuts what does not fit. Not for a whole week (plan-my-week), ranking a long list (sort-my-tasks), running one focus hour (start-a-focus-session) or framing one piece of work (plan-the-work).
---

# Plan My Day

A day plan usually fails the same way: it is written for an empty day. The meetings, the walk to the next room, the ten minutes that every call runs over and the messages that arrive at 9:40 are not in it, so by 11am it is already wrong and the person stops trusting it.

The failure this exists to prevent: **a plan that assumes an empty day, lists more than fits, and collapses by 11am.**

Build the plan from the real day: fixed commitments first, honest capacity second, a short list of things that must happen third, everything else cut on purpose.

---

## What this needs

**Minimum: a list of what is on the person's mind for today, typed or pasted.** No calendar, no hours, no tool. Without hours or fixed times, assume an ordinary working day, say so in "What I had to assume", and build blocks that can slide.

**Better with** fixed commitments (calendar pasted or typed: meetings, school pick-up, a shift, appointments), the hours actually available, and when the person thinks best.

**Best with** the method they already use (Ivy Lee, 1-3-5, day theming, Pomodoro and so on), their rough time per task, and a pasted `my-system.md` if they have one. Read its peak focus hours, hard constraints and the methods marked trying or keeping. Ignore methods marked dropped. If there is no such file, do not ask for it.

Claude cannot see a calendar, keep time or remember tomorrow. Say it once where it matters: the person pastes or types the calendar, sets their own alarms, and saves the plan somewhere they will see it.

---

## When this runs

Runs when the person wants a plan for one day (usually today, sometimes tomorrow), including a reset partway through a day that has gone wrong.

**Does not run for:**

- A week. `plan-my-week` handles that, and this skill is what it hands each day to.
- A list that is too long or too tangled to plan from, where the real question is what matters most. `sort-my-tasks` ranks and cuts it first.
- One hour of focus: `start-a-focus-session` sets up and debriefs the hour.
- One large piece of work with no plan: `plan-the-work` writes the Work Card. Here that work appears as a block.
- Too much work for a deadline, not just for a day: `fit-to-deadline`.
- Constant interruptions as the main problem: `protect-my-focus`.

---

## Step 1: Read what was given

Pull out: the task dump, fixed commitments with times, hours available, peak time, the method, and any hard constraint (a shift, children, a commute, a sleep window). Do not ask yet. Use `references/methods-cheatsheet.md` for the methods named below.

If the dump is longer than about 15 items and nothing is ranked, plan from the 15 most time-sensitive and tell the person that `sort-my-tasks` would rank the rest.

## Step 2: Ask at most two questions, only if the answer changes the plan

Likely ones: "What is fixed today (times that cannot move)?" and "When are you sharpest?" Ask both in one message. Never ask about anything that can be assumed and labelled. If the person says "just do it", build the plan on stated assumptions.

If no calendar was given, do not invent one. Build the plan on the open day, mark every block "floating", and ask for the fixed times after the plan so the blocks can be re-pinned.

## Step 3: Do the capacity sum, in view

Write the arithmetic in three lines, so the person can see why things are cut:

1. **Hours available**: start to finish of the working window.
2. **Minus fixed commitments**, **minus a buffer after each meeting** (10 to 15 minutes to write up, move and breathe), minus meals and travel.
3. **Plannable time**: plan only about two thirds of what is left and keep the rest as unscheduled slack. This is a rule of thumb, not a measured fact. Raise the slack to about half on a day with children, unpredictable shifts or a lot of inbound requests; lower it for a day with no one else in it.

Estimate each task. Use the person's figure if given; otherwise guess and label it. People tend to underestimate how long tasks take, so round up and do not stack tasks back to back.

**If the dump is more than fits, say so in one line with the numbers**: "You have about 3.5 plannable hours and the list adds up to about 7. Half of it is not happening today." Then cut. Do not squeeze everything in by shrinking every estimate. Cutting is the plan.

## Step 4: Choose the must-dos

Pick **1 to 3** items. The day counts as a success if only these happen. Each must pass one test: if it does not happen today, something specific gets worse (a deadline passes, someone is blocked, a bigger piece of work slips). "It would be nice" fails the test. Write each as a result with a stopping point, not a topic: "Send the draft budget to Hana" beats "budget".

If three things all qualify and only two fit the plannable time, keep two. A fourth must-do is a sign the cut has not been made.

## Step 5: Apply the person's method, or the default

The default is **most-important tasks plus time blocking**: the must-dos are the day's anchors, then each gets a block with a start time and a stopping point.

If the person uses another method, build the plan in its shape:

- **Ivy Lee**: list the six items in rank order and work them one at a time, no skipping ahead. Unfinished items roll to tomorrow's list. Still mark the top one to three as the must-dos.
- **1-3-5**: one big, three medium, five small. Check the nine fit the plannable time. If not, drop to 1-2-3 and say so.
- **Day theming**: if today has a theme, only theme-fitting work enters the plan. Everything else goes to the not-today list with a place to land.
- **Pomodoro** or another timer format: count rounds, not hours, and tell the person to set their own timer; Claude cannot keep time.
- **Anything else** (GTD-style lists, time boxing, flowtime): use its vocabulary and keep the same output sections.

If the method is one Claude does not know well, say what was assumed about it.

## Step 6: Place the work on the day

Order of placement, always:

1. **Fixed commitments** go in first, as they are.
2. **A buffer after each meeting**, as a named block, not as hopeful empty space.
3. **Hard work in the peak window**: the must-do that needs thinking goes where the person thinks best. If the peak time is unknown, assume the first free stretch of the morning and label it. Most days hold two or three blocks of real concentration at most; plan fewer on a day heavy with meetings.
4. **Shallow tasks batched**: messages, admin, small calls and forms go into one or two named windows, not scattered. Name the window's size and what happens when it ends.
5. **Unscheduled slack** as one or two named blocks the person can see. These absorb the overrun. Name them "slack", not "free time".
6. **Meals and a real break** where the day needs them.

Every block gets a start and end time, or a duration if the day is floating, and one sentence on what finished looks like.

Add a **slip rule**: "If you are more than 30 minutes behind at [checkpoint time], drop in this order: [lowest-value item first]." The person sets an alarm for the checkpoint. This is what stops a late morning from taking the whole day.

## Step 7: Cut to a not-today list

Everything that did not make the plan goes on a not-today list, and each item gets a landing place: a named day, "this week", a person who should have it (see `delegate` for work an AI could take), or "drop". An item with no landing place is a silent rollover and is not allowed. If the list is long, the person can run `sort-my-tasks` on it.

## Step 8: Write the shutdown line

One sentence the person can follow when the day ends, with a time: "At 17:15: write tomorrow's first action on this sheet, move the rest to the list, close the laptop." Make it specific to the day, for example naming the one thing left half-done and the exact point to resume.

---

## Special cases

### No calendar

Say: "I can't see your calendar. Paste or type today's fixed times and I will re-pin the blocks." Until then every block is marked floating and the plan is built on an ordinary working day. Never imply the day was checked.

### Shift workers and irregular hours

Do not assume a 9-to-5. Define the person's "day" as wake to sleep, not midnight to midnight. Treat the sleep window as a fixed commitment. Place the must-do in the stretch where they are most alert after waking, and say the assumption. After a night shift or before an early start, the plan is smaller: one must-do, the fixed commitments, and sleep protected. Do not give medical or sleep advice beyond that.

### Caregivers and anyone interrupted

Build **interruptible blocks**: units of 15 to 25 minutes, each ending at a point where stopping loses nothing, with one line to write at each stop ("pick up at paragraph 3"). Cut the must-do into pieces that can each finish alone. If a protected window exists (school hours, a partner on duty, a nap), put the hard work in it and say which window was assumed; do not invent one. Raise the slack to about half. A day that gets one must-do done between interruptions has worked.

### Bad-day mode: the minimum viable day

Triggers: "bad day", "barely slept", "low energy", "can't think", "everything's on fire", "I'm already behind". Do not build a block schedule. Give:

1. Fixed commitments that really cannot move, and one line on which can be shortened or moved.
2. **Three small wins**, each finishable in about 20 minutes or less, picked so that doing all three means tomorrow is easier. At least one is about the next hard thing (open the file, send the one message), not the whole of it.
3. Everything else to the not-today list with a landing place.
4. A permission line: "If you do only the first win, the day still counts."

Boundary: this is a work-planning skill. If the person describes more than a hard day (not sleeping for days, hopelessness, being unable to function), say once, kindly and without alarm, that a person who can help is worth talking to, then continue with the practical part only if they want it. Do not diagnose or repeat it.

---

## Output

Use `assets/day-plan.md`. In this order, short:

1. **Capacity** in three lines (hours, what is taken, what is plannable) and the cut, if any.
2. **Must-dos** (1 to 3).
3. **The schedule**: a time-blocked table including buffers, batched windows and slack.
4. **Slip rule** with the checkpoint time.
5. **Not today**, each with a landing place.
6. **Shutdown line.**
7. **What I had to assume.**

Keep it to one screen where possible. A plan that needs scrolling will not be read at 2pm.

---

## Failure modes

**Planning the empty day.** Blocks back to back, no buffers, no slack, a 9-to-5 assumed. Run the capacity sum in Step 3 and show it.

**Squeezing instead of cutting.** Every estimate shaved so the list fits. Cut the list and say what was cut.

**Four "must-dos".** If everything is a must-do the label is empty. Three at most, each passing the Step 4 test.

**Hard work in the dead hour.** Deep work after lunch for someone who flags at 2pm. Use the person's peak time, or label the guess.

**Slack hidden as optimism.** "Free time" that is really a task someone forgot to name. Slack is an explicit block with no task.

**Silent rollovers.** Items dropped from the plan with no new home. Every not-today item gets a landing place.

**Pretending to see the calendar or keep time.** Say it cannot, and give the person the alarm, checkpoint and paste instruction.

**Method cosplay.** Naming Ivy Lee or Pomodoro and then producing the default plan. If the method was chosen, the plan must have its shape.

**Motivational filler.** No "you've got this". State the plan.

---

## Supporting files

- `references/methods-cheatsheet.md` - the methods this skill applies, with how each is used here and when it backfires.
- `assets/day-plan.md` - the Day Plan template and the minimum viable day card.
