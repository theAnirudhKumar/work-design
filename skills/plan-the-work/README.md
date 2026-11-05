# plan the work

**Never start non-trivial work without one page that says what it is for, what done looks like, and what to do first.**

Most work that goes wrong was wrong at the start. The task arrived as a topic ("the Q3 report", "the wedding", "the export feature"), and the first hours went to whatever was easiest to begin. Nobody had said who it was for, what finished looked like, or what to leave alone. By the time that showed, the time was spent.

This skill turns a task into a one-page Work Card before the work begins. It does not interview you first. It drafts the whole card from one sentence, marks every guess as an assumption, and asks at most three questions at the foot, only if the answer would change the card. The card has an outcome you could observe, who it is for and what they will do with it, why now, an appetite (the time this deserves, decided up front), three checkable done criteria and one line on what excellent looks like, an explicit out-of-scope list, the biggest risk with an if-then tripwire, who or what helps, a first move under 30 minutes, and what had to be assumed.

The failure this exists to prevent: **starting non-trivial work with no stated outcome, audience or definition of done, so effort goes to the wrong thing and nobody can tell when to stop.**

**Reach for it:** at the start of anything that will take more than about half an hour. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it. The people and company are invented.*

You type: `I have to run the customer survey for Brightwell Cycles. I don't know where to start.`

You get (shortened):

```
Work Card: Brightwell Cycles customer survey      (full card, assumed 2 to 3 days)

1. Outcome
   By Friday, the owner has a one-page summary of what 100 or more customers
   say about delivery times, and a yes/no on whether to change courier.

2. For whom, and what they will do with it
   The owner. She will decide on Monday whether to keep the current courier.

3. Why now
   The courier contract renews at month end. (assumed)

4. Appetite
   Up to 10 hours, because a courier change is worth a survey but not a study.
   At the limit: report the replies in, with the response count stated.

5. Done looks like
   - Survey sent to the full customer list, with a test send checked on a phone
   - At least 100 replies, or a stated reason if fewer
   - One page that answers "change courier: yes, no, unclear" in its first line
   Excellent: the owner quotes a customer's words in the Monday meeting.

6. Out of scope
   Pricing questions. Website feedback. A repeat survey next quarter.

7. Biggest risk, and tripwire
   Too few replies. If under 40 replies by Wednesday noon, send one reminder
   and add a text-message nudge to the 30 most recent customers.

8. Who or what helps
   Question draft: AI, you edit. Send and monitor: you. List export: ask Sam.

9. First move
   Today, 20 minutes: write the single decision question ("should we change
   courier?") and the three questions that would change the answer.

10. What I had to assume
   - About 400 customers on the list (changes the reply target)
   - The survey tool is already available (not checked)
   - The renewal date (not checked)

Questions: Is there a hard date from the courier? (changes line 4)
Next, if useful: `what-could-go-wrong` on the plan before you send.
```

Four more cards from unrelated fields are in [`assets/worked-examples.md`](assets/worked-examples.md): a product launch, a lab experiment, a legal memo and a wedding, plus three 5-line cards.

---

## What it actually does

| Section | What you get |
| :--- | :--- |
| Outcome | One sentence a stranger could check, instead of an activity like "work on the report" |
| Who it is for | The person and the action they will take, which sets the quality bar |
| Why now | What waiting costs. If nothing, the card says so and the appetite shrinks |
| Appetite | The time this deserves, decided up front, with what happens at the limit |
| Done looks like | Three criteria a third party could verify, and one line on what excellent looks like beyond done |
| Out of scope | The adjacent things you might assume are included, named |
| Biggest risk and tripwire | One risk, and an if-then with a date: "If X by Y, then Z" |
| Who or what helps | Alone, a named person, or an AI, per part |
| First move | One action under 30 minutes you can begin without deciding anything else |
| What I had to assume | Every guess, and what could not be checked |

---

## The depth dial

| The work is | The card is |
| :--- | :--- |
| About 30 minutes or less | No card. You get the first move only |
| Up to about 2 hours | 5 lines: outcome, done, out, first move, assumed |
| Half a day to several days | The full card above |
| Weeks, or several people | A full card for the whole, then a separate card for the first stretch |

It also skips the card when the task is already fully specified. If outcome, audience, done condition and deadline are all in your message, it says what is covered and adds only the risk and the first move.

---

## Who this is for

Anyone starting a piece of work in any field: a marketing launch, a lab experiment, a legal memo, a wedding, a thesis chapter, a software feature, a sales proposal. Nothing in the card assumes an industry. The same ten lines work because every kind of work has an outcome, an audience, a stopping point and a first step.

You do not need a workspace, a connector or a file. A sentence typed into a chat is enough.

---

## What this needs

**Minimum:** the task described in a sentence.

**Better with:** the deadline, who it is for, and the message from whoever asked for it, pasted as written.

**Best with:** a past piece of similar work and how it went, so the risk line names a real risk.

Missing context never blocks this skill. It drafts the card anyway and lists what it had to assume.

---

## Where the card hands off

The card stands alone. If the matching skill is installed, it names the next step in one line:

- The appetite does not fit the deadline: `fit-to-deadline`
- A plan worth stress-testing before you start: `what-could-go-wrong`
- A requester who keeps adding to the request: `scope-the-work`
- Work that includes handing a part to an AI or another person: `delegate`
- You want a realistic duration, not a budget: `how-long-will-it-take`

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the plan-the-work skill from https://github.com/theAnirudhKumar/work-design: copy its skills/plan-the-work folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/plan-the-work` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `assets/work-card.md` is the fill-in template, and `assets/worked-examples.md` holds filled cards from seven fields.

---

## Where this comes from

**Appetite** is borrowed from Basecamp's Shape Up (Ryan Singer): decide the time the work is worth first, then let the scope flex to fit, instead of estimating the scope and discovering the time afterwards.

**The tripwire and the first move** are written as if-then plans because of research on implementation intentions (Gollwitzer, 1999), which found that people follow through on an intention more reliably when they decide in advance when and where they will act.

**Naming the audience and what they will do with the work** reflects a long line of work design research, which treats knowing who your work affects as part of what makes work well designed (see Parker, Morgeson and Johns, 2017, for a review).

The skill states no figures for how much time a card saves. None is claimed.

---

## What this does not do

- **Not a project plan.** It is the first page of the work. It does not schedule tasks or track progress.
- **Not a boundary note with a requester.** If you and a requester disagree on what is in, that is `scope-the-work`.
- **Not a time-box fix.** If the card shows the work does not fit the time, `fit-to-deadline` shrinks it.
- **Not an estimate.** The appetite is a decision. A realistic duration is `how-long-will-it-take`.
- **Not a guarantee.** A filled card means the start was decided on purpose. It does not mean the work will go well.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
