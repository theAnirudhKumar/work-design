# fit to deadline

**Fix the time. Shrink the work to fit. Decide the cuts before the deadline does.**

When time is fixed, the work has to give. Most people let it give by accident: everything moves at the same pace until the deadline is close, then the last third is cut in a panic, in whatever order it falls. The part that mattered most is often the part that got dropped, because it was last on the list.

This skill starts from the time budget, not from the work. Give it the work, the outcome it has to achieve, and the time available (or a deadline, which it converts into working hours). It builds a ladder of three versions: a Minimum, which is the smallest thing that still delivers the outcome, with a line on why it still counts; a Target that fits the time with room to spare; and a Stretch that gets added only if things go well. It ranks what to cut, first to last, by least outcome lost per hour saved, and says in plain words what each cut costs. It writes a decision rule for the middle of the work, pinned to a calendar date, so no one decides under pressure. And it names the risk that the Minimum is too thin, with a cheap early check.

It also works the other way. If the work is smaller than the time, it says so, and suggests raising the quality bar or stopping early, rather than letting the work swell to fill the space.

The failure this exists to prevent: **a fixed deadline with no decision about what goes first, so the cuts are made in the last hours by whatever is left, and the part that mattered most is the part that got dropped.**

**Reach for it:** whenever the time is set and more is wanted than fits. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it. The project and people are invented.*

You type: `I have until Friday noon to put together a hiring plan for the two new support roles. It's Wednesday morning.`

You get (shortened):

```
Time: about 10 working hours, assumed: Wed 4, Thu 5, Fri 1 before noon.
Outcome (assumed): the support lead can approve a hiring plan on Friday.

Minimum (6 h): role descriptions for both roles; a posting channel and a
  budget line; a 4-step interview process. Still counts: the lead can say
  yes or no to a concrete plan.
Target (8 h): Minimum, plus a scoring sheet for interviews and a 30-day
  onboarding outline.
Stretch (10 h): a sourcing list of communities and referral asks.

Cut first to last:
 1. Sourcing list (2 h)    cost: you will rely on the usual job boards
 2. Onboarding outline (2 h)  cost: the new hires arrive with no plan for
                              week one, fixable after approval
 3. Scoring sheet (1 h)    cost: interviews are less comparable; the lead
                              may ask how you will rank people

Midpoint rule: Thursday 10:00, if both role descriptions are not drafted,
  drop the onboarding outline and work to the Minimum.

If the Minimum is too thin: the lead asks "how will we choose between
  candidates?" Check: send the interview process to the lead on Wednesday
  evening with one question, "is this the right number of rounds?"
  If not, the scoring sheet moves back into the Minimum.

Assumed / could not check: the budget figure exists; the hours per day.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Fix the inputs | The work, the outcome, and the time as working hours, with the conversion from a deadline shown |
| Treat time as fixed | The budget is the constraint and the scope moves, not the other way round |
| Weigh the parts | Each part sized (marked as a guess where it is one), and tagged essential, helps or polish |
| Build the ladder | Minimum (with why it still counts), Target, Stretch, each with hours against the budget |
| Rank the cuts | What to drop first, by least outcome lost per hour saved, with the cost of each cut in plain words |
| Midpoint rule | "At [date], if [observable] is not done, cut [item]". A calendar point, not a feeling |
| Check the Minimum | The risk that it is too thin, and a cheap early check |
| The inverse | If the work is smaller than the time, a choice of raising the bar, stopping early, or adding one named part |

If even the Minimum does not fit, it says so first and gives the reason, then offers the options: a smaller outcome, more time, or more hands. It never quietly stretches the deadline or squeezes the Minimum.

---

## How it differs from its neighbours

| Skill | Starts from | Produces |
| :--- | :--- | :--- |
| **fit-to-deadline** | The time budget | A ladder of versions to fit it, a ranked cut list, a midpoint rule |
| `scope-the-work` | A defined job | A boundary note: in, out, done, who moves the line |
| `how-long-will-it-take` | An estimate | A duration corrected against how long similar work took |
| `plan-the-work` | A task with no outcome yet | A one-page card at the start of the work |

---

## Who this is for

Anyone with a deadline and more work than fits: a launch date, a grant application, a lab report, a client deck, a conference talk, a house move. Nothing in the method depends on the field.

You do not need a workspace, a connector or a file. The work, the outcome and the time, typed in a chat, are enough.

---

## What this needs

**Minimum:** the work and the time available.

**Better with:** the outcome the work must achieve and who it is for. The Minimum is only honest against a stated outcome. If you do not give one, the skill writes it and marks it as an assumption.

**Best with:** a rough list of the parts and any that someone else is waiting on.

The one thing it will ask for, once, is the time. Everything else it assumes and labels.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the fit-to-deadline skill from https://github.com/theAnirudhKumar/work-design: copy its skills/fit-to-deadline folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/fit-to-deadline` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, and `assets/sizing-ladder.md` is the template the skill fills in, with a filled example from an invented project.

---

## Where this comes from

**Fixed time, variable scope** is the appetite idea from Basecamp's Shape Up (Ryan Singer). The skill borrows it directly: the time is decided first, and what goes in is what fits.

**Parkinson's law** is cited only as a named observation, that work tends to expand to fill the time available. It is the reason to set a budget instead of leaving the time open. The skill puts no figure on it.

The hours in any ladder are the user's own, or marked as guesses. The skill quotes no typical durations.

---

## What this does not do

- **Not a boundary note.** Drawing in, out and done around a defined job, often with a requester, is `scope-the-work`.
- **Not a duration estimate.** Checking a guess against how long similar work took is `how-long-will-it-take`.
- **Not a start-of-work card.** If there is no outcome yet, `plan-the-work` comes first.
- **Not a way to make a deadline longer.** It extends time only as an option it states plainly, when the Minimum cannot fit.
- **Not a guarantee.** A filled ladder means the cuts were decided in advance. It does not mean the work will fit.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
