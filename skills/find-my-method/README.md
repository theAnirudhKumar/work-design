# find my method

**Stop trying popular productivity methods at random. Get one that fits how you work, a backup, one to leave alone, and a 7-day trial you can judge.**

There are over a hundred productivity methods, and advice usually treats them all as right for everyone. A method that suits someone who owns their calendar can fail a nurse on rotating shifts, a parent with a school run, or a founder who is interrupted every ten minutes. People fail, then decide they are the problem.

This skill diagnoses your main friction, then gives you a Method Fit Card: one primary method, one backup, one to avoid for now, each with fit reasons tied to what you said and an honest evidence label (Strong, Some, Mixed, Practice only). It then gives a 7-day trial with a scorecard: what to track, what counts as keeping the method, and what counts as dropping it without guilt. It changes at most two things at once.

The failure this exists to prevent: **adopting a popular method that does not fit, failing at it, and concluding the problem is personal.**

**Reach for it:** when you want to get more done and do not know what to try, or when nothing has worked. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The person is invented.*

You type: `I'm a ward nurse on rotating shifts. I start to-do lists and drop them in a week. I want to get more done outside work.`

You get (shortened):

```
Method Fit Card: you

1. What I heard
   Friction: lists fail within a week (forgets things, drops systems)
   Work: rotating shifts, no control over hours (assumed: off days vary)
   Tried: to-do lists. Stopped when the shift pattern changed. (assumed)

2. Primary: Brain dump
   Fit: you said lists die when shifts change. Getting everything out of your head works
   at any hour, and needs no schedule.
   Evidence: Some (library card). Studies on writing down open tasks
   suggest it can ease intrusive thoughts; effects vary by person.
   Watch for: the list is useless if you never look at it.

3. Backup: Two-minute rule (replaces, does not join)
4. Avoid for now: Time blocking
   Your hours change weekly, so blocks would break by Thursday.

5. 7-day trial: capture only, nothing else new. Set your own reminder.
6. Scorecard: days I captured something; things I forgot. Keep it if used
   5 of 7 days. Drop it without guilt if it felt like another chore.
8. Assumed: your off days vary week to week.
```

---

## What it does

| Part | What you get |
| :--- | :--- |
| Friction read | Your main problem, in your words, matched to the ten commonest |
| Primary, backup, avoid | One of each, with fit reasons that quote you |
| Evidence label | Strong, Some, Mixed or Practice only, with one honest sentence |
| 7-day trial | A setup under 10 minutes, one daily action, a day 7 review |
| Scorecard | What to track, what counts as keeping it, what counts as dropping it without guilt |

It asks at most three questions, only when the answer would change the recommendation. Otherwise it drafts and labels its assumptions.

---

## What this needs

**Minimum:** a sentence about what is going wrong.

**Better with:** your kind of work, how much control you have over your time, your constraints, and what you tried before.

**Best with:** the method library in `references/`, which has 137 method cards. Without it, the skill works from general knowledge and marks every evidence label "general knowledge".

It cannot keep time, remember across chats or see your calendar. You set the reminders and keep the scorecard.

---

## Where it hands off

- Explaining one method, or comparing two: `explain-a-method`
- A full setup in your tools: `build-my-system`
- Planning today: `plan-my-day`
- Interruptions, one habit, or life balance: `protect-my-focus`, `build-a-habit`, `balance-my-life`

---

## What this does not do

- **Not a guarantee.** The card is a considered guess. The trial tests it.
- **Not medical advice.** If the problem is exhaustion or distress rather than workflow, it says once that a professional who can help is worth talking to.
- **Not a stack.** It will not hand you five new methods at once.
- **Not a study summary.** Evidence labels come from the library cards; it cites no study or percentage it cannot verify.

---

## Install

As a plugin in Claude Code or Cowork:

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill:

```
Install the find-my-method skill from https://github.com/theAnirudhKumar/work-design: copy its skills/find-my-method folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/find-my-method` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill.

**Or just read it.** `SKILL.md` is the method, `assets/method-fit-card.md` is the template, `assets/trial-scorecard.md` is the scorecard, and `references/friction-guide.md` maps ten frictions to methods.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
