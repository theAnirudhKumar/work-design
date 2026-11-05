# optimize tokens

**Catch the expensive request before it runs, not after the bill.**

The waste is rarely the work itself. It's pasting a whole document when only one section needs a look, re-explaining context from three messages ago, asking for a full rewrite where an edit would do, or sending three messages for what was always one ask. None of it buys better output - it just costs more for the same answer, and each instance feels too small to notice.

This skill watches for that shape of request, named explicitly or not, and flags it before starting. Two gates run first: what quality bar does this output need, and is the task one of the genuinely expensive ones - a full deck, a multi-file analysis, a long article - that can't be made lighter, in which case it says so instead of pretending to trim it. Where trimming is real, it shows the original ask, why it's heavy, a leaner version, what changes, and the quality impact, then waits for a green light.

The failure this exists to prevent: **spending extra tokens for the same answer, without noticing, because the waste was too small on its own to flag.**

**Reach for it:** every day. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it.*

You type: `Here's my whole 80-page handbook [paste]. Give me feedback on all of it.`

You get:

```
What you sent: the full handbook, for feedback on everything.

Why it's heavy: 80 pages go in as input, and the reply has to cover all of them.

Leaner version: "Here is section 4, the leave policy [paste]. What is
unclear or missing for a new hire?" Then repeat per section you care about.

What changes: you review the sections that matter, one at a time.

Quality impact: Minimal. You lose cross-section consistency checks; ask for
those separately on the headings only.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Detect | An expensive request flagged before it runs - a full-document paste, an open-ended ask likely to loop, a full rewrite where an edit would do, repeated context |
| Gate 1: quality check | The output's actual quality bar named - publication-grade, internal draft, or quick reference - before anything gets trimmed |
| Gate 2: complexity check | An honest answer on whether this task can be made lighter at all, said plainly when it can't rather than trimming anyway |
| The rewrite | Original ask, why it's heavy, a leaner version, what changes, and the quality impact - none, minimal, or moderate - shown side by side |
| The confirmation | One flag, one rewrite, one green light - then it proceeds, no lecture |

---

## Who this is for

Anyone working with an AI agent regularly enough that token cost adds up - a large paste that only needed a paragraph, a request repeated across many files that could have been batched, a rewrite asked for when an edit was the actual need. It fires on request or on its own when a task looks like it's about to run expensive.

You don't need a workspace, connectors, or any setup. It works in any chat from the first message.

---

## What this needs

**Minimum:** nothing. It works from the request itself, in any chat.

Missing context never blocks this skill - there's no floor to clear. It reasons from the shape of the request that's already in front of it.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other eight skills):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the optimize-tokens skill from https://github.com/theAnirudhKumar/work-design: copy its skills/optimize-tokens folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/optimize-tokens` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the whole method - it's plain markdown, no other files needed.

---

## What this does not do

- **Not for output that's expensive because the output has to be long.** Writing a new article, a full deck, or a report from scratch carries a real cost, and this skill says so rather than trying to cut it.
- **Not a trim-everything reflex.** Genuinely new context, creative or strategic exploration, and anything external-facing or high-stakes don't get suggested for cutting.
- **Not a lecture.** One flag, one rewrite, one confirmation, then it moves - the user needs a better prompt and a green light, not a talk about token usage.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
