# meeting or message

**Choose the channel the decision needs, not the one that's already open.**

Most communication overhead isn't a bad meeting or a bad message - it's the wrong one. A decision needing five minutes of back-and-forth gets a thirty-minute meeting; a call needing everyone's live reaction gets a message three people don't open until the next day. Nobody chose badly on purpose - they reached for the habitual channel before asking what this decision actually needed.

This skill asks that question first. It names what has to be true when the communication is over - a decision made, information passed one direction, live reactions gathered at once, or something durable to point back to - then checks reversibility, how many people genuinely need to be live versus just informed, and what waiting actually costs. It ends on one medium, names the runner-up, and says what the runner-up would have cost. When the answer is a meeting, it hands off to [`meeting-design`](https://github.com/theAnirudhKumar/meeting-design) for the agenda and attendee list rather than duplicating that work.

The failure this exists to prevent: **choosing the medium out of habit - "let's hop on a call" or "I'll just send a quick message" - before asking what the decision actually needs.**

**Reach for it:** every day. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it.*

You type: `Sarah and Tom need to agree on the vendor. Should I set up a meeting?`

You get:

```
Medium: written proposal with a reply deadline (Thursday 5pm).
Runner-up: a 25-minute call with the two of them.
What the runner-up would have cost: finding a slot in both calendars for a
decision that is cheap to reverse (30-day trial) and blocks nobody.

Switch to the call if either of them objects in writing: at that point it
needs live back-and-forth, between two people, which is a call, not a meeting.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Name what has to happen | Not what this is about - what has to be true when it's over: a decision, a one-way transfer, gathered live reactions, or a durable record |
| Check reversibility | The single biggest lever - whether this decision tolerates a fast, lossy channel or earns the slower one that lets people push back first |
| Check who needs to be live | The line between an audience (who can absorb this on their own time) and people who need to react to each other in real time |
| Check what waiting costs | Whether async's usual cost advantage actually holds here, or whether the work is genuinely blocked until this resolves |
| Make the call | One medium, one runner-up named, one sentence on what the runner-up would have cost |
| Hand off if it's a meeting | A plain stop-here line naming `meeting-design` for the agenda and attendee list, with the install commands if it is missing, rather than building either itself |

---

## Who this is for

Anyone about to default to "let's hop on a call" or "I'll just send a message" and wants a real answer instead of a habit - someone weighing email against Slack, a sync against an async thread, or whether a decision is actually worth a meeting before the invite goes out.

You don't need a calendar connector or any tooling. What needs deciding, and roughly who's involved, is enough to get a real answer.

---

## What this needs

**Minimum:** what needs to get decided or conveyed, and roughly who is involved.

**Better with:** how reversible the decision is, whether the people involved share a timezone, and whether this is one-off or something that recurs in this shape.

**Best with:** what happened last time something like this was handled the wrong way - a meeting that should have been a message, or a message thread that dragged for days because it actually needed a call.

Missing context never blocks this skill. It produces a medium and the reasoning from what it's given, and marks plainly what it had to assume.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other eight skills):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the meeting-or-message skill from https://github.com/theAnirudhKumar/work-design: copy its skills/meeting-or-message folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/meeting-or-message` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/evidence.md` is the research this skill's framing draws on, and `assets/medium-call.md` is the one-page fill-in template - what has to happen, reversibility, who needs to be live, what waiting costs, the call and the runner-up.

---

## Where this comes from

The reversibility-and-simultaneity framing draws on media richness theory - Daft & Lengel, "Organizational Information Requirements, Media Richness and Structural Design," *Management Science*, 1986 - which established that different media carry different capacity for fast feedback, multiple cues and shared context, and that mismatching a message's need for richness to the medium carrying it is a distinct, nameable failure rather than a vague complaint about "too many meetings." It's cited as conceptual grounding for the shape of the skill, not a fresh dataset - decades-old, foundational theory, not a statistic requiring a live check. The step-by-step decision table itself is this skill's own synthesis for the single-decision case, not lifted from the 1986 paper, which addresses organizational structure rather than one piece of communication.

---

## What this does not do

- **Not a meeting builder.** Once a meeting is the call, building the agenda, picking the decision rule, and deciding who's in the room is `meeting-design`'s job. This one hands off rather than duplicating it.
- **Not a review of an existing standing meeting.** Whether a recurring meeting already on the calendar should keep happening is `meeting-audit`'s question, not this one's.

## Where the meeting goes next

If the answer is a meeting, install [`meeting-design`](https://github.com/theAnirudhKumar/meeting-design):

```
/plugin marketplace add theAnirudhKumar/meeting-design
/plugin install meeting-design@meeting-design-marketplace
```

That repository has `meeting-design` for before a meeting, `meeting-close` for after it, and `meeting-audit` for recurring meetings. `meeting-close` and `meeting-audit` arrive with its v2.0.0 release; if they are not in your install yet, `meeting-design` is.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
