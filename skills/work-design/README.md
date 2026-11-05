# work design

**Don't pick a skill. Just ask Work Design how you should work.**

Say "work-design", or describe how your week goes, and it looks at what your AI tool already knows about you: the conversation, your notes or memory, a `my-system.md` if you have one, and, only if you say yes, this week's calendar and task list. It notices patterns, then suggests one to three methods, working styles or management practices, each with the reason, an honest evidence label and the skill that runs it. It also tells you what not to change.

It consults; it does not impose. It suggests one thing to try this week, offers the rest for later, and never reads anything you have not agreed to.

The failure this exists to prevent: **generic productivity advice handed to someone whose actual week, role and constraints were never looked at, or a recommendation built on a context the user never agreed to share.**

**Reach for it:** when you do not know what you need, when you lead a team, or when you want a second opinion on how you work. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what it can see. The person and company are invented.*

You type: `work-design. I run a six-person design studio and I'm always behind. Can you look at my week?`

It asks: `I can also look at this week's calendar and task list if they're connected. Want me to?` You say yes.

You get (shortened):

```
Work Design Read

What I looked at: this conversation, this week's calendar, your task list.

What I noticed
1. 23 of your 34 working hours this week are meetings; the longest free
   block is 50 minutes.
2. Seven open tasks have been moved to a later date three times or more.
3. You said the team "keeps re-deciding things".

What I would suggest
Try this week: Meeting-free blocks (Practice only)
  Why: you have no block long enough for the work that keeps slipping.
  First step: put two 2-hour blocks in tomorrow's calendar and decline
  anything that lands on them. Runs with: protect-my-focus.
Later: Decision log (Practice only) for the re-deciding. One line per
  decision, owner and date. Runs with: meeting-close.
Later: One-on-ones (Practice only), since you did not mention any.

What to leave alone: your Friday planning session. It is the one place
the week gets a shared plan.

What I had to assume: I did not read email or chat. "Behind" means
missed dates, not hours worked.
```

---

## What it looks at, and what it never does

| It may use | Only if |
| :--- | :--- |
| What you have said in this conversation | Always |
| Notes or memory your AI tool has already loaded, a pasted `my-system.md` | They are already in context |
| This week's calendar, your task list | You say yes, and your tool exposes them. Read-only, one week |

It never writes, sends, schedules or moves anything while looking. It never saves what it learned without asking. It does not read your email or chat history. It says what it looked at in every Read.

---

## Make it ambient (optional)

If you want Work Design to speak up without being asked, add one line to your AI tool's instructions or memory yourself, for example: *"When I describe how I work and something looks fixable, offer one Work Design suggestion at the end of your answer."* This skill does not write that for you, and it limits itself to one unsolicited suggestion per conversation.

---

## What it does not do

It does not plan your day, review your draft, estimate or unstick anything. It names the skill that does. If your message already says "I'm stuck" or "plan my day", the matching skill answers directly and this one stays out of the way.

---

## What this needs

Nothing. A sentence about your work is enough. The method library in `find-my-method` makes the evidence labels exact but is optional.
