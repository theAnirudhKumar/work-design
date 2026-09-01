# chat context

**Close a chat without losing what it knows.**

Long conversations get expensive because every message drags the whole history behind it. The fix is a fresh chat - but re-explaining from memory is where it goes wrong: the new chat re-decides something already settled, or re-tries an approach the last session already killed, because the only record was a scrollback nobody reread.

This skill writes the record instead. Ending a chat produces a structured handoff, not a summary: decisions and their reasoning, approaches already tried and killed, open blockers, exact file paths, and any wording explicitly signed off on, quoted verbatim. With file access it's saved with a master index, building a trail; without it, the same structure prints as one copyable block. Resuming means reading the handoff in full before touching the work, then stating in three lines or fewer what loaded and what's next.

The failure this exists to prevent: **a chat that ends, gets summarized in someone's head, and starts over - re-deciding things already decided, and re-trying an approach the last session already ruled out for a reason nobody now remembers.**

Part of the **Working with agents** group in [work-design](../../#readme).

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Identify the project area | The right place for this handoff to live, or a short topic label when there's no workspace to route into |
| Write the handoff | A fixed structure - goal, current state, decisions made, open blockers, files touched, rejected approaches, approved wording, next action - filled in even where the honest answer is "none" |
| Register it | A master index row (file route only), so a later "resume" can find the right handoff without you carrying it |
| The paste-ready opener | One line to drop into the new chat, or the handoff block itself when there's no file route |
| Resume: find it | The named topic, the most recent active handoff, or a question rather than a guess if two could plausibly match |
| Resume: state what loaded | Which handoff was read, which files came with it, and the recorded next action - three lines, before any work starts |

---

## Who this is for

Anyone working alongside an AI agent day to day, across more than one session - closing a chat that's gotten long or expensive, and picking the next one up without re-litigating what the last one already settled.

You don't need a workspace, a `CLAUDE.md`, or file access for this to work. In a plain chat with nothing connected, the handoff just prints as a block you copy forward - that's the whole loop, and it's a complete answer, not a fallback.

---

## What this needs

**Minimum:** nothing. The handoff prints in chat as a block to paste into the next one.

**Better with:** somewhere to write files. The handoff becomes a saved file with a master index, so handoffs accumulate into a trail and resume can find the right one on its own.

Missing context never blocks this skill - the handoff's structure is identical either way, only where it lands changes.

---

## Install

**The easy way: one paste**

```
I want to install the chat-context skill from
https://github.com/theAnirudhKumar/work-design. Download or clone the
repository, then copy the skills/chat-context folder into
~/.claude/skills/ (or .claude/skills/ if this is for one project only),
keeping its own folder name. Tell me the exact folder path it landed in
when you are done.
```

**In the Claude app (no terminal needed)**

1. Download this repository as a ZIP, or clone it
2. Zip the `skills/chat-context` folder on its own
3. In Claude, go to Customize, then Skills, then Create skill, then Upload skill
4. Upload the ZIP

**As a plugin, in Claude Code or Cowork**

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

**Want the whole set?** The [main README's install section](../../#readme) installs all 9 skills at once.

**Or just read it.** `SKILL.md` is the whole method - it's plain markdown, no other files needed.

---

## What this does not do

- **Not a substitute for `MEMORY.md`.** A handoff is session state, not durable memory. Anything that outlives this one thread of work gets proposed as a memory entry separately, not folded into the handoff.
- **Not for a short chat where nothing was decided.** Say so and skip the file rather than writing a handoff with nothing in it.
- **Not a transcript.** No dialogue, no blow-by-blow, no reasoning that led nowhere. Just what the next chat actually needs to act.
- **Not a conversational recap.** A request to summarize the chat back to the user gets a summary, not a handoff - the two are different jobs.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
