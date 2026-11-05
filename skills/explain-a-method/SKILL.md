---
name: explain-a-method
description: >
  Trigger on "how does time blocking work", "what is the Eisenhower matrix", "explain Pomodoro", "is Getting Things Done worth it", "does the Ivy Lee method actually work", "X vs Y", "Pomodoro vs time blocking", "walk me through the 1-3-5 rule", "what is that productivity thing where". Looks up the method, then gives what it is, a 10-minute start, a worked example, an honest evidence label, when it backfires, and a try-it-today step. Compares two methods in a small table with a pick-by-situation line. Says so when a method is not recognised instead of inventing one. Not for choosing a method from scratch, "what should I use" or "nothing works", which is find-my-method, and not for running today's plan, which is plan-my-day.
---

# Explain A Method

Productivity content explains methods with confidence and leaves out when they fail, and sometimes explains methods that do not exist.

The failure this exists to prevent: **confident explanations of methods that omit when they fail, or invented methods.**

Give a short, usable explanation of one method, or a side-by-side of two, with an honest evidence label and a step the user can take today.

---

## What this needs

**Minimum: the name of a method.** "Explain time blocking" is enough. No files, tools, connectors or sibling skills.

**Better with** the user's field and situation, so the example fits them.

**Best with** the method library from `find-my-method` (`references/method-index.md` and the category cards), if the user has it pasted or installed. A library card supplies the evidence label, "Skip it when" and the 10-minute start. Without it, work from general knowledge and mark the evidence label "general knowledge, not checked against a card".

Claude cannot keep time or remember across sessions. Where a method needs a timer, tell the user to set one.

---

## When this runs

Runs when the user names a method and asks how it works, what it is, whether it is worth it, to be walked through it, or to compare two.

**Does not run for:**

- "What should I use", "I want to get more done", "nothing works". That is `find-my-method`.
- Building a full system. That is `build-my-system`.
- Running a focus session now. That is `start-a-focus-session`.
- Planning today or this week. Those are `plan-my-day` and `plan-my-week`.
- Ranking a pasted list. That is `sort-my-tasks`.
- Designing one habit. That is `build-a-habit`.

If the user names one method and wants it walked through, stay here. If they ask which to pick for themselves, hand to `find-my-method`.

---

## Step 1: Identify the method

Find it in the library if present, otherwise in general knowledge.

- **Recognised, in the library:** use the card.
- **Recognised, not in the library:** explain from general knowledge and flag it.
- **Not recognised, or not a real method:** say so plainly: "I do not recognise that as an established method." Offer the closest real one, or ask where they heard it. Do not make up steps, an originator or a name.
- **Same method, several names or variants:** name the variants once, explain the common core.
- **Disputed origin:** "often attributed to X; the attribution is disputed".

## Step 2: Write the explanation in six parts

Use `assets/method-explainer.md`. Keep it to roughly one screen.

1. **What it is.** Two sentences, plain words, no hype.
2. **Start in 10 minutes.** Three to five numbered steps doable now.
3. **A worked example.** From a field the user mentioned, otherwise a sensible default such as a teacher, freelancer or student. Invented people, labelled illustrative.
4. **Evidence.** Exactly one of Strong, Some, Mixed, Practice only, plus one honest sentence. When unsure, choose Practice only. Cite no study by author or year and give no percentage or "boosts productivity by N%".
5. **When it backfires.** At least two concrete situations. This part is not optional.
6. **Try it today.** One action, under 15 minutes, with a stopping point.

Health-adjacent methods (sleep, naps, exercise, eye rest) are general wellbeing practice, not medical advice. Say to follow a professional's advice for any condition.

## Step 3: Comparisons

For "X vs Y": a table with rows for what it is for, effort to set up, works best when, backfires when, and evidence. Then one line picking by situation: "If you control your calendar, X. If you are interrupted all day, Y." Do not declare a winner without a situation. Then offer `find-my-method` once if they want a pick for themselves.

## Step 4: Answer "is it worth it" honestly

Say who it is worth it for and who it is not, and what the evidence label means in a sentence. "Practice only" is not an insult: it means widely used and little tested. Do not hedge into nothing; give a view tied to their situation if they described one.

## Step 5: Close with What I had to assume

One line each: the field, the version of the method used, whether the library was available. Offer the single next step: `find-my-method` for a recommendation, or `plan-my-day` to use it today.

---

## Output

The six parts from `assets/method-explainer.md` for one method, or the comparison table plus pick-by-situation line for two, then What I had to assume. No preamble.

---

## Failure modes

**Hype.** "Game-changing." Remove it; state what the method does.

**Leaving out the backfire.** Every method fails somewhere. Say where.

**Inventing a method.** If it is not recognised, say so. A plausible name with plausible steps is the worst outcome.

**Invented evidence.** A study, a founder, a percentage. Use the label and one sentence only.

**Giving a recommendation when asked to explain.** If the user wants a pick, hand to `find-my-method`.

**An example from the wrong world.** Use their field when they gave one.

**Pretending to keep time.** Tell the user to set the timer.

A good explanation lets someone decide not to use the method as well as use it.

---

## Supporting files

- `assets/method-explainer.md` - the template for one method and for a comparison
- The method library lives in `find-my-method`'s `references/`. Not required here.
