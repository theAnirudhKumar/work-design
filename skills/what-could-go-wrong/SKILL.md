---
name: what-could-go-wrong
description: >
  Stress-tests a plan by assuming it has already failed. Trigger when the user
  says "what could go wrong with this plan", "stress test this plan",
  "pre-mortem", "poke holes in this", "assume this fails, why", "is this plan
  realistic", "what am I missing", "risks for", or pastes a plan, launch,
  project or decision and asks whether it will hold. Works backwards from a
  dated failure to 5 to 7 causes specific to this plan, each with a dated
  early-warning signal, an if-then response and the cheapest prevention, then
  names the one assumption that sinks the work, a test of it this week, and a
  verdict: proceed, proceed with changes, or re-plan. Has a solo mode and a
  group script. Not for reviewing a finished draft, which is review-my-work,
  and not for framing the work in the first place, which is plan-the-work.
---

# What Could Go Wrong

Plans are usually reviewed by asking what could go wrong, and people answer that politely with generic risks nobody acts on. A pre-mortem changes the question: the work has already failed, so explain why. That makes it safe to say the things the plan's author does not want to hear.

The failure this exists to prevent: **a plan that goes ahead carrying a fatal assumption nobody examined, because the review asked for "risks" and got scope creep and timeline slip instead of the specific thing that would actually sink it.**

The method follows Gary Klein's project premortem (Harvard Business Review, 2007) and uses Gollwitzer's implementation intentions (1999) for the responses: a decision made now in the form "If X by Y, then Z", so that nobody has to decide under pressure later.

---

## What this needs

**Minimum: the plan, pasted or described in a few sentences.** Goal, rough timing, who is involved. No file, connector or tool.

**Better with** the date the work is meant to finish, what success looks like, and the one or two things the author is already worried about.

**Best with** what happened the last time similar work was tried, and the names or roles of the people the plan depends on.

If the plan is too thin to name anything specific, do not guess at generic risks. See Step 1.

---

## When this runs

Runs when there is a plan, launch, project, hire, migration, campaign or decision that has not happened yet, and the user wants to know where it breaks.

**Does not run for:**

- A finished draft, document or deliverable. That is `review-my-work`.
- Framing the work: what it is, who it is for, what done means. That is `plan-the-work`, whose "biggest risk and tripwire" line is the seed this skill expands. If the user has one, start from it.
- Fitting the work into a time budget. That is `fit-to-deadline`. Estimating how long it takes is `how-long-will-it-take`.
- Drawing the boundary of the work. That is `scope-the-work`.
- Planning for a deadlocked meeting. That belongs to `meeting-design`.
- Work already under way and stuck. That is `get-unstuck`.

---

## Step 1: Check there is enough to be specific

Read the plan. Can at least five failures be named that would not fit any other plan? If yes, go to Step 2.

If not, ask at most two questions, the two that would unlock the most specificity. Usually: who or what does this depend on that the author does not control, and what is the date it must be done by. Ask them as the whole reply. If the user cannot or will not answer, proceed on stated assumptions and mark every cause built on an assumption as "assumed".

Never fill the gap with "scope creep", "poor communication", "lack of resources" or "unclear ownership" unless the plan itself shows how that would happen here. A cause is acceptable only if it names a person, a dependency, a number, a date or a mechanism from this plan.

## Step 2: Set the failure

State the failure as fact, in the past tense, with a date: "It is [date]. The [work] has failed." Use the plan's own deadline or the point where success should be visible. Define failure in one line the way the user would: missed the date, shipped and nobody used it, shipped and was rolled back, was cancelled.

If the user did not give a date, pick one from the plan and say which.

## Step 3: Generate 5 to 7 causes

Write the causes as things that happened, not things that might: "The vendor's API access was approved six weeks late", not "vendor delays are a risk".

Cover all four groups. At least one cause in each:

- **Internal.** Skills, capacity, tooling, process, the team's own habits.
- **External.** Vendors, customers, regulators, markets, other teams, timing.
- **People.** Who decides, who blocks, who leaves, who was never asked.
- **Assumptions.** Things the plan treats as true and has not checked.

Include at least one cause the author would find uncomfortable. Include at least one that is dull and logistical, since those fail plans more often than dramatic ones.

## Step 4: For each cause, write the three things that make it usable

1. **Early-warning signal.** Something observable, with a date: "No signed data-sharing agreement by the 14th." Not "stakeholders seem disengaged".
2. **If-then response.** "If [signal] by [date], then [action by named role]." The action must be something that can be done, by someone, without a meeting to decide whether to do it.
3. **Cheapest prevention now.** The smallest thing that removes or shrinks the cause before the work starts. Often it is a question to ask or a person to ping, not a project.

## Step 5: Rank in plain words

Rank the causes by likelihood times damage, using words only: likely or unlikely, survivable or fatal. Give one line of reasoning each, drawn from the plan. Do not give percentages or scores. No honest numbers exist for most plans, and a fake one invites false precision.

A fatal and likely cause goes first even if it is dull. A fatal and unlikely cause still gets its prevention if the prevention is cheap.

## Step 6: Name the one assumption

Pick the single assumption which, if wrong, sinks the work however well everything else goes. It is usually hiding inside a cause from the assumptions group, or is what several causes share. State it as a sentence that could be false: "Customers will switch without a migration incentive."

Then give a test of it that can run this week, costs little, and could come back "no": a call to three people, a one-page mock-up shown to a buyer, a calculation, a request to the owner of the dependency. If no test can run this week, say what the nearest cheaper one is.

## Step 7: Give the verdict

One of three, with the reason in a sentence:

- **Proceed.** No fatal and likely cause is unmitigated. Say so only if that is true.
- **Proceed with changes.** List the changes, each tied to a cause. Changes come from the prevention column and the key-assumption test.
- **Re-plan.** The key assumption is untested and cannot be tested cheaply, or a fatal cause has no cheap prevention. Say what the new plan must settle first.

A pre-mortem that always ends on "proceed with changes" is not discriminating. Re-plan is a real outcome.

## Step 8: Say what you assumed

End with a short block: what the plan did not say that you assumed, which causes rest on those assumptions, and what you could not know (internal politics, past history, the true state of a dependency). The author knows these better than you do; their correction is the most valuable input in the whole exercise.

---

## Solo mode and group mode

**Solo mode** is the default: the user pastes a plan, Claude runs Steps 1 to 8. Suggest that the user show the output to one person who knows the work and ask what is missing, since a pre-mortem run by one author's assistant has the author's blind spots.

**Group mode** applies when the user is about to run it with a team. Offer this script, 30 to 45 minutes, and do not run the cause generation for them first, since the point is independent thinking:

1. **Frame (3 minutes).** The leader reads the plan aloud in one minute and says: "It is [date]. This has failed badly. Everyone write down why."
2. **Silent writing (7 minutes).** Each person writes their own causes, alone, on paper or in a private doc. No talking. Aim for at least five each, and ask for the ones they would not say in a planning meeting.
3. **Pool (10 minutes).** Go round the room, one cause per person per turn, until everything is out. The leader writes them up without comment or rebuttal. Merge duplicates only at the end.
4. **Rank (5 minutes).** Each person marks the three they think most likely and the three most damaging, silently. Tally. Take the top five to seven.
5. **Respond (10 minutes).** For each cause on the shortlist, fill one row of `assets/pre-mortem-sheet.md`: signal, if-then, prevention, and a named owner.
6. **Name the assumption (3 minutes).** Ask: "Which one thing, if wrong, makes all of this irrelevant?" Agree the test and who runs it by Friday.

Offer to take the pooled list afterwards and complete Steps 4 to 8 from it. Where the team's list and Claude's own list differ, show both: causes only Claude found are worth a look, causes only the team found are probably closer to the truth.

---

## Output

Fill `assets/pre-mortem-sheet.md` and give it in the chat. In order:

1. The failure statement, with its date.
2. A table of 5 to 7 causes: group, cause, why it is plausible here, ranking in words, early-warning signal with date, if-then response, cheapest prevention.
3. The one assumption and its test this week.
4. The verdict, with changes listed if any.
5. What I assumed and could not check.

---

## Failure modes

**Generic risks.** "Scope creep", "resourcing", "stakeholder buy-in" with nothing from the plan attached. Go back to Step 1 and ask, or cut the cause.

**Seven versions of one cause.** Five of the causes are really "the vendor is late". Merge them and find causes in the other groups.

**Signals nobody can observe.** "Team morale drops." Replace with something a person could see on a calendar, in a tracker, in an inbox or in a number.

**Responses that need a decision to start.** "Escalate and discuss." The if-then must name the action and who takes it.

**Invented likelihoods.** No percentages. Words and a reason.

**A pre-mortem as ritual.** If the verdict is always "proceed with changes" and no change is ever made, the exercise did nothing. Ask the user to put the first change on a date before closing.

**Treating a clean result as safety.** A pre-mortem surfaces what the people in the room can imagine. It does not find what none of them know. Say so when the verdict is "proceed".

---

## Supporting files

- `assets/pre-mortem-sheet.md` - the fill-in table and the key-assumption block this skill hands over
