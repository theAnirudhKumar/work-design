# get unstuck

**Find out why the work is stalled before you try harder at it.**

Most advice for a stuck task is one sentence: break it down and just start. That fits one cause in nine. If you are waiting on a reply, a smaller task does nothing. If a decision is hiding inside the task, starting makes it worse. If the work should not exist, effort is wasted.

This skill diagnoses first. It matches what you said against nine causes (unclear outcome, too big, waiting on someone, a hidden decision, fear of the result being judged, dull task, competing priority, wrong energy, not needed) and asks at most two questions, preferably one pick-from-a-list. It then gives one next action of 15 minutes or less, concrete enough to start without more thought, with a 5-minute fallback and an if-then to schedule it. If the cause is outside you, it drafts the exact message to send or the decision to force. If the work looks unnecessary, it offers to drop or defer it and says what that costs.

The failure this exists to prevent: **applying a generic push to a task that is stalled for a specific reason, so you try harder at the wrong thing and conclude the problem is you.**

**Reach for it:** when something has been on your list for too long. Part of [work-design](https://github.com/theAnirudhKumar/work-design), at the point where work stalls mid-run.

---

## Examples

*Illustrative. The people and organisations are invented, and the exact output varies with what you give it.*

**A grant report, in a small charity.** You type: `I keep putting off the year-two report for the Harbour Lights Trust. It's been on my list for three weeks. I have all the numbers but I can't write it.`

You get (shortened):

```
Diagnosis: this looks like a hidden decision. You said you have the
numbers but can't write it, which usually means there is a choice about
how to frame the shortfall in the numbers that hasn't been made.
Next action (15 min): write the shortfall in two sentences, once as
"we missed target because..." and once as "we changed approach because...".
Pick one. Stop there.
5-minute version: write only the first of the two.
If-then: if I sit down with my first coffee tomorrow, then I write
the two sentences before opening email.
Assumed / could not check: whether the funder has a template that
already dictates the framing.
```

**A restaurant supplier switch.** You type: `I need to move us to a new produce supplier and I'm going in circles on it.`

You get (shortened):

```
Diagnosis: could be a hidden decision or waiting on someone. One
question: which sounds most like it? (a) I haven't decided between the
two suppliers, (b) I'm waiting on a quote, (c) it's too big to start.
```

You reply `b`, and the output becomes the exact message to the supplier with a needed-by date, one thing to do while waiting, and no self-help action at all, because the stall is not yours.

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Read what you said | Tells matched against nine causes, with the phrase of yours that points to the cause |
| Ask at most two questions | One pick-from-a-list question where causes overlap, never an interview |
| Diagnose in one sentence | The cause plus the evidence, stated as a read you can correct |
| One next action | Verb, object, stopping point, 15 minutes or less, plus a 5-minute fallback |
| Schedule it | An if-then (implementation intention, Gollwitzer 1999) tied to a cue that already happens in your day |
| External cause | The message or forced decision, drafted, with hand-offs to `meeting-or-message` or `delegate` where relevant |
| Not needed | An explicit drop or defer option, with its consequence stated |

---

## Who this is for

Anyone with one specific piece of work that has stalled, in any field. It does not need a task tool, a calendar or a file. A sentence about the work and that it is stuck is enough.

---

## What this needs

**Minimum:** one sentence on the work and that it is stalled.

**Better with:** how long it has been stuck, what you tried, and who else is involved.

**Best with:** the deadline and what happens if it slips, which decides whether "drop it" is a real option.

Missing context never blocks this skill. It diagnoses from what it has, marks what it had to assume, and names any cause it could not rule out.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the get-unstuck skill from https://github.com/theAnirudhKumar/work-design: copy its skills/get-unstuck folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/get-unstuck` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/causes.md` holds the nine causes with a tell and a move for each, and `assets/stuck-check.md` is a one-page table you can run alone, without the skill.

---

## Where this comes from

The if-then scheduling is an implementation intention, from Gollwitzer (1999): deciding in advance when and where you will act. The skill does not claim it works for everyone or quote an effect size. The nine causes are a working checklist for sorting stalls, not a taxonomy from research, and the skill treats a tell as a lead, not proof.

---

## What this does not do

- **Not therapy or medical advice.** It does not diagnose anxiety, ADHD, depression or anything else. If you describe distress beyond work friction, it says once, kindly, that a person who can help is worth talking to, and goes on with the practical part only if you want it.
- **Not scoping, sizing or stress-testing.** `scope-the-work`, `fit-to-deadline` and `what-could-go-wrong` do those. "Too big to start" here gets a first slice, not a re-scope.
- **Not who does the work.** `delegate` decides that; this skill hands off to it when the cause points there.
- **Not a motivation tool.** No pep talk. It names the cause and the next move.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
