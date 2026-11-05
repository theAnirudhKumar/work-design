# what could go wrong

**Assume the plan already failed, then say why.**

Ask "what could go wrong?" and people give polite, generic answers: scope creep, timeline slip, stakeholder buy-in. None of them are wrong and none of them change what anyone does on Monday. A pre-mortem asks a different question. It is the date the work was due, it has failed, and you have to explain why. That framing makes the uncomfortable explanations easier to say, and it forces them to be specific to this plan.

This skill takes a plan and works backwards from a dated failure. It writes 5 to 7 causes that could only belong to this plan, spread across internal, external, people and assumptions. Each gets an early-warning signal you could actually see by a date, a pre-committed "If X by Y, then Z" response, and the cheapest thing to do about it now. Then it names the one assumption that, if wrong, sinks the work, gives you a test of it that runs this week, and ends on a verdict: proceed, proceed with changes, or re-plan. If the plan is too thin to be specific, it asks at most two questions rather than hand back generic risks.

The failure this exists to prevent: **a plan that goes ahead carrying a fatal assumption nobody examined, because the review asked for "risks" and got the generic list instead of the specific thing that would sink it.**

**Reach for it:** before committing to any plan, launch, hire, migration or decision you cannot easily undo. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The company, people and plan are invented, and the exact output varies with what you give it.*

You type:

```
Pre-mortem this: Brightwell Clinics plans to move all appointment reminders
from phone calls to text messages by 31 January. Two staff run the project
part-time. The text vendor needs patient consent on file first.
```

You get (shortened):

```
It is 1 February. The move has failed: calls were switched off and
no-shows went up.

1. People: Front-desk staff kept calling patients "to be safe", so
   patients got both and ignored both.
   Signal: call log still shows reminder calls on 10 Jan.
   If reminder calls are still logged on 10 Jan, then the clinic manager
   removes the call script from the desk. Prevention: tell the desk now
   that calls stop on a named date.
2. External: The vendor's consent check rejected patients whose consent
   was on paper only.
   Signal: under 60 percent of the patient list shows as consented on
   10 Jan. ...
[causes 3 to 6 omitted]

The one assumption: patients will read texts from a number they do not
recognise. Test this week: text 20 patients from the vendor's number and
count replies by Friday.

Verdict: proceed with changes. Do the consent audit before anything else.
Assumed: "all reminders" means appointment reminders only, not billing.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Check there is enough | If the plan is too thin to be specific, at most two questions, then it runs on stated assumptions |
| Set the failure | A dated, plain statement of what failed, in the past tense |
| Generate 5 to 7 causes | Specific to the plan, with at least one each from internal, external, people and assumptions |
| Make each usable | A dated early-warning signal, an if-then response with a named owner, the cheapest prevention now |
| Rank in plain words | Likely or unlikely, survivable or fatal, one line of reasoning each, no invented percentages |
| Name the one assumption | The sentence that could be false, and a cheap test that can run this week |
| Give the verdict | Proceed, proceed with changes (listed), or re-plan |
| Say what it assumed | What the plan did not say, and what the skill could not know |

There is also a group mode: a short script for running it with a team, with silent writing first, then pooling, then ranking, so the loudest voice does not set the list.

---

## Who this is for

Anyone about to commit to something that is hard to reverse. A product launch, a grant application timeline, a contractor hire, a data migration, a wedding, a clinic process change, a research study, a fundraising push, a house renovation. The method does not depend on the field. It depends on the plan having enough in it to be specific about.

You do not need a project tool or a team. A few sentences describing the plan are enough to get a real pre-mortem out of it.

---

## What this needs

**Minimum:** the plan, in a few sentences. Goal, rough timing, who is involved.

**Better with:** the date it must finish, what success looks like, and the one or two things you are already worried about.

**Best with:** what happened the last time something like this was tried, and who the plan depends on.

Missing context never blocks this skill. It either asks up to two questions or runs on stated assumptions and marks which causes rest on them.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the rest of the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the what-could-go-wrong skill from https://github.com/theAnirudhKumar/work-design: copy its skills/what-could-go-wrong folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/what-could-go-wrong` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, and `assets/pre-mortem-sheet.md` is the fill-in table.

---

## Where this comes from

The method is Gary Klein's project premortem, written up in Harvard Business Review in 2007. The "If X by Y, then Z" responses are implementation intentions, from Peter Gollwitzer's 1999 work on how specifying when and where you will act makes acting more likely.

One honest caveat. The support for the technique comes mostly from practice and from related research on prospective hindsight and if-then planning. It has not been tested in trials that measure knowledge-work outcomes. Treat it as a cheap, structured way to make people say what they already suspect, not as a proven predictor of what will fail.

---

## What this does not do

- **Not a review of finished work.** For a draft, memo or deliverable, use `review-my-work`. This is for plans that have not happened yet.
- **Not the framing.** `plan-the-work` writes down what the work is and its biggest risk. This skill takes that risk line and stress-tests the whole plan.
- **Not sizing or estimating.** `fit-to-deadline` fits scope to a time budget and `how-long-will-it-take` corrects a time guess.
- **Not a probability forecast.** It ranks in words. It will not give you a percentage chance of failure, because there is no honest one.
- **Not a guarantee.** It surfaces what the people involved can imagine. It cannot find what none of them know.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
