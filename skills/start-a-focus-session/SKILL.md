---
name: start-a-focus-session
description: >
  Trigger on "help me focus for an hour", "start a Pomodoro", "set me up for a focus session", "I need to concentrate on this", "Pomodoro or 90 minutes", "I keep sitting down and not working", "focus block", or a user returning with "done", "I got interrupted" or "didn't finish" after a session. Picks a format (Pomodoro 25/5, 52/17, 90-minute block, flowtime, plain one-hour block) by task and energy, writes a Focus Card (one task, what done looks like for this session, first action, parking lot, phone away, break plan), tells the user to set the timer because Claude cannot keep time, then runs a 60-second debrief on return. Not for choosing what to do today (plan-my-day), ranking a long list (sort-my-tasks), a stalled task (get-unstuck) or recurring interruptions (protect-my-focus).
---

# Start A Focus Session

Turns "I should get some work done" into one defined block: a single task, a visible end, and the phone out of reach. When the user comes back, it runs a short debrief and sets up the next block or a stop.

The failure this exists to prevent: **sitting down to "work" with no defined task, no end, and the phone in reach, so the hour disappears into switching and nothing is finished.**

---

## What this needs

**Minimum: the task, in the user's words, and roughly how long they have.** "Write the intro to my essay, about an hour" is enough. No files, no calendar, no timer app, no other skill.

**Better with** how their energy is right now, where they are working (home, open office, library, ward station) and what usually pulls them away.

**Best with** a `my-system.md` profile pasted in, if they have one, so the format matches the methods and peak hours they already chose. Without it, work from their words and say what was assumed.

**Claude cannot keep time.** It cannot start a clock, notice the block has ended or message the user later. The user sets the timer. Say this once, plainly, in the Focus Card step, and never apologise for it or repeat it.

---

## When this runs

Runs when the user is about to work on something and wants a structured block, names a format ("Pomodoro", "90 minutes"), or returns from a block with a status.

**Does not run for:**

- Deciding what the day should contain. `plan-my-day` handles that, and may hand one block to this skill.
- Ranking a long list. `sort-my-tasks` handles that.
- A task that has stalled for a reason the user cannot name. `get-unstuck` diagnoses first. If the user says they cannot start, use Step 5 below, and hand off if the cause is not about starting mechanics.
- Interruptions that happen every day, from people or systems. `protect-my-focus` handles the pattern; this skill handles one block.
- Choosing or comparing productivity methods in general. `find-my-method` and `explain-a-method` do that.

---

## Step 1: Take the task and constrain the questions

Read what the user gave. Ask at most two questions, only for what changes the format:

1. What is the one task, and what would "done for this session" look like?
2. How much time do you have, and how is your energy (fresh, ok, flat)?

If the task is a project ("work on the thesis"), do not ask for a plan. Pick a slice that fits one block and propose it: "Draft section 2.1 only." Let the user correct it. If the user gave enough, ask nothing.

## Step 2: Pick the format

Use the table in `references/formats.md`. The decision runs on three inputs: task type (shallow admin, analytical, creative/open-ended), energy, and time available. Name the format, give the one reason it fits, and name the runner-up in one clause. Default when unsure: a plain one-hour block or 25/5, whichever the user is closer to; both are easy to adjust.

Do not present the format list as a menu to choose from. Choose, then let the user override.

## Step 3: Write the Focus Card

Fill `assets/focus-card.md` in chat. Every line is specific to this session:

- **The one task.** One, in verb + object form. Move anything else to the parking lot.
- **Done for this session.** Observable, and smaller than the whole project: "section 2.1 has a complete first draft, roughly 600 words, rough is fine".
- **First action.** The literal first thing to do in the first two minutes, small enough to start without thinking: "Open the file and write the heading and the first topic sentence."
- **Parking lot.** A place to write stray thoughts and tasks (paper next to the keyboard is best) without acting on them. Pre-load it with anything the user mentioned that is nagging them. Tell them to review it only at the break or after.
- **Phone and notifications.** Phone in another room or a bag, or at minimum face down and on Do Not Disturb with notifications off. If the user needs to be reachable (child's school, on-call, a family member who is ill), name the one exception: which callers can get through, and nothing else. Never tell someone who must be reachable to switch everything off.
- **Timer.** State once: "I cannot keep time or tell you when the block ends. Set a timer now, before you start: [length]." Suggest a timer that is not the phone: a kitchen timer, a watch, or a computer clock. If it must be the phone, set it before putting the phone face down or out of reach.
- **Break plan.** What the break is for and what it is not: stand, water, look at something far away, a short walk. Not social media or email, which restart the pull. For the long break, a real stop.
- **If interrupted.** One line: jot the stopping point on the parking lot, handle the interruption, and restart the same block or tell me "got interrupted".

Close the card with: "Start the timer, do the first action, and come back and tell me done, interrupted or didn't finish."

## Step 4: Handle the situation the user is in

Apply only what fits.

**Shared workspace or open office.** The card gets one extra line: a signal to others (headphones on, a sign, a status message with a return time) and a fallback location (a meeting room, a quiet corner, a library). If the interruptions are a daily pattern, say that this is the point to run `protect-my-focus`, and keep going with this block.

**Creative or open-ended work (writing, design, composing, research thinking).** Timers can break a flow state that has just started. Recommend a longer block (90 minutes) or flowtime with a soft check at about the 60-minute mark, and set the done-condition as an output ("a rough draft of the opening, however ugly") rather than a time. Say honestly that the evidence for any format on creative work is thin and the user's own experience is the test.

**Care and on-call work (nursing, support, parenting at home).** Fixed-length blocks will be broken. Use short blocks (15 to 25 minutes), name the exception callers, and make the stopping-point note part of the card so resuming costs seconds. Do not suggest hiding.

**Student, exam revision.** Same card, with the task as a question set or a past paper section, and the break plan as a real rest, not a social feed.

## Step 5: Difficulty starting

If the user says they sit down and cannot begin, or have trouble starting even when they want to, offer strategies, framed as things to try, not as a reading of the user. Do not diagnose, name a condition or suggest the user has one, even if they offer a label themselves. Options, pick one or two:

- **Shrink the first step** until it is nearly silly: open the document, write one sentence, put the tool on the desk. Shrink the block too: 10 minutes, with permission to stop after.
- **Body doubling.** Work alongside another person, in the same room, a library, or on a video call with the camera on and a one-line "I'm working on X for 25 minutes" said aloud. Some people find that the presence of someone else makes starting easier. Claude can be the person who hears the Focus Card, but it is not present while the user works.
- **Shorter blocks** with a visible finish line (15 minutes, then reassess).
- **Start with the easiest piece**, not the most important, then move.
- **Make the start physical**: same chair, same playlist or a particular mug, as a cue.

If starting trouble extends beyond work into daily life, or the user mentions that it is affecting health or sleep, say once, kindly, that a professional who knows this area could help, and continue with the practical part if they want it.

## Step 6: The debrief

When the user returns, run it in under a minute of reading. Ask for or read the status, then answer four things in a compact block:

1. **What got done**, against the done-for-this-session line: done, partly, or not started. Name it without judgement.
2. **What pulled attention.** Outside (a message, a person, noise) or inside (a stray thought, boredom, "I should check..."). Check the parking lot: was it used? Count nothing; just name the top one or two.
3. **Adjust the next block.** One change only: a shorter or longer block, a different time of day, a different location, a smaller task, the phone moved. Match the change to what pulled attention.
4. **Next move.** Offer either another block (write the next card in two lines, same format unless changed) or a stop. A stop is a legitimate answer: if energy is gone, say so, note the breadcrumb for the next session (the exact next action, written down) and end.

Handle the three statuses:

- **"Done."** Confirm, note what worked, offer a break and the next block.
- **"Got interrupted."** No blame. Write the stopping point as the breadcrumb, decide: resume now with a fresh short block, or reschedule. If the interruptions are a pattern, mention `protect-my-focus` once.
- **"Didn't finish."** Ask whether the done-sentence was too big. If so, cut it; the next card's done-line is the remainder. If the task was fine and attention drifted, apply item 3. Do not turn it into a lecture about discipline.

If this is a new chat, the card is gone: ask the user to paste it or restate the task and done-line, and proceed.

---

## Output

For the start of a session, in order:

1. **Format** and one-line reason.
2. **The Focus Card**, filled in (see `assets/focus-card.md`).
3. **The timer line**, once.
4. **What I had to assume**, one or two lines.

For a debrief:

1. **Status line** (done, partly, not started).
2. **What pulled attention.**
3. **One adjustment** for the next block.
4. **Next block card (two lines) or a stop**, with the breadcrumb.
5. **What I had to assume**, if anything changed.

---

## Failure modes

**More than one task on the card.** The most common failure. If the user lists three, pick one and park the others by name. A card with a "main task and a couple of small things" is an unfocused hour.

**A done-line that is the whole project.** "Finish the report" is not a session. Cut to the slice.

**Pretending to keep time.** Never say "I'll let you know when 25 minutes are up" or "check back in half an hour and I'll remind you". Say the timer is theirs.

**Prescribing the same format for everyone.** 25 minutes suits some tasks and cuts others in half. Choose by task and energy and say why.

**Treating a break as optional or as a scroll.** The break plan is part of the card.

**Telling people to hide.** For anyone who must stay reachable, design the exception instead.

**Diagnosing.** Starting difficulty is handled with strategies. No labels.

**A debrief that turns into planning the week.** Keep it to four items and one adjustment.

**Overselling the format.** None of these formats is proven better than the others; say what the user's own results will show after a few blocks.

---

## What I had to assume

Close every output with a short list: the length of the time available if not stated, the energy level if not asked, where they are working, whether they can really be unreachable, and anything about the task (size, difficulty) that was guessed.

---

## Supporting files

- `references/formats.md` - the five formats with when to use each, when each backfires, and how to choose.
- `assets/focus-card.md` - the pre-session card and the debrief block, usable without the skill.
