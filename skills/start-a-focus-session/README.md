# start a focus session

**Turn "I should get some work done" into one block with a task, an end, and the phone out of reach.**

Most people who say they will focus for an hour sit down with a vague project, no finish line and the phone beside the keyboard. This skill picks a format (Pomodoro 25/5, 52/17, a 90-minute block, flowtime or a plain hour) from the task and your energy, and writes a Focus Card before you start: one task, what done looks like for this session, the first two-minute action, a parking lot for stray thoughts, phone and notifications away, and a break plan. When you come back and say "done", "got interrupted" or "didn't finish", it runs a 60-second debrief and offers the next block or a stop.

Claude cannot keep time. It says so once, and you set the timer.

The failure this exists to prevent: **sitting down to "work" with no defined task, no end, and the phone in reach, so the hour disappears into switching and nothing is finished.**

**Reach for it:** when you are about to start something and want a structured block. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Examples

*Illustrative. The people are invented, and the exact output varies with what you give it.*

**A nursing student before an exam.** You type: `Help me focus for 90 minutes on pharmacology, I keep opening my phone.`

You get (shortened):

```
Format: two 45-minute blocks (Pomodoro-style would chop your recall
practice; a single 90 is long for revision you have been avoiding).
Task: answer the 25 practice questions on cardiac drugs.
Done: all 25 attempted, wrong ones starred, not yet reviewed.
First action: open the question set and read question 1 aloud.
Parking lot: paper beside you. Phone: in your bag across the room.
Timer: I cannot keep time. Set one for 45 minutes now, on a watch or a
kitchen timer, not the phone.
Break: stand, water, window. No feed.
```

**A designer who works in an open office.** You type: `I need 2 hours on the brand deck but people keep stopping by.` You get a 90-minute block, a headphones-on signal, a fallback room, a note that a daily pattern is a job for `protect-my-focus`, and a done-line written as an output ("slides 1 to 6 in rough layout").

**After the block.** You type: `got interrupted at about 40 minutes by the landlord's call.` You get a four-line debrief: what got done, what pulled you away, one change (a 25-minute restart with the phone on Do Not Disturb), and the stopping point written down so you resume without re-reading.

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Take the task | One task and a done-line, with at most two questions |
| Pick the format | One format and a reason, with the runner-up named |
| Write the card | Task, done-line, first action, parking lot, phone, timer, breaks |
| Special cases | Shared workspaces, creative work, interruptible jobs, difficulty starting |
| Debrief | What got done, what pulled attention, one adjustment, next block or stop |

---

## Who this is for

Students, nurses, founders, writers, engineers, parents working from home, freelancers and shift workers. Anyone with a task and a block of time. It works for people who find starting hard: it offers strategies such as shrinking the first step, body doubling and shorter blocks, and never diagnoses.

---

## What this needs

**Minimum:** the task and roughly how long you have.

**Better with:** your energy, where you are working and what usually pulls you away.

**Best with:** a `my-system.md` profile, if you have one, so the format matches methods you already chose.

Missing context never blocks this skill. It marks what it assumed. A timer is yours to set: Claude cannot keep time, remember across chats or see your phone.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the start-a-focus-session skill from https://github.com/theAnirudhKumar/work-design: copy its skills/start-a-focus-session folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/start-a-focus-session` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/formats.md` is the cheat-sheet of formats and when each backfires, and `assets/focus-card.md` is a card you can fill in without the skill.

---

## Where this comes from

Pomodoro is from Francesco Cirillo. The 52/17 split is popularised from a time-tracking company's own data, not a controlled trial. The 90-minute block rests on a rhythm claim that is contested. Flowtime is folk practice. All of these are labelled Practice only or Mixed in the reference file, and the skill tells you to judge them by your own results over several blocks.

---

## What this does not do

- **Not a timer.** It cannot keep time or remind you. You set the timer.
- **Not day planning.** `plan-my-day` chooses what the day holds; this runs one block.
- **Not a fix for daily interruptions.** `protect-my-focus` handles the pattern.
- **Not therapy or diagnosis.** Starting difficulty gets strategies, not labels.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
