---
name: find-my-method
description: >
  Trigger on "what productivity method should I use", "which method fits me", "I want to get more done", "nothing works for me", "I've tried everything", "I keep failing at productivity systems", "pomodoro or time blocking for me", "I'm always behind", "how do I get more done in less time". Diagnoses the main friction, then recommends one primary method, one backup and one to avoid for now, each with fit reasons and an honest evidence label, plus a 7-day trial plan with a scorecard. Changes at most two things at once. Asks at most three questions. Not for explaining how one named method works or comparing two, which is explain-a-method, and not for planning today, which is plan-my-day.
---

# Find My Method

There are over a hundred productivity methods and most advice treats them all as equally good for everyone. They are not. A method that suits a person who controls their calendar can be useless to a nurse on shifts.

The failure this exists to prevent: **adopting a popular method that does not fit, failing at it, and concluding the problem is personal.**

Produce a Method Fit Card: one primary method, one backup, one to avoid for now, and a 7-day trial the person can run and judge.

---

## What this needs

**Minimum: one sentence about what is going wrong.** "I never finish anything" is enough. No files, tools, connectors or sibling skills. Draft the whole card from it and label every guess.

**Better with** the kind of work, how much control they have over their time, hard constraints (fixed hours, caregiving, shifts), and what they tried before and why it stopped.

**Best with** the method library in `references/` (`method-index.md` plus the category files). Without it, work from general knowledge and mark every evidence label "general knowledge, not checked against a card".

Claude cannot keep time, remember across sessions or see the calendar. The trial plan tells the user to set their own reminders and keep the scorecard themselves.

---

## When this runs

Runs when the user wants a recommendation: which method, what to try, why nothing has worked.

**Does not run for:**

- "How does time blocking work", "is Pomodoro worth it", "X vs Y". That is `explain-a-method`.
- One named method and a request to be walked through it. That is `explain-a-method`.
- Planning a specific day or week. Those are `plan-my-day` and `plan-my-week`.
- A list that needs ranking. That is `sort-my-tasks`.
- A single stuck task. That is `get-unstuck`.
- A running focus session, interruptions at work, one habit, or life balance. Those are `start-a-focus-session`, `protect-my-focus`, `build-a-habit` and `balance-my-life`. Hand off if the diagnosis points there.
- A full setup. That is `build-my-system`.

---

## Step 1: Read what was given

Pull four things from the user's words, quoting them:

1. **Main friction.** Match to the ten in `references/friction-guide.md`.
2. **Kind of work and control over time.** Own calendar, someone else's, shift-based, on call, student, caregiver.
3. **Hard constraints.** Fixed hours, caregiving, no phone at work, shared devices, no budget.
4. **What was tried and why it failed.** The failure reason matters more than the method name: "I forgot it" and "it felt childish" point to different fixes.

If `my-system.md` is pasted, read it first and do not recommend anything marked "keeping" or "trying" as new.

## Step 2: Ask at most three questions, only if they change the answer

Draft first. Ask only when two candidate primary methods would differ on the answer. Good questions: "Do you choose when you work on things, or does someone else?" and "What did you try last, and what made you stop?" Not worth asking: favourite apps, age, job title when the work type is already clear.

If the message is empty of friction ("help me be productive"), ask one question: "What is the one thing that goes wrong most days?" Then draft.

## Step 3: Choose with three rules

- **Fit before fame.** Pick the method that addresses the friction under the constraints, not the best-known one.
- **Change at most two things at once.** One primary method. If the backup is a second change, label it "instead, not as well". A stack of five new methods is the failure this skill exists to prevent. If the person already tried to adopt several, say that is the likelier cause and start with one.
- **Respect the control gap.** Someone without control of their calendar gets methods that work inside gaps (batching, small blocks, capture), not calendar-heavy ones.

Read `references/method-index.md` to shortlist, then open the relevant category card for the primary and backup so the evidence label, "Skip it when" and "Start in 10 minutes" come from the card. If the library is absent, say so once and mark labels as general knowledge.

## Step 4: Write the three picks

- **Primary:** fit reasons that quote the user ("you said meetings fill your day, and this works in 30-minute gaps"), the evidence label with the card's one sentence, and the card's "Skip it when" checked against their situation.
- **Backup:** when to switch to it (a specific failure at day 7), why it differs from the primary.
- **Avoid for now:** one popular method that is likely to fail for them, with the reason tied to their constraint. "For now", never "never". Pick something they actually mentioned or are likely to reach for.

Never write a method name that is not in the library or not a recognised method. Never cite a study or a percentage. Evidence labels are exactly: Strong, Some, Mixed, Practice only.

## Step 5: Write the 7-day trial and the scorecard

Use `assets/method-fit-card.md` and `assets/trial-scorecard.md`.

- **Day 1 setup** in under 10 minutes, taken from the card.
- **Days 2 to 6:** one daily action, no additions.
- **Day 7:** a five-minute review of the scorecard.
- **Track one or two things only.** Examples: days the method was used, and one outcome that matters to them.
- **Keep it** if it was used on at least five of seven days and the outcome they named moved, or it felt lighter. **Drop it without guilt** if it was used fewer than three days for reasons the method caused, or it made the day worse. Between those, adjust one thing and run three more days.
- Tell the user to set the reminders and save the scorecard themselves, since Claude cannot.

## Step 6: Offer the hand-offs, once

One line: `build-my-system` for a full setup, and `plan-my-day` to apply the primary method to today. If the diagnosis is mainly a single-friction skill (interruptions, one habit, life balance), name that skill instead as the first hand-off. If a named skill is not installed, say what the step would be in a sentence.

## Step 7: Close with What I had to assume

Every guess, one line each, with the card line it changes if wrong.

If the user describes severe distress, exhaustion that does not lift, or health problems rather than a workflow problem, say once, kindly, that a professional who can help is worth talking to, and give the practical part only if they want it. Never diagnose.

---

## Output

The Method Fit Card from `assets/method-fit-card.md`, in plain text the user can paste, in this order: friction read, primary, backup, avoid for now, 7-day trial, scorecard, hand-offs, what I had to assume. Then up to three questions, each naming the line it would change. No preamble.

---

## Failure modes

**Recommending a stack.** Three methods "that work together". Pick one; mention a pairing only as a day-8 option.

**The famous method by default.** Pomodoro for everyone. Check the "Skip it when" line against the person.

**Invented evidence.** A study, a percentage, a founder's name. Use the card's label and sentence, or "Practice only" when unsure.

**Blaming the person.** If past methods failed, name the mismatch (control, constraints, setup cost) rather than discipline.

**Interviewing first.** Draft, then ask.

**A trial with no exit.** Always state what counts as dropping it without guilt.

**Pretending to remember or keep time.** Say what the user must do themselves.

A card means a considered guess, not a diagnosis. The 7-day trial is how the guess gets tested.

---

## Supporting files

- `references/method-index.md` - one row per method; read first
- `references/methods-*.md` - the cards, one file per category (time, prioritize, organize, focus, start, habits, decide, goals, energy, review, learn, team, life)
- `references/friction-guide.md` - the ten commonest frictions and the methods that address each
- `assets/method-fit-card.md` - the output template
- `assets/trial-scorecard.md` - the 7-day scorecard
