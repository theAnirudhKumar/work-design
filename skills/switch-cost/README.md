# switch cost

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

The decision to leave a tool gets made on the reasons to leave; the cost of actually leaving shows up afterward, when the export turns out to be a PDF nobody can reuse or an integration nobody remembers building stops firing silently. This skill inventories what's actually stored in the tool - content, configuration, integrations, history, other people's access - then checks each item against three separate questions: does it export at all, and in a shape the destination can use (a CSV of contacts is usable, a PDF of a board isn't, and configuration frequently doesn't export at all and has to be rebuilt by hand); what's lost outright with no export path (other people's notification history, the tool's own analytics and audit logs, URLs and embeds that break even after a clean migration); and what the exit terms actually say (notice period, contract minimum, what happens to the data after cancellation). It converts all of that into an hours estimate rather than a dollar figure, since no credible cross-tool cost data exists, and ends on low, conditional, or high switching cost - where, exactly as in before-you-install, a condition has to be a named action, never an attitude.

The failure this exists to prevent: **finding out what you lose on the way out, after you've already committed to leaving.**

Part of the **Tool lifecycle** group in this repository.

## Who this is for

For anyone deciding whether to bring a tool in, keep paying for one, or leave it, without redoing the research from scratch every time.

## What this needs

Works with nothing but the tool's name. Gets better with what is actually stored in it, and the destination tool named, which turns the estimate from a category guess into an answer about this account.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the switch-cost skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/switch-cost,
zip the switch-cost folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/switch-cost`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
