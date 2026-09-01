# estimate from precedent

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

Ask someone how long a piece of work will take and they picture it going well - no interruptions, no rework, nobody waiting on someone else - which is the planning fallacy, not a discipline problem, and it gets corrected by changing what the estimate is built from. This skill writes down that inside-view number first, then pulls two or three ordinary past cases of similar work - not the smoothest one, not the outlier - and asks what they actually took, not what they were estimated to take at the time, since memory of past duration compresses optimistically in the same direction as a fresh guess. It names the gap between the two, states what the inside-view number left out (a review cycle, a dependency, a revision after feedback), and adjusts toward the reference class in proportion to how many comparable cases there were and how consistent they were - landing on a range where the cases varied, not a single number dressed up as more certain than the evidence supports. If nothing comparable exists, it says so and stops rather than inventing a reference class to correct against.

The failure this exists to prevent: **an estimate built entirely from imagining this specific instance going well, when a look at similar past instances would have caught the gap first.**

Part of the **Deciding how work runs** group in this repository.

## Who this is for

For anyone shaping a piece of work before committing time to it: an estimate, a channel choice, or a scope line.

## What this needs

Works with nothing but an inside-view estimate and what the work is. Gets better with two or three ordinary past cases and their actual duration, which is what turns the correction from a guess into a measured gap.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the estimate-from-precedent skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/estimate-from-precedent,
zip the estimate-from-precedent folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/estimate-from-precedent`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
