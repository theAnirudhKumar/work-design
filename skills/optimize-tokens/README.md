# optimize tokens

**Part of [work-design](../../#readme): nine skills, in three categories, for deciding how a piece of work will run before it starts.**

Spots token-heavy requests before they run and proposes a cheaper approach that gets the same answer. Fires on request, or on its own when a task looks expensive.

Part of the **Working with agents** group in this repository.

## Who this is for

For anyone working alongside an AI agent day to day: deciding what to hand off, carrying context between sessions, and catching an expensive request before it runs.

## What this needs

Runs from nothing at all: no extra input improves it.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

> Download the `optimize-tokens` skill from https://github.com/theAnirudhKumar/work-design/tree/main/skills/optimize-tokens, zip the `optimize-tokens` folder on its own, then upload it as a skill in Claude.

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/optimize-tokens`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs all nine skills at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
