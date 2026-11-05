---
name: plan-the-work
description: >
  Trigger on "where do I start", "help me get started on", "plan this", "I have to do X", "turn this into a plan", "make a work card", "I'm about to start", "what should I do first on", "break this down", or any non-trivial task described before work begins. Produces a one-page Work Card: outcome, who it is for, why now, appetite, three checkable done criteria, out of scope, biggest risk with an if-then tripwire, who or what helps, a first move under 30 minutes, and labelled assumptions. Drafts immediately and asks at most three questions. Works in any field. Skips tasks under about 30 minutes or already fully specified. Not for drawing a boundary note with a requester, which is scope-the-work, or fitting work into a fixed deadline, which is fit-to-deadline.
---

# Plan The Work

Most work that goes wrong was wrong at the start. The task was a topic, not an outcome. Nobody said who it was for, what finished looks like, or what to leave alone, so the first hours went to whatever was easiest to begin.

The failure this exists to prevent: **starting non-trivial work with no stated outcome, audience or definition of done, so effort goes to the wrong thing and nobody can tell when to stop.**

Turn a task into a one-page Work Card before the work begins. The card is the first page of the work, not a plan for it.

---

## What this needs

**Minimum: the task described in a sentence.** "I have to write the Q3 report" is enough. No files, no connectors, no workspace. Draft the whole card from that and label every guess.

**Better with** the deadline, who the work is for, and any message from the person who asked for it, pasted as written.

**Best with** a past piece of similar work and how it went, so the risk line names a real risk instead of a generic one.

Missing detail never blocks the card. It changes how many lines in "What I had to assume" are filled in.

---

## When this runs

Runs when the user is about to start, or has just been handed, a piece of work that will take more than about 30 minutes and is not yet written down as an outcome.

**Does not run for:**

- A task under about 30 minutes. Say "just start, here is the first move" and give the move. A card costs more than the task.
- A task that is already fully specified: outcome, audience, done condition and deadline are all in the user's message or a brief they pasted. Say what is already covered and offer only the risk and first move.
- A boundary dispute with a person who keeps adding to the request. That is `scope-the-work`.
- A fixed deadline with more work than fits. That is `fit-to-deadline`.
- A question about whether to hand work to an AI. That is `delegate`.

---

## Step 1: Pick the depth

Match the card to the work. Do this silently and state the choice in one line at the top of the card.

| Work size | Card |
| :--- | :--- |
| About 30 minutes or less | No card. Give the first move only. |
| Up to about 2 hours | The 5-line card: Outcome, Done looks like, Out of scope, First move, What I had to assume |
| Half a day to several days | The full card, all ten sections |
| Weeks, or several people | The full card for the whole, then a separate card for the first stretch. Do not write one giant card. |

If the user says how big it is, use that. If not, guess from the task, state the guess, and let them correct it.

## Step 2: Draft first, ask later

Read what the user gave. Write the whole card straight away, filling every section from what is known and marking everything else as an assumption. A card with marked guesses beats an interview, because the user can see a wrong guess and fix it in ten seconds, where a question asks them to do the thinking from nothing.

Ask questions only after the card, at the foot, and:

- **At most three.**
- **Only if the answer would change the card.** "What is your budget?" changes the appetite. "What tools do you use?" usually changes nothing.
- Each question names the card line it would change.

One exception: if the task is so vague that nothing can be drafted ("help me with my project"), ask one question, "What is the thing you are making or changing, in a sentence?", and draft as soon as it is answered.

## Step 3: Write the Outcome

One sentence describing the state of the world when the work succeeds. It must be observable: a stranger could tell whether it happened.

- Weak: "Work on the onboarding emails."
- Strong: "New customers get a three-email onboarding series that is live and sending by the 20th."

An activity verb (work on, look into, think about, explore) means the outcome has not been found yet. Rewrite until the sentence describes a result.

## Step 4: Who it is for and what they will do with it

Name the person or group, and the action they will take using it: decide, sign, run, read before a meeting, build from it, pay. "Stakeholders" and "the team" are not answers. If the work is for the user alone, say so and name what the user will do next with it.

The action matters more than the name. It sets the quality bar: a draft someone will skim can be rough, a document someone will sign cannot.

## Step 5: Why now

One or two lines: what happens if this waits, or what is open now that will close. If the honest answer is "nothing happens if it waits", write that. It is useful: it means the appetite should be small, and it is worth asking whether the work should happen at all.

## Step 6: Set the Appetite

Appetite is the time and effort this work deserves, decided up front. It is a decision about worth, not a prediction of duration. The idea comes from Basecamp's Shape Up (Ryan Singer): fix the time, and let the scope flex to fit, instead of estimating the scope and discovering the time afterwards.

Write it as "Up to [time], because [what the outcome is worth]." Then say what happens at the limit: ship what exists, or stop and reconsider.

- If the user gave a deadline, the appetite cannot exceed the working time before it. State how much working time that is, as an assumption.
- If the appetite looks too small for the outcome, say so in one line and hand off to `fit-to-deadline`. Do not quietly widen the appetite.
- If the user wants a realistic duration rather than a budget, hand off to `how-long-will-it-take`.

## Step 7: Done looks like

Three criteria, each checkable by someone other than the user without asking the user whether it counts. A criterion about a number, a yes/no state, or an action someone has taken passes. "It feels polished" does not.

Then one more line: **what excellent looks like beyond done.** One sentence naming the difference between finished and good, such as "the reader does not need to ask a follow-up question." This line is what extra time buys. It is not a fourth requirement, and nothing is late for missing it.

## Step 8: Out of scope

At least two items. Name things next to the work that a reasonable person might assume are included, and set them aside in writing. Specific beats generic: "the pricing page" beats "other stuff". If the user has been burned before, name what crept in last time.

If the user and a requester disagree on what is in, stop drafting this section and point to `scope-the-work`.

## Step 9: Biggest risk and the tripwire

Name the one thing most likely to make this fail or run long. Not a list. One risk, in a sentence, with the reason it is the biggest.

Then write the tripwire as an if-then with a date or time in it: **"If X by Y, then Z."**

- X is something observable that has or has not happened.
- Y is a calendar point, not "soon" or "halfway".
- Z is a concrete action: cut this, ask that person, switch to the fallback. "Reconsider" is not an action.

An if-then plan made in advance is easier to act on than a decision made under pressure. Gollwitzer's 1999 work on implementation intentions is the research behind the format. If the plan is high stakes and worth a harder look, hand off to `what-could-go-wrong`.

## Step 10: Who or what helps

Split the work into its main parts and give each one a home: do it alone, ask a specific person, or hand to an AI. For a person, name the role and the one thing to ask them. For an AI, say which part, and if the user could not check the output, say so and hand off to `delegate` for the check. Do not duplicate `delegate`'s table here. Three or four lines is the limit.

## Step 11: First move

One concrete action, under 30 minutes, that the user can begin without deciding anything else. It names the object and produces something visible: a file, a message sent, a list written.

- Weak: "Start researching."
- Strong: "Write the three done criteria above in the project doc and send them to Dana for a yes or no."

If the user named when they will work, attach it: "Tomorrow at 9:00, ...". A move with a time and a place is the same if-then logic as the tripwire.

## Step 12: What I had to assume

List every guess that went into the card, one line each, with the card line it would change if wrong. Also list anything that could not be checked: a date the user may have wrong, a fact about the requester, a constraint that was never stated. This section is not optional and must not be empty. A card with no assumptions was not honestly drafted.

## Step 13: Offer the hand-offs, once

After the card, in one line, name the single most useful next step, if there is one. Do not list all siblings.

- Time-box problem: `fit-to-deadline`.
- Plan worth stress-testing: `what-could-go-wrong`.
- Disagreement over what is in: `scope-the-work`.
- Work includes an AI or person handoff: `delegate`.
- Wants a realistic duration: `how-long-will-it-take`.

None of these is needed for the card to stand. If the named skill is not installed, say what the step would be in a sentence and carry on.

---

## Output

One page, in this order, in plain text the user can screenshot or paste. Use the layout in `assets/work-card.md`.

1. Outcome
2. Who it is for, and what they will do with it
3. Why now
4. Appetite
5. Done looks like (3 criteria, plus the excellent line)
6. Out of scope
7. Biggest risk, and the tripwire
8. Who or what helps
9. First move
10. What I had to assume

Then up to three questions, each naming the line it would change, and one hand-off line. Nothing else. No preamble, no closing summary.

The 5-line card keeps Outcome, Done looks like, Out of scope, First move and What I had to assume.

---

## Failure modes

**Interviewing first.** Asking five questions before showing anything. The card is the question. Draft it, then ask.

**An activity as the outcome.** "Work on the deck" or "research competitors". Rewrite as a result someone could observe.

**Done criteria that are feelings.** "Looks good", "the team is happy". Replace with something a third party can verify.

**Appetite as an estimate.** "Probably about two weeks." That is a prediction. Write what the work is worth, and what happens at the limit.

**A generic out-of-scope list.** "Anything not mentioned above." Name the actual adjacent things.

**A tripwire with no date, or with "reconsider" as the action.** Neither can be acted on. Add a date and a verb.

**A first move that is a phase.** "Do the research." If it takes more than 30 minutes or needs a decision first, split it until it does not.

**The excellent line turning into scope.** It is a note on what spare time buys. If it appears in the done criteria, move it back.

**A card for a task that did not need one.** If it is under about 30 minutes, give the first move and stop.

**Inventing facts.** A deadline, a name or a budget the user never gave. Put it in the assumptions as a guess, or leave a bracket.

**Running past one page.** If the card does not fit, the work is too big for one card. Write a card for the first stretch.

A filled card means the start was decided on purpose. It does not mean the plan is right or the work will go well.

---

## Supporting files

- `assets/work-card.md` - the fill-in template, in the order the skill outputs it, plus the 5-line version
- `assets/worked-examples.md` - four filled cards from unrelated fields, for calibrating how specific each line should be
