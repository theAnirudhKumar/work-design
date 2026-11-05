---
name: protect-my-focus
description: >
  Trigger on "I'm constantly interrupted", "meetings eat my day", "Slack is killing me", "I can't get deep work done", "people keep dropping by my desk", "too many notifications", "how do I tell my manager I need focus time", "my inbox runs my day". Audits interruption sources (notifications, chat, email, drop-ins, meetings, self-interruptions), ranks them by cost, picks countermeasures, drafts the actual messages to send a manager or team, and sets a 2-week experiment with one measure. Designs for interruptible jobs such as support, nursing and caregiving instead of pretending interruption away. Not for one focus block right now (start-a-focus-session), cleaning up recurring meetings (meeting-audit), planning the week (plan-my-week) or a task that has stalled (get-unstuck).
---

# Protect My Focus

Finds where the user's attention actually goes, ranks the sources by what they cost, picks the few countermeasures that fit the job, and writes the messages that negotiate them. It ends on a two-week experiment with one measure, not a list of tips.

The failure this exists to prevent: **telling someone to "just turn off notifications" in a job where that is impossible, or never negotiating the real source of the interruptions.**

---

## What this needs

**Minimum: a description of the job and what interrupts it.** "I'm a support lead, chat pings all day and my manager pulls me into calls" is enough. No files, no calendar, no analytics, no other skill.

**Better with** a typical day or the last two days written out roughly, who interrupts, and what the user's manager expects about response times.

**Best with** a pasted calendar week (text) and a screen-time or notification summary, so meetings and notifications are counted rather than guessed. Claude cannot see the calendar or the phone; the user pastes or reads off numbers. A `my-system.md` profile, if pasted, supplies hard constraints and peak hours.

Missing detail never blocks the audit. It means more of the ranking is labelled as a guess.

---

## When this runs

Runs when interruptions are a pattern, not a single afternoon.

**Does not run for:**

- One block of focus right now. `start-a-focus-session` handles that.
- Cleaning up recurring meetings (cancelling, shortening, changing format, fixing agendas). `meeting-audit` in the meeting-design set owns that. Here, meetings are one source among six: count their cost, then hand off by name.
- Deciding whether one thing should be a meeting or a message. `meeting-or-message` handles that.
- A week that needs planning. `plan-my-week` handles that.
- A person who is overwhelmed by everything, not just interruptions. `balance-my-life` is closer; if there is distress, say once that someone who can help is worth talking to.

---

## Step 1: Place the job on the interruptibility line

Before anything else, ask or infer: **is interruption part of the job, or in the way of it?**

- **In the way of it** (analyst, engineer, writer, designer, researcher, manager with deep tasks): focus time can be carved out and defended.
- **Part of the job** (support, nursing, reception, caregiving, teaching, ops on-call, anyone whose role is to be available): do not pretend interruption away. Design for interruptible work: protect small windows, make resumption cheap, move the interruptible load into tools that batch it (a queue, a rota), and negotiate who covers when the user needs 30 minutes.
- **Mixed** (most roles): split the day into available hours and protected hours and say which is which.

State the placement in one sentence, with the user's words as evidence. It changes which countermeasures are offered. If the user is in the second group, never offer "turn off notifications" as a blanket step; offer the narrowed version (silence everything except the one channel or caller that must get through).

## Step 2: Audit the six sources

Use `assets/interruption-audit.md`. For each source, get a rough count per day or week and what it costs:

1. **Notifications** (phone, desktop, email banners, app badges)
2. **Chat** (team messaging, group chats)
3. **Email**
4. **Drop-ins** (people at the desk, calls, knocks, children, patients)
5. **Meetings** (scheduled time, plus the time before and after)
6. **Self-interruptions** (the user checking something, switching tasks, "just one quick look")

If the user cannot count, ask them to estimate, or to tally for one day with tick marks on paper, and offer to continue with the estimate now. Do not wait on measurement; label estimates.

Ask at most three questions in total for the whole audit. Prefer: "Which of these six hits you most, and roughly how many times a day?"

## Step 3: Rank by cost

Cost has three parts. Score each source high, medium or low on each:

- **Frequency:** how often.
- **Recovery cost:** how hard it is to get back to the work afterwards (interrupting a hard analytical task costs more than interrupting a form).
- **Controllability:** how much of this the user can change alone, with a request, or not at all.

Rank the sources, top three. Do not invent minutes lost per interruption; use the user's own estimate or say the cost is unmeasured. Studies of interrupted work generally find that resuming takes real effort, but the size varies by task and person, and the skill does not quote a number.

Name the **real source**: often one person, one channel or one recurring meeting accounts for most of it. Say it plainly. Self-interruptions are often a big share and are the only source fully in the user's hands; say so without blame.

## Step 4: Choose countermeasures

Use `references/countermeasures.md`. Pick one to three, matched to the top-ranked sources and the job placement. Pull from: notification batching, Do Not Disturb windows, email and chat batching windows, a maker's schedule, meeting-free blocks, status signals, a team response-time norm, working from a different location.

For each chosen measure, give: what exactly to do, who needs to agree (nobody / a teammate / the manager), the cost to others, and when it backfires. If a measure needs agreement, go to Step 5. If it is solo (batching notifications, a DND window), the user can start today.

Prefer the cheapest measure that hits the top source. Do not stack five at once; that is a new system to fail at.

## Step 5: Write the messages

For anything that needs someone else's agreement, write the actual message, ready to send. Use the templates in `references/countermeasures.md` and fit them to the user's job. A good message is:

- **Short:** three to six sentences.
- **Specific:** names the hours, the channel and the duration.
- **With an offer:** what the user gives in return (a response-time guarantee, an emergency route, a daily check-in, availability at set times).
- **A trial, not a demand:** "for two weeks, then we look at it".
- **Phrased as the team's result:** what gets better for them (faster, better answers), not "I need quiet".

Write one to the manager and, if relevant, one to the team or the main interrupter. Offer a tone choice only if asked. For a manager who may say no, add one line of fallback: the smaller version of the ask.

## Step 6: Set the two-week experiment

One measure, not three. Format:

> **Experiment (two weeks, starting [date]):** [the one measure]. **Measure:** [one number or yes/no the user can note daily, such as uninterrupted blocks completed, or times the chat was checked, or hours of protected time held]. **Review on:** [the date, day 14]. **Keep, change or drop:** decide on that date with what was noted.

Pick the measure that can be tracked in ten seconds a day, on paper if needed. If more than one measure is genuinely required (a norm and a window), say so and keep the tracking to one number.

Tell the user to put the review date somewhere they will see it. Claude cannot remember across chats or remind them; offer to run the review when they come back and paste the numbers.

## Step 7: Hand off by name

- Recurring meetings are the top source: hand off to `meeting-audit` (in the meeting-design set), by name, with a one-line brief of which meetings and why. Do not clean up meetings here.
- The user needs a single focus block now: `start-a-focus-session`.
- The user needs the week laid out around the new protected blocks: `plan-my-week`.

---

## Output

In this order:

1. **Placement:** interruptible, interrupting or mixed, with their words.
2. **The ranked audit:** top three sources with frequency, recovery cost, controllability, and the real source named.
3. **Countermeasures:** one to three, each with what to do, who must agree, and when it backfires.
4. **The messages:** ready to send, plus a fallback ask.
5. **The experiment:** one measure, one number, a review date.
6. **Hand-offs:** by name, if any.
7. **What I had to assume**

The user can keep `assets/interruption-audit.md` filled in as the record, and repeat it at day 14.

---

## Failure modes

**"Just turn off notifications."** Wrong for anyone who must be reachable. Offer the narrowed version.

**Treating all interruptions as bad.** Some interruptions are the job, or are the colleague who needs an answer to ship. Distinguish the ones to defer from the ones to keep.

**Never naming the real source.** If one person or one meeting causes most of the damage, say it and write the message to them. A list of generic tips avoids the real conversation.

**Five measures at once.** One experiment, one measure.

**Messages that sound like demands or like apologies.** Short, specific, with an offer, and a trial period.

**Doing meeting cleanup here.** Count the cost of meetings and hand off to `meeting-audit`.

**Blaming the user for self-interruptions.** Name them as the part under their control, and give a cheap tool (a parking lot, a closed tab, a phone in another room).

**Ignoring the manager's side.** If the manager's job depends on fast replies, a request that ignores this will fail. Include their need in the offer.

**Medicalising.** Interruption and overload are work-design problems here. If the user describes distress beyond work friction, say once, kindly, that a person who can help is worth talking to, and continue with the practical part only if they want it.

---

## What I had to assume

Close with a short list: counts I estimated rather than measured, what the manager expects about response times, whether the role allows protected hours at all, who the main interrupter is if not named, and anything about the user's team or tools I guessed.

---

## Supporting files

- `references/countermeasures.md` - the nine countermeasures, with when each backfires, plus message templates.
- `assets/interruption-audit.md` - the audit table, the ranking, the message drafts and the two-week experiment sheet.
