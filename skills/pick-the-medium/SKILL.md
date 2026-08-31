---
name: pick-the-medium
description: >
  Picks the channel for one piece of communication before it happens: a
  written message, a call, a shared document, or a meeting. Trigger when the
  user says "should this be a meeting or can I just send a message", "sync or
  async", "do I need a call for this", "email or Slack", "should I write this
  up or just tell them", "is this worth a meeting", "how should I communicate
  this", or names a decision or update and asks how to get it across. Weighs
  reversibility, how many people need to weigh in at once, and what waiting
  for a reply costs here, then ends on one medium and states why the others
  lost. When the answer is a meeting, hand off to a meeting-design skill for
  the agenda and attendee list; this one only picks the channel. Not for
  restructuring an existing meeting, building an agenda, or deciding whether
  a standing meeting should keep happening, which are that skill's own first
  step, not this one's.
---

# Pick the Medium

Most communication overhead is not a bad meeting or a bad message. It is the wrong one: a decision that needed five minutes of back-and-forth got a thirty-minute meeting, or a call that needed everyone's live reaction got a message three people didn't open until the next day.

The failure this exists to prevent: **choosing the medium out of habit ("let's hop on a call" or "I'll just send a quick message") before asking what the decision actually needs.** That is not a communication-skills problem. It is a design problem, and it is cheap to fix before the invite or the message goes out, expensive to fix after.

---

## What this needs

**Minimum: what needs to get decided or conveyed, and roughly who is involved.** It will produce a medium and the reasoning, and mark what it had to assume.

**Better with** how reversible the decision is, whether the people involved are in the same timezone, and whether this is one-off or something that will come up again in this shape.

**Best with** what happened last time something like this was handled the wrong way: a meeting that should have been a message, or a message thread that dragged for days because it needed a call.

---

## Step 1: Name what actually has to happen

Not "what is this about", what has to be true when it's over. A decision made. Information transferred one direction. Multiple people's reactions gathered at the same time. Something in writing that can be pointed back to later. These need different media, and naming the wrong one first is how a status update turns into a standing meeting.

## Step 2: Check reversibility

A decision that is cheap to undo tolerates a fast, lossy medium: a message, a quick reaction. A decision that is expensive or embarrassing to reverse earns the slower medium that lets people actually think and push back before it's made. This is the single biggest lever: most medium mismatches are a reversible decision routed through a slow, synchronous channel out of caution that the decision didn't need.

## Step 3: Check how many people need to be live at once

Information flowing one direction to people who can each absorb it on their own time does not need everyone in a room. A decision that needs several people's live reactions to each other (not just to the proposer) does. If nobody in the group needs to hear anyone else's reaction, that is not attendance, it is an audience, and an audience does not need a meeting.

## Step 4: Check what waiting actually costs

Async is cheaper than sync by default, but only when the wait is affordable. If a reply landing four hours from now blocks nothing, async wins even for something that would otherwise argue for a call. If the work is stalled until this is resolved, that cost has to be weighed against the medium honestly, not used to justify defaulting to a meeting out of habit.

## Step 5: Make the call

| Signal | Points toward |
| :--- | :--- |
| Reversible, one direction, nobody blocked | Written message |
| Reversible, needs a quick reaction, nobody blocked | Written message with a short reply window |
| Irreversible or high-stakes, needs live pushback from more than one person | Meeting, hand off to meeting-design |
| Needs live back-and-forth but only between two people | A call, not a meeting |
| Needs a durable record more than a live discussion | A shared document with comments, not a call |
| Recurring and always resolves in ten minutes with the same two people | A standing short call, not a recurring meeting |

Name the medium, name the runner-up, and say in one sentence what the runner-up would have cost that the choice avoids.

## Step 6: Hand off if the answer is a meeting

If Step 5 lands on a meeting, this skill's job is done. Say so plainly and point to a meeting-design skill for the agenda, the decision rule and who actually needs to be in the room; this skill does not build any of that, it only established that a meeting is the right container.

---

## Output

One medium, one runner-up named, one sentence on what the runner-up would have cost. Where a meeting is the call, an explicit hand-off line rather than an agenda.

## Failure modes to watch for

**Answering with the medium the user already has open.** The point is to check whether the habitual channel fits this decision, not to confirm it.

**Treating "this is important" as an argument for a meeting.** Importance argues for care in how the decision gets made, not automatically for everyone being live at once. A written proposal with a firm deadline for objections can carry as much weight as a room.

**Recommending async for something genuinely blocked and expensive to leave open.** Cheaper is not better when the wait itself is the cost. Say so rather than defaulting to the cheaper medium on principle.

## What this does not do

Build the agenda, pick the decision rule, or decide who is in the room once a meeting is the call; that is a meeting-design skill's job, and this skill hands off to it rather than duplicating it. Does not decide whether a standing meeting that already exists should keep happening; that is the same meeting-design skill's own first step, applied to a meeting already on the calendar rather than a new piece of communication.

## Supporting files

- `assets/medium-call.md` - a one-page fill-in template: what has to happen, reversibility, who needs to be live, what waiting costs, the call and the runner-up.
