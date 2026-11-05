---
name: lessons-learned
description: >
  "that's done, what did we learn", "wrap this up", "retro on this",
  "post-mortem on this project", "log this", "how did that go compared to the
  plan", "close out this work", "lessons from this". Runs a five-minute retro
  on one piece of finished or abandoned work: planned vs actual (time, scope,
  quality), the biggest surprise, what to repeat and stop, one if-then change,
  the miss classified (estimate, scope, dependency, quality bar, energy,
  information), and a log entry that how-long-will-it-take can use as a
  reference case. Not for reviewing a draft's quality (review-my-work), carrying
  chat context (continue-in-new-chat), estimating (how-long-will-it-take) or closing
  a meeting (meeting-close).
---

# Lessons Learned

Most finished work teaches nothing, because the lesson is a feeling ("that took longer than I thought") that fades by the next project. The estimate for the next piece of work is then built from the same optimistic picture as the last one.

The failure this exists to prevent: **finishing a piece of work and keeping only a vague sense of how it went, so the same miss repeats and nothing is on record to show it is a pattern.**

Spend about five minutes, produce a small table and one change, and write one log entry.

---

## What this needs

**Minimum: a sentence on what the work was and how it went.** Enough to fill the table with ranges and mark what is unknown. A retro from memory is worth doing.

**Better with** the original plan or estimate, and the real start and end dates or hours. Memory of duration drifts toward the plan, so numbers beat recollection.

**Best with** file access and an existing `work-log.md`, so the entry is appended and patterns across entries can be read.

Nothing is a prerequisite. Without file access the entry is printed in a block to paste into the user's own notes.

---

## When this runs

Runs once, soon after a piece of work finishes **or is abandoned.** Abandoned work gets a retro too, and often the more useful one: it records what made stopping the right call.

**Does not run for:**

- Judging whether a draft is any good. The `review-my-work` skill does that.
- Carrying a conversation into a new chat. `continue-in-new-chat` does that.
- Producing an estimate for new work. `how-long-will-it-take` does that; this skill writes the log it reads.
- Closing out a meeting: decisions, actions, owners. `meeting-close` in meeting-design does that.
- Stress-testing a plan before it starts. The `what-could-go-wrong` skill does that.

---

## Step 1: Pin down planned vs actual

Ask for or find, in one message: what was planned and what happened, for three things.

- **Time:** planned and actual duration, in the same unit. Use hours of effort if known, otherwise elapsed days. Say which.
- **Scope:** what was in the plan, what was added, what was cut.
- **Quality:** the bar set at the start (if any) and where the result landed against it. If no bar was set, say that; it is itself a finding.

If the user does not know a figure, record a range and mark it "recalled". Ask at most three questions in total. Do not hold the retro for missing numbers.

If a `plan-the-work` or `scope-the-work` boundary note exists, read it for the original plan rather than asking.

## Step 2: Fill the table

| | Planned | Actual | Gap |
| :--- | :--- | :--- | :--- |
| Time | | | |
| Scope | | | |
| Quality | | | |

Gap in words and, for time, a ratio or difference. Do not round a recalled figure into a precise one.

## Step 3: Name the largest surprise

One thing: the event or discovery that moved the outcome most. Not the longest list. If the user names three, pick the one that, removed, would have closed the most of the gap, and say why.

## Step 4: What to repeat, what to stop

One to three items each, specific to this work. "Communicated well" is not repeatable; "sent the client a draft on day two instead of day six" is. Each "stop" names a behaviour, not a trait.

## Step 5: Classify the miss

Where there is a gap in time, scope or quality, assign the **primary cause** to one of six. Pick one; note a secondary if truly needed.

| Class | Meaning | Typical sign |
| :--- | :--- | :--- |
| Estimate | The plan was too optimistic about the same work | Same work, took longer or shorter than imagined |
| Scope | The work grew or shifted | New items added, boundary never written |
| Dependency | Waiting on a person, approval or input | Idle time between active time |
| Quality bar | The bar was unclear or moved | Rework after "done" |
| Energy | Capacity, interruption or attention, not the work itself | Slow weeks, context-switching |
| Information | A fact was missing or wrong at the start | Reversal once a fact appeared |

If there was no miss, record "none" and say what helped. Do not invent one.

## Step 6: One change, written as an if-then

Exactly one. Not a list of resolutions. Form: **"If [a situation that will actually recur], then [specific action]."** Example: "If a task needs a sign-off from someone outside the team, then I ask for their turnaround time before I commit a date." Tie it to the classified cause. The if-then form is borrowed from implementation intentions (Gollwitzer 1999); do not claim more for it than that it fixes the trigger in advance.

## Step 7: Write the log entry

Fill `assets/work-log-entry.md`. It is built to match the precedent worksheet in `how-long-will-it-take`: **type of work, size, planned duration, actual duration, what drove the gap**, so each entry can be read as a reference case later.

- **With file access:** offer to append the entry to `work-log.md` (suggested name, in a place the user chooses). Confirm before writing. Create the file with the entry format's header only if it does not exist and the user agrees.
- **Without file access:** print the entry in a code block and say to paste it into the user's own notes, under a date.

Keep the entry short enough to fill in two minutes. A log that is tedious does not get kept.

## Step 8: Offer a pattern read, but only at five entries

If `work-log.md` exists and holds **five or more** entries, offer a read across them: the recurring miss class, the type of work most under-estimated (planned vs actual ratio by type), and whether the one-change if-thens from earlier entries show up as fixed. Present as a read of the user's own log, not a general finding.

If there are **fewer than five**, say plainly: fewer than five entries is anecdote, not pattern. Offer to keep logging, and do not report a trend. With one to four entries, you may point out an observation but label it as one case.

---

## Output

In this order:

1. **Planned vs actual** table (time, scope, quality).
2. **Largest surprise**, one sentence.
3. **Repeat** and **Stop**, one to three each.
4. **Miss class**, with the evidence.
5. **One change for next time**, as an if-then.
6. **Log entry**, filled, in a block or appended.
7. **What I had to assume or could not check**: recalled figures, missing plan, anything classified on thin evidence.
8. **Pattern read**, only if five or more entries exist.

---

## Failure modes

**A retro that becomes blame.** The unit of analysis is the work and the plan, not the person. "The estimate left out review time" beats "I was too slow".

**A list of ten lessons.** Ten lessons is none. One change, an if-then, tied to the miss class.

**Recalled numbers presented as measured.** Mark them. A wrong precise number poisons the log, which is later used as a reference class.

**Classifying every miss as "estimate".** Check scope, dependency and information first. If the plan was fine and the world changed, that is not an estimate error.

**Skipping abandoned work.** The entries from stopped work show the real rate of false starts. Log it with "abandoned" and the reason.

**Calling a pattern from fewer than five entries.** Fewer than five is anecdote. Say so.

**Writing to the log without asking.** Confirm before appending.

**Drifting into quality review.** If the user wants the output itself judged, hand off to `review-my-work`; this skill reviews the process.

---

## Supporting files

- `assets/work-log-entry.md` - the log entry template, one block per piece of work, compatible with the `how-long-will-it-take` precedent worksheet, plus a one-line row form for the log file.
