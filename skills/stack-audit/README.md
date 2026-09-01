# stack audit

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

Subscriptions are the easiest spend in a budget to lose track of because the bill is the only thing that recurs - the decision to keep paying doesn't recur unless something forces it to, and this skill is that force. It builds its inventory from an actual statement or subscription export where one exists, because memory reliably omits exactly the tools nobody opens, then groups tools by the one-phrase job each was actually hired to do rather than by vendor category - the check that catches two "project management" tools doing different jobs, and two tools in unrelated categories quietly doing the same one. Every row gets exactly one of four verdicts (keep, cancel, downgrade, consolidate) with a stated reason, never a bare guess, and the total amount a cancel, downgrade or consolidate verdict would free up leads the output before the table does. It closes with a recheck date three to six months out, because an audit run once and never repeated drifts straight back to the state that made the first one worth running.

The failure this exists to prevent: **paying every month for a decision made once, on a tool nobody has opened since, because nobody put a date on revisiting it.**

Part of the **Tool lifecycle** group in this repository.

## Who this is for

For anyone deciding whether to bring a tool in, keep paying for one, or leave it, without redoing the research from scratch every time.

## What this needs

Works with nothing but a list of tool names from memory. Gets better with a card statement, bank export or subscription list pasted in, which turns last use from a guess into a fact.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the stack-audit skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/stack-audit,
zip the stack-audit folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/stack-audit`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
