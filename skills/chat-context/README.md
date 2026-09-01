# chat context

**Part of [work-design](../../#readme): nine skills, in three categories, for deciding how a piece of work will run before it starts.**

Carries context between chats. Handoff mode writes a structured context file when a session ends; resume mode reads it back and states what was loaded before doing any work.

Part of the **Working with agents** group in this repository.

## Who this is for

For anyone working alongside an AI agent day to day: deciding what to hand off, carrying context between sessions, and catching an expensive request before it runs.

## What this needs

Works with nothing but nothing, the handoff prints in chat to paste forward. Gets better with file access, which turns handoffs into a saved trail with an index.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the chat-context skill from https://github.com/theAnirudhKumar/work-design/tree/main/skills/chat-context, zip the chat-context folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/chat-context`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs all nine skills at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
