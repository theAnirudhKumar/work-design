---
name: fit-to-deadline
description: >
  Trigger on "I only have X to do this", "this has to be done by", "how do I fit this in", "cut this down", "what can I drop", "what's the minimum version", "I'm running out of time", "too much to do before Friday", "how big should this be", or any work where the time is fixed and more is wanted than fits. Starts from the time budget and shrinks the work to fit: a ladder of three versions (Minimum, Target, Stretch), a ranked cut list with the cost of each cut, a calendar checkpoint rule for the halfway point, and the risk the Minimum is too thin. Also says so when the work is smaller than the time. Not for drawing a boundary note, which is scope-the-work, or for correcting a duration guess, which is how-long-will-it-take.
---

# Fit To Deadline

When time is fixed, the work has to give. Most people let it give by accident: everything is done at the same pace until the deadline, and then the last third is cut in a panic, in whatever order it happens to fall.

The failure this exists to prevent: **a fixed deadline with no decision about what goes first, so the cuts are made in the last hours by whatever is left, and the part that mattered most is the part that got dropped.**

Take the time as given, shrink the work to fit it, and decide the cuts in advance, while there is still room to choose.

---

## What this needs

**Minimum: the work and the time available**, such as "a client deck, I have two days". If the outcome is not stated, infer it, state it, and mark it as an assumption.

**Better with** the outcome the work must achieve and who it is for, since the Minimum is only honest against a stated outcome.

**Best with** a rough list of the parts of the work and any that someone else is waiting on.

If no time or deadline is given at all, ask once: "How much time do you have, or what is the deadline?" Do not draft until it is answered. This is the one question that cannot be replaced by an assumption, because the whole method runs off it.

---

## When this runs

Runs when the time is fixed or close to it and the work could grow past it, or when the user asks what the smallest acceptable version is.

**Does not run for:**

- Starting work with no outcome or audience yet. That is `plan-the-work`.
- Drawing a written boundary around a defined job, with a person who keeps adding to it. That is `scope-the-work`.
- Checking whether a duration guess is realistic against how long similar work took. That is `how-long-will-it-take`.
- Deciding who does which part. That is `delegate`.
- Being stuck mid-work. That is `get-unstuck`.

The difference from its neighbours: `scope-the-work` draws a boundary around a job whatever its length, and `how-long-will-it-take` corrects a duration. This skill starts from the time budget and shrinks the work to fit. It does not lengthen the deadline, unless it says plainly that the Minimum cannot fit and why.

---

## Step 1: Fix the three inputs

1. **The work**, in a sentence.
2. **The outcome it must achieve**, as one observable sentence. If the user gave only the work, write the outcome yourself and mark it as an assumption.
3. **The time**, as working hours the user can really protect. If the user gave a deadline, convert it: list the working days left, the hours per day they can focus, and subtract known commitments. State that conversion as an assumption so the user can correct it. Use the user's own numbers. Do not invent a typical figure.

## Step 2: Treat the time as fixed

The time budget is the constraint, and the scope is what moves. This is the appetite idea from Basecamp's Shape Up (Ryan Singer): fix the time first and let the scope flex, instead of fixing the scope and letting the time flex.

There is a reason not to leave the time open. Parkinson's law is the observation that work tends to expand to fill the time available for it. A named budget is the counter. Treat it as an observation, not a rule, and quote no figure for it.

## Step 3: Break the work into parts and weigh each

List five to ten parts of the work. If there are more, group them. For each part give:

- **Its size in hours**, marked as a guess where it is one. Use the user's figures where they gave them. If the user wants the sizes checked against past work, hand off to `how-long-will-it-take`.
- **What it contributes to the outcome**: essential (the outcome fails without it), helps (the outcome is weaker without it), or polish (the outcome holds without it).
- **What depends on it**: other parts that cannot exist without it.

This is a working list, shown in the ladder file, not a project plan.

## Step 4: Build the ladder

Three versions, each a set of the parts above.

**Minimum.** The smallest set that still delivers the outcome. Test it against the outcome sentence, and say in one or two lines why it still counts. If the Minimum does not honestly deliver the outcome, it is not the Minimum, it is a draft. Include only the essential parts.

**Target.** What fits the budget with some room left. Essential parts plus the helps parts that fit. This is the plan to work to.

**Stretch.** What gets added, in order, if things go better than planned. Each item must be something that can be stopped halfway without leaving damage. Never start Stretch before Target is finished.

Give each version its hours total, against the budget.

### If the Minimum does not fit

If even the essential parts exceed the budget, say so plainly, before anything else: "The Minimum does not fit in [time]. It needs about [hours], which is [N] over." Then give the reason in one line, and offer the options, in this order:

1. Change the outcome to something smaller that does fit, and say what it gives up.
2. Add time, and say how much and from where. This is the only case where the deadline is lengthened, and only as an option the user chooses.
3. Add hands, by moving a part to someone else or to an AI, with `delegate` for the check.

Do not quietly squeeze the Minimum to fit, and do not quietly stretch the deadline.

## Step 5: Rank the cuts

List what to drop, first to last. Order by **least outcome lost per hour saved**: the part that costs the outcome least and returns the most hours goes first.

For each item give:

- The hours saved.
- **The cost to cut**, in plain words: what the reader, client or user will notice or not notice. "Nobody will see it" and "the sceptic on the panel will ask this and we will have no answer" are both honest costs.
- Any part that must be cut with it.

Do not rank by what is easiest to cut or what the user likes least. Where the order is a close call, say so.

## Step 6: Write the midpoint rule

A decision rule written now, for the middle of the work, so that nobody has to decide under pressure. Format:

**"At [calendar point], if [observable thing] is not done, cut [item] and work to [version]."**

- The calendar point is a day and time, not "about halfway" or "when it feels behind".
- The observable thing is something a person could check, such as "the first full draft exists", not "I feel on track".
- The cut is an item already ranked in Step 5.

Write one rule for the halfway point. Add a second for the last stretch if the work is long, for example the day before. Offer to put them in the user's calendar if a calendar tool is connected, and write them out as text if not.

## Step 7: Name the risk of the Minimum being too thin

State what it looks like if the Minimum is cut too far: who would notice, and what they would say. Then give a cheap check that catches it early, such as showing the Minimum to one person who matches the audience before time is spent on the Target, with the one question to ask them. If the check fails, say what moves from the cut list back into the Minimum.

## Step 8: The inverse case

If the work is smaller than the time available, say so first: "This looks smaller than the time you have." Then offer, in this order:

1. **Raise the quality bar.** Name the specific thing the extra time buys: a review by someone who has not seen it, a test with a real user, a second pass on the part the audience reads first. For a skeptical read of a draft, `review-my-work` is the match.
2. **Stop early.** Finish at Target and give the time back. Finishing early is a legitimate outcome and often the best one.
3. **Add the next most valuable part**, but only a named one. Do not pad.

Do not let the work swell to fill the time. That is the Parkinson pattern this skill exists to work against.

## Step 9: Fill the ladder and hand it over

Fill `assets/sizing-ladder.md` and give it to the user. Put the assumptions and the unchecked items at the foot.

---

## Output

A filled sizing ladder:

1. The three inputs: work, outcome, time (with the conversion if a deadline was given).
2. The ladder: Minimum (with why it still counts), Target, Stretch, each with hours against the budget.
3. The ranked cut list: item, hours saved, cost to cut in plain words, dependencies.
4. The midpoint rule, as a calendar checkpoint.
5. The risk of the Minimum being too thin, and the cheap check.
6. What I had to assume and could not check.

If the Minimum does not fit, or the work is smaller than the time, that finding comes first, above the ladder.

---

## Failure modes

**Cutting by effort instead of by outcome.** Dropping the hardest part, or the part the user likes least. Rank by outcome lost per hour saved.

**A Minimum that is only a draft.** Test it against the outcome sentence. If it fails, it is not the Minimum.

**A midpoint rule with no date.** "Halfway through" cannot be checked. Use a day and an observable.

**Quietly extending the deadline.** The whole method is fixed time. Only extend as a stated option when the Minimum cannot fit, and say why.

**Quietly squeezing the Minimum to fit.** If it does not fit, the user needs to hear it now, not on the last day.

**Starting Stretch early.** Stretch only begins when Target is finished. Otherwise there are three half-done versions.

**Inventing hours.** If the user gave no sizes, mark every size as a guess. Do not present a guess as a measured figure.

**Filling spare time.** When the work is smaller than the time, name what the time buys, or give it back.

**Treating the Minimum as the goal.** The Minimum is the floor that was agreed in advance, the version to fall back to. The plan is the Target.

A filled ladder means the cuts were decided in advance. It does not mean the work will fit.

---

## Supporting files

- `assets/sizing-ladder.md` - the template this skill fills in and hands over, with one filled example from an invented project
