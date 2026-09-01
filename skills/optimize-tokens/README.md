# optimize tokens

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

This skill runs two gates before touching anything, in order. Gate 1 asks what quality bar the output actually needs - publication-grade, internal draft, or quick personal reference - because a token-efficient but wrong answer is worse than an expensive correct one. Gate 2 asks whether the task can honestly be made lighter at all: some things (a full deck, a genuine multi-file analysis, a 2,000-word article written from scratch) are expensive because the output itself has to be long, and the skill says so plainly and asks before proceeding rather than forcing a cut that costs quality. Where a request can be trimmed - a whole document pasted in for feedback when one section would do, a full rewrite requested where a targeted edit would work, context re-pasted that was already established earlier in the session - it shows the original, why it's heavy, a leaner rewrite, exactly what got cut, and the quality impact, in that fixed format, every time.

The distinction it holds itself to: **token savings that cost quality are not savings, they're regressions** - this skill eliminates waste, never output.

Part of the **Working with agents** group in this repository.

## Who this is for

For anyone working alongside an AI agent day to day: deciding what to hand off, carrying context between sessions, and catching an expensive request before it runs.

## What this needs

Runs from nothing at all: no extra input improves it.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the optimize-tokens skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/optimize-tokens,
zip the optimize-tokens folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/optimize-tokens`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
