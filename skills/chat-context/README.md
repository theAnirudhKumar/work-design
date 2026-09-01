# chat context

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

Closes a long chat and opens a fresh one without losing anything. Long conversations get expensive because every new message carries the whole history with it - this skill writes a structured handoff when a session ends and reads it back, out loud, at the start of the next one, before doing any work.

The handoff isn't a summary. It captures what a summary drops: decisions made and why, approaches already tried and rejected (so the next chat doesn't re-propose something already killed), open blockers, exact file paths, and any wording that was explicitly approved, quoted verbatim. Where file access exists, it becomes a saved file with a master index so handoffs accumulate into a trail; where it doesn't, the same structure prints as one block to paste forward. Either way, resuming means reading the handoff in full and stating what was loaded and what's next, in three lines or fewer, before touching the actual work.

The failure this exists to prevent: a chat that ends, gets summarized in someone's head, and starts over - re-deciding things already decided, and re-trying an approach the last session already ruled out for a reason nobody now remembers.

Part of the **Working with agents** group in this repository.

## Who this is for

For anyone working alongside an AI agent day to day: deciding what to hand off, carrying context between sessions, and catching an expensive request before it runs.

## What this needs

Works with nothing but nothing, the handoff prints in chat to paste forward. Gets better with file access, which turns handoffs into a saved trail with an index.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the chat-context skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/chat-context,
zip the chat-context folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/chat-context`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
