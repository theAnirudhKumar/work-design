# lessons learned

**Five minutes after the work ends, so the next estimate starts from what happened.**

Most finished work teaches nothing. The lesson is a feeling ("that ran long") that fades by the next project, and the next estimate is built from the same optimistic picture as the last one.

This skill runs a short retro on one piece of work, finished or abandoned. It fills a small planned-versus-actual table for time, scope and quality, names the largest surprise, picks what to repeat and what to stop, and classifies the cause of any miss as estimate, scope, dependency, quality bar, energy or information, so patterns show up over time. It ends on one change for next time, written as an if-then, and a log entry in a shape that `how-long-will-it-take` can use as a reference case: type of work, size, planned duration, actual duration, what drove the gap.

The failure this exists to prevent: **finishing a piece of work and keeping only a vague sense of how it went, so the same miss repeats and nothing is on record to show it is a pattern.**

**Reach for it:** at the end of any piece of work, including work you dropped. Part of [work-design](https://github.com/theAnirudhKumar/work-design), at the Learn stage.

---

## Examples

*Illustrative. The people and organisations are invented, and the exact output varies with what you give it.*

**A kitchen renovation, for a small builder.** You type: `Kitchen job for the Okafor-Lindqvist house is finished. I quoted 6 weeks, it took 9. Retro?`

You get (shortened):

```
Planned vs actual
Time:    6 weeks / 9 weeks / +3 weeks (+50%)
Scope:   full strip-out and refit / plus a relocated gas line / added
Quality: no snagging list at handover (recalled: no bar was set)

Largest surprise: the gas line move, which needed an inspection slot
two weeks out.
Miss class: dependency (waiting on the inspection), not estimate.
One change: if a job includes any regulated trade work, then I book the
inspection slot before I confirm the end date to the client.

Log entry:
| 2026-11 | kitchen refit | medium, 1 room | 6 wk | 9 wk | dependency | inspection lead time |
Assumed: weeks are elapsed, not effort. Could not check: whether the
gas line was in the original quote.
```

**A data migration, in a software team.** You type: `We dropped the billing-service migration after three weeks. Log this.` The retro records it as abandoned, classifies the miss as information (the legacy schema was undocumented), and logs the reason for stopping so the next migration estimate can carry it.

With five or more entries in `work-log.md`, it offers a read across them: the recurring miss class and the type of work most under-estimated. With fewer, it says plainly that fewer than five entries is anecdote, not pattern.

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Planned vs actual | A table for time, scope and quality, with recalled figures marked as recalled |
| The largest surprise | One event, the one that closes most of the gap if removed |
| Repeat and stop | One to three each, specific to this work |
| Classify the miss | One of six causes, with the evidence |
| One change | A single if-then tied to the cause (Gollwitzer 1999) |
| The log entry | A short block in the `how-long-will-it-take` shape, appended to `work-log.md` if you agree, otherwise printed to paste |
| The pattern read | Offered only at five or more entries |

---

## Who this is for

Anyone who finishes pieces of work and plans the next ones, in any field. You do not need a project tool or a file system. Without file access, the entry is printed for you to paste into your own notes.

---

## What this needs

**Minimum:** a sentence on what the work was and how it went.

**Better with:** the original plan and the real start and end dates or hours.

**Best with:** an existing `work-log.md`, so entries accumulate and can be read across.

Missing context never blocks this skill. It records ranges, marks what was recalled and what it could not check, and does not invent a miss.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the lessons-learned skill from https://github.com/theAnirudhKumar/work-design: copy its skills/lessons-learned folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/lessons-learned` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method and `assets/work-log-entry.md` is the entry template you can fill by hand.

---

## Where this comes from

The log exists to feed `how-long-will-it-take`, which corrects an estimate against how long similar work took. An estimate can only be corrected against cases someone wrote down. The if-then change is an implementation intention (Gollwitzer 1999). The five-entry threshold is a deliberate caution, not a statistical test: it keeps one odd project from being reported as a trend.

---

## What this does not do

- **Not a review of the work's quality.** `review-my-work` challenges a draft. This reviews the process and the plan.
- **Not a conversation handoff.** `continue-in-new-chat` carries a chat into the next chat.
- **Not an estimate.** `how-long-will-it-take` reads the log; this writes it.
- **Not a meeting close.** Decisions and actions from a meeting belong to `meeting-close` in meeting-design.
- **Not blame.** The unit is the work and the plan, not the person.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
