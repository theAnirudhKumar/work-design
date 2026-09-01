# pick the medium

**Choose the channel the decision needs, not the one that's already open.**

Most communication overhead isn't a bad meeting or a bad message - it's the wrong one. A decision needing five minutes of back-and-forth gets a thirty-minute meeting; a call needing everyone's live reaction gets a message three people don't open until the next day. Nobody chose badly on purpose - they reached for the habitual channel before asking what this decision actually needed.

This skill asks that question first. It names what has to be true when the communication is over - a decision made, information passed one direction, live reactions gathered at once, or something durable to point back to - then checks reversibility, how many people genuinely need to be live versus just informed, and what waiting actually costs. It ends on one medium, names the runner-up, and says what the runner-up would have cost. When the answer is a meeting, it hands off to a meeting-design skill for the agenda and attendee list rather than duplicating that work.

The failure this exists to prevent: **choosing the medium out of habit - "let's hop on a call" or "I'll just send a quick message" - before asking what the decision actually needs.**

Part of the **Deciding how work runs** group in [work-design](../../#readme).

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Name what has to happen | Not what this is about - what has to be true when it's over: a decision, a one-way transfer, gathered live reactions, or a durable record |
| Check reversibility | The single biggest lever - whether this decision tolerates a fast, lossy channel or earns the slower one that lets people push back first |
| Check who needs to be live | The line between an audience (who can absorb this on their own time) and people who need to react to each other in real time |
| Check what waiting costs | Whether async's usual cost advantage actually holds here, or whether the work is genuinely blocked until this resolves |
| Make the call | One medium, one runner-up named, one sentence on what the runner-up would have cost |
| Hand off if it's a meeting | A plain stop-here line pointing to a meeting-design skill for the agenda and attendee list, rather than building either itself |

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

**The easy way: one paste**

```
I want to install the pick-the-medium skill from
https://github.com/theAnirudhKumar/work-design. Download or clone the
repository, then copy the skills/pick-the-medium folder into
~/.claude/skills/ (or .claude/skills/ if this is for one project only),
keeping its own folder name. Tell me the exact folder path it landed in
when you are done.
```

**In the Claude app (no terminal needed)**

1. Download this repository as a ZIP, or clone it
2. Zip the `skills/pick-the-medium` folder on its own
3. In Claude, go to Customize, then Skills, then Create skill, then Upload skill
4. Upload the ZIP

**As a plugin, in Claude Code or Cowork**

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

**Want the whole set?** The [main README's install section](../../#readme) installs all 9 skills at once.

**Or just read it.** `SKILL.md` is the method, `references/evidence.md` is the research this skill's framing draws on, and `assets/medium-call.md` is the one-page fill-in template - what has to happen, reversibility, who needs to be live, what waiting costs, the call and the runner-up.

---

## Where this comes from

The reversibility-and-simultaneity framing draws on media richness theory - Daft & Lengel, "Organizational Information Requirements, Media Richness and Structural Design," *Management Science*, 1986 - which established that different media carry different capacity for fast feedback, multiple cues and shared context, and that mismatching a message's need for richness to the medium carrying it is a distinct, nameable failure rather than a vague complaint about "too many meetings." It's cited as conceptual grounding for the shape of the skill, not a fresh dataset - decades-old, foundational theory, not a statistic requiring a live check. The step-by-step decision table itself is this skill's own synthesis for the single-decision case, not lifted from the 1986 paper, which addresses organizational structure rather than one piece of communication.

---

## What this does not do

- **Not a meeting builder.** Once a meeting is the call, building the agenda, picking the decision rule, and deciding who's in the room is a meeting-design skill's job - this one hands off rather than duplicating it.
- **Not a review of an existing standing meeting.** Whether a recurring meeting already on the calendar should keep happening is that same meeting-design skill's own first step, not this one's.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
