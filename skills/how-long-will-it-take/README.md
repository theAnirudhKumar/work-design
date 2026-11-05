# how long will it take

**Correct the estimate against what actually happened last time, not against how this time feels.**

Ask someone how long a piece of work will take and they picture it going well - no interruptions, no rework, no waiting on someone else's sign-off. That's not dishonest, it's the wrong question. The right one is how long the last several things like this actually took, including the parts that didn't go well, because those parts show up again almost every time.

This skill writes down the gut number first, then asks for two or three ordinary past cases - not the smooth one, not the disaster - and pulls their actual duration, not the estimate given for them at the time. It puts the two numbers side by side, names the gap and what the fresh estimate likely missed, and adjusts toward the reference class in proportion to how many cases there were and how consistent they were. With nothing comparable to check against, it says so and stops rather than inventing a reference class.

The failure this exists to prevent: **an estimate built entirely from imagining this specific instance of the work, when a look at similar past instances would have caught the gap before it became a missed deadline.**

**Reach for it:** every project. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it.*

You type: `I think the website migration is 2 days. Sanity check?`

You get:

```
Inside view:  2 days
Reference cases (you told me):
  blog migration     4 days actual
  docs migration     5 days actual
  landing page move  3 days actual

Gap: 2 days against 3 to 5. All three cases included a redirect pass and
one review round; the 2-day picture has neither.

Adjusted: 3 to 5 days, leaning 4. Three cases is thin: treat this as a
range, not a promise.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Get the inside-view estimate | The gut number, written down before anything else, so the size of the correction is visible later |
| Build the reference class | Two or three ordinary past cases - similar work, scope, and people - never the best case or a forced comparison |
| Get what those cases actually took | Actual duration, not the estimate given for them at the time, because memory of past duration compresses toward the plan the same way a fresh estimate does |
| Compare and name the gap | The inside-view number next to the reference-class number, and what the fresh estimate likely left out - a review cycle, a dependency, a revision after feedback |
| Adjust and give the range | A corrected estimate weighted toward the reference class, with an honest range rather than a single number dressed up as more certain than the input supports |

---

## Who this is for

Anyone who has to give or check a time estimate and has been burned by "this should only take a day" before - a scope-the-work note or a delegate allocation that needs a real number attached, a team that always runs over on a certain kind of task and wants to know why, or a single estimate someone wants sanity-checked before it goes into a plan.

You don't need a project tracker or logged hours to start. Even roughly remembered past cases move the number in the right direction; exact logs just move it further.

---

## What this needs

**Minimum:** the estimate someone has already made or is about to make, and what the work is.

**Better with:** two or three past instances of similar work and how long they actually took, even roughly remembered.

**Best with:** actual logged time or dates from those past instances rather than memory, since memory of past duration is itself optimistic in the same direction as the fresh estimate.

Missing context never blocks this skill outright, but it changes what it can honestly claim - without a real reference class, it says so rather than estimating from nothing.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other eight skills):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the how-long-will-it-take skill from https://github.com/theAnirudhKumar/work-design: copy its skills/how-long-will-it-take folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/how-long-will-it-take` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/evidence.md` is the research citation behind it, and `assets/precedent-worksheet.md` is the one-page fill-in template - inside-view estimate, reference cases, the gap, the adjusted range.

---

## Where this comes from

Two established findings, both named rather than paraphrased in `references/evidence.md`. **The planning fallacy** - Buehler, Griffin & Ross, *Journal of Personality and Social Psychology*, 1994 - found that people underestimate task duration even with direct experience of similar tasks running long, because the estimate is built from an idealized "inside view" of this instance rather than the outcome of comparable past ones, and that simply knowing about the bias does not correct it. **Reference class forecasting** - most associated with Flyvbjerg's later work applying the same inside-view/outside-view distinction to infrastructure and IT project forecasting - is the corrective: build the estimate from a class of genuinely comparable past cases instead of reasoning about the specific case alone. This skill's reference-class step is a direct, much smaller-scale application of that method to a single piece of work rather than a portfolio of projects. No claim in the skill rests on a specific statistic from either paper - the citation is for the mechanism, not a number to quote.

---

## What this does not do

- **Not a cost estimate.** This is time and effort; a dollar figure built the same way would need its own reference class of costs, not durations.
- **Not a decision about whether the work should happen or who should do it.** `scope-the-work` and `delegate` answer those, and either can hand a number here to check.
- **Not usable without a real reference class.** It says so rather than estimating from nothing.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
