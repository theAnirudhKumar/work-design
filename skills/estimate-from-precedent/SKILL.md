---
name: estimate-from-precedent
description: >
  Corrects a time or effort estimate by checking it against how long similar
  work actually took last time, instead of how long this instance feels like
  it should take. Trigger when the user says "how long will this actually
  take", "estimate this", "how long should I budget for", "is this timeline
  realistic", "we always run over on these, why", "sanity check my estimate",
  "how long did this take last time", or gives a time estimate and asks
  whether it holds up. Also trigger when a scope-the-work note or a delegate
  allocation needs a time figure attached. Asks for the closest past cases,
  pulls their actual duration, and adjusts the estimate toward that reference
  class rather than the gut number, naming the gap and why. Ends on an
  adjusted estimate with the reference cases shown, not a bare number. Not
  for cost in money, and not useful without a comparable past case; without
  one it says so rather than inventing a reference class.
---

# Estimate from Precedent

Ask someone how long a piece of work will take and they picture it going well: no interruptions, no rework, no waiting on someone else. That picture is not dishonest, it is just the wrong question. The right question is how long the last several things like this actually took, including the parts that did not go well, because those parts show up again almost every time.

The failure this exists to prevent: **an estimate built entirely from imagining this specific instance of the work, when a look at similar past instances would have caught the gap before it became a missed deadline.** This is a well-documented, specific failure, not a character flaw or a discipline problem, and it is corrected by changing what the estimate is built from, not by trying harder to imagine accurately.

---

## What this needs

**Minimum: the estimate someone has already made or is about to make, and what the work is.** It will ask for reference cases from that.

**Better with** two or three past instances of similar work and how long they actually took, even roughly remembered.

**Best with** actual logged time or dates from those past instances rather than memory, since memory of past duration is itself optimistic in the same direction as the fresh estimate.

---

## Step 1: Get the inside-view estimate

The number the person would give if asked right now, imagining this specific piece of work going the way they picture it going. Write it down before doing anything else; it is the number being corrected, and it needs to exist on the record to see the size of the correction later.

## Step 2: Build the reference class

Ask for the two or three closest past cases: similar work, similar scope, similar people involved. Not the best case that went unusually smoothly, and not the worst case that was a known outlier: the ordinary ones. If nothing comparable exists, say so plainly and stop here; an estimate corrected against an invented or forced reference class is worse than an uncorrected one, because it borrows false confidence.

## Step 3: Get what those cases actually took

Actual duration, not the estimate that was given for them at the time. This is the step most likely to get skipped because it takes longer than trusting memory, and it is the step where the correction actually happens, because memory of past duration compresses toward the plan the same way a fresh estimate does.

## Step 4: Compare and name the gap

State the inside-view number next to the reference-class number. If they are close, say so, that is useful information too. If they differ, name roughly by how much and, where it is visible, name what the inside-view estimate left out that the past cases had to deal with: a review cycle, a dependency on someone else, a revision after first feedback.

## Step 5: Adjust and give the range

The corrected estimate leans toward the reference class, not the inside view, in proportion to how many comparable cases there were and how consistent they were with each other. Give a range where the cases varied, not a single confident number dressed up as more certain than the input supports.

---

## Output

The original inside-view number, the reference cases with their actual durations, the gap named, and an adjusted estimate or range. All four shown together, not just the final number.

## Failure modes to watch for

**Accepting a reference class of one, described as "basically the same thing every time."** One case is an anecdote, not a class. Say the estimate is under-supported rather than presenting it with false confidence.

**Letting the person pick only the reference cases that went well.** The point of asking for ordinary cases rather than best cases is specifically to catch this. If every case offered went smoothly, ask directly whether any comparable case ran long, and use it if one did.

**Treating the adjusted number as exact.** The output is a corrected estimate, still an estimate. A range that is honest about the spread in the reference class is more useful than false precision.

## What this does not do

Estimate cost in money: this is about time and effort, and a dollar figure built the same way would need its own reference class of costs, not durations. Does not decide whether the work should happen at all or who should do it; scope-the-work and delegate answer those, and either can hand a number here to check. Does not work without a real reference class; it says so rather than estimating from nothing.

## Supporting files

- `assets/precedent-worksheet.md` - a one-page fill-in template: inside-view estimate, reference cases and their actual durations, the gap, the adjusted estimate or range.
- `references/evidence.md` - the planning-fallacy and reference-class-forecasting research this skill's approach is built on.
