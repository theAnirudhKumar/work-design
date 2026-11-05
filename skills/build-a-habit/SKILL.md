---
name: build-a-habit
description: >
  Trigger on "I want to start doing X every day", "I can't stick to Y", "help me build a habit", "I keep quitting my routine", "how do I make this stick", "I want to read, stretch, journal or study daily", "I started five new habits on Monday". Designs a one-page Habit Plan: the tiny version for the worst day, an anchor in if-then wording, an environment change, what to track, a miss rule, a day-14 review and a scale-up rule. Starts one habit at a time and says why. Never claims a habit takes 21 or 66 days. Not medical advice; suggests a clinician for sleep, eating, exercise or substance changes tied to a health condition. Not for planning a day (plan-my-day) or week (plan-my-week), a one-off stalled task (get-unstuck), life-area balance (balance-my-life) or a whole system (build-my-system).
---

# Build A Habit

Designs one habit so small and well-anchored that it survives a bad week. It produces a Habit Plan, not a lecture about motivation.

The failure this exists to prevent: **starting five ambitious habits at once on Monday and abandoning all of them by Thursday.**

---

## What this needs

**Minimum: the habit the user wants, in a sentence.** "I want to stretch every morning" is enough. No app, no tracker, no other skill.

**Better with** their usual day (when they wake, eat, commute, finish work), what has been tried before, and what happened to it.

**Best with** a `my-system.md` profile, if they have one, for existing routines and constraints. Without it, work from their words and say what was assumed.

Claude cannot remember across chats, send reminders or check whether the user did the habit. The plan puts the cue in the user's day and the tracking on paper or an app they already use. For the day-14 review, the user comes back and pastes their log.

---

## When this runs

Runs when the user wants to start, restart or make stick a recurring behaviour: exercise, reading, language practice, journaling, a work routine like a daily review, meditation, tidying.

**Does not run for:**

- Planning a particular day or week. `plan-my-day` and `plan-my-week` handle those; a habit can appear in them as a recurring item.
- A one-time task that has stalled. `get-unstuck` handles that.
- A general sense of imbalance across life areas. `balance-my-life` handles that.
- Designing the user's whole productivity system. `build-my-system` handles that; it can call for a habit and hand it here.
- A single focus block today. `start-a-focus-session` handles that.
- Medical, mental health or addiction treatment. See the boundary in Step 6.

---

## Step 1: Take the habit and pin it to a behaviour

Read what the user said. The habit must be a **behaviour they can do and observe**, not an outcome. "Get fit" is an outcome; "put on trainers and walk for ten minutes" is a behaviour. "Be more organised" becomes "write tomorrow's top three before closing the laptop." Propose the behaviour version and let the user correct it.

Ask at most three questions, only if the answers change the plan:

1. What is the habit, and why does it matter to you? (One sentence. The reason is for the day-14 review.)
2. What does an ordinary weekday look like, from waking up to bed, roughly?
3. What did you try before, and what ended it?

If the user gave this already, ask nothing.

## Step 2: One habit at a time

If the user names several habits, or has just started or restarted several, do not build all of them. Say why in two or three sentences, without scolding:

> Each new habit needs setup time, attention and a cue in your day, and those are limited. When several start together, one slipped day tends to feel like the whole project failing, and you cannot tell which one is working. One habit gives you a clear signal and a base to add to.

Then ask which one to start with, and recommend one: the one that is smallest, most anchored in the day already, or most supportive of the others (sleep schedule before exercise schedule, if that is the pattern). Park the rest on a "later" list with a rough order. Name that the list is where they wait, not where they die.

If the user insists on more than one, build them, with these rules: start at most two, keep both tiny, give each its own anchor, and tell them which one gets dropped first if the week goes badly. Do not refuse.

## Step 3: Design the Habit Plan

Fill `assets/habit-plan.md`. Each part is specific:

1. **The tiny version.** The version small enough to do on the worst day (ill, exhausted, travelling, in a crisis at work), taking under two minutes. "One page of the book", "put on the trainers and step outside", "write one line in the journal", "open the language app and complete one exercise". It is the habit's floor, not a warm-up. Doing the tiny version counts as doing the habit.
2. **The anchor.** An existing, reliable routine to attach the habit to, written as an if-then: **"After I [existing routine], I will [tiny version]."** Check the anchor is specific, happens daily or on the planned days, and is in the same place and rough time. "After I pour my morning coffee" works. "When I have a moment" does not. If the user has no stable routine (shift work, new baby, travel), anchor to something that does recur, such as arriving at work, finishing a meal, getting into bed, or the first time they sit down.
3. **The environment change.** Make the cue obvious and the start easy: book on the pillow, mat unrolled in view, shoes by the door, language app on the home screen, tracker on the desk. Remove one source of friction, and where the habit is something to do less of, add friction to the cue (the app logged out, the snack out of sight). One or two changes, no more.
4. **What to track, and how.** One simple mark per day: a tick on a paper calendar, a note in an app they already use. Track "did the tiny version", not performance. Say that tracking is a record, and that a visible streak can motivate some people and backfire for others; if it makes a miss feel catastrophic, switch to counting days done this week.
5. **The miss rule.** Write it: "If I miss a day, I do the tiny version the next day, no catching up and no guilt. I never miss twice." The idea of never missing twice is widely repeated; treat it as a useful rule of thumb, not a law. Plan for the usual breaks before they happen: illness, travel, a bad week. A miss is data about the plan (cue, size, timing), not about the person.
6. **The day-14 review.** A date, and four questions: Did I do it, roughly how often? What got in the way? Is the anchor right? Is the tiny version too small, too big or right? Decide: keep as is, adjust the cue or the size, or drop. The user brings their log back to Claude, or runs the questions alone.
7. **The scale-up rule.** Only grow the habit when the tiny version is automatic and easy, not when motivation is high. Grow one notch at a time (one page to two pages, five minutes to ten), keep the tiny version as the fallback for bad days, and drop back a notch for a week if it starts to slip. A habit is not "formed" at a date; see below.

## Step 4: Be honest about time

**Never say a habit takes 21 days, 66 days or any fixed number of days.** Research on habit formation in real life found wide variation between people and between habits. Say: "How long it takes to feel automatic varies a lot, from a few weeks to many months, depending on you and on the habit. Do not judge it on a fixed date. The day-14 review checks whether the plan fits, not whether you have 'built' the habit."

Do not promise results. Say what the plan does: reduces the effort of starting, attaches the habit to something that already happens, and makes a miss recoverable.

## Step 5: Common situations

- **"I tried this before and quit."** Ask what ended it (usually size, timing or a break with no way back). Fix that specific cause in the plan.
- **No spare time.** Shrink further or bundle with an existing activity (stretch while the kettle boils, listen to the language lesson while commuting). Do not tell people to wake up earlier unless they want to.
- **Habits to do less of** (phone, snacking, doomscrolling). Design the replacement and the friction: what to do instead at the cue, and what to make harder. Be gentle; do not moralise.
- **Work habits** (daily shutdown, weekly review, a writing session). Anchor to the end of the working day or the first coffee; keep the tiny version real ("write the three top tasks for tomorrow").
- **Shift workers and caregivers.** Anchor to events (getting home, after the first meal, putting the child down), not clock times.
- **Habit stacking too many.** Remind of Step 2, once.

## Step 6: The boundary

This is a behaviour-design skill, not medical advice. For anything that touches a health condition or a risk, say once, plainly, that a clinician is the right person for that part, and continue with the behaviour side if the user wants:

- **Sleep** (insomnia, sleep apnoea symptoms), **eating** (restriction, bingeing, disordered patterns, diets for a condition), **exercise** with an injury, pregnancy, heart or other conditions, **alcohol, tobacco or other substances** where stopping could be unsafe or the user is dependent.
- Mood problems that look like more than a missing routine.

Do not prescribe a diet, dose, training load, or schedule for a medical condition. Do not diagnose. Do not repeat the suggestion after saying it once.

---

## Output

The Habit Plan, in this order:

1. **The habit, as a behaviour**, and the reason in the user's words.
2. **One habit or two:** which one, and what is parked.
3. **Tiny version, anchor (if-then), environment change, tracking, miss rule.**
4. **Day-14 review:** the date and the four questions.
5. **Scale-up rule.**
6. **Boundary line,** only if a health part is involved.
7. **What I had to assume**

Offer `assets/habit-plan.md` as the one-page version to keep.

---

## Failure modes

**A big habit with a big first step.** "Run 5k daily" on Monday is the failure this prevents. The tiny version must be doable on the worst day.

**An anchor that is a feeling or a time.** "When I feel motivated" and "at 7am" break the first bad morning. Use an event that happens anyway.

**Five habits at once.** Say why they should not and build one. If they insist, build at most two and name which drops first.

**Quoting 21 or 66 days.** Neither is a rule. Never state a fixed number.

**Lecturing.** No motivation speeches or willpower talk. Design the plan.

**Guilt in the miss rule.** The rule is "return without guilt". A miss is data about the plan.

**Tracking more than one thing.** One mark a day.

**Medical advice by the back door.** A workout plan for a heart condition, a diet for diabetes, an alcohol cut-down for a dependent drinker: refer that part to a clinician.

**Scaling on a high.** Growing the habit after a good week and then losing the habit after a bad one. Scale on ease, not on mood.

---

## What I had to assume

Close with a short list: the user's daily routine if not described, whether the anchor actually happens every day, how much time they truly have, what happened last time, and whether any health condition is involved.

---

## Supporting files

- `references/habit-methods.md` - the methods the plan uses, with evidence labels and when each backfires.
- `assets/habit-plan.md` - the one-page Habit Plan the user keeps.
