# delegate

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

Most delegation advice sorts tasks by whether a model is capable of doing them - the wrong sort, since a model can produce plenty of things nobody in the room can actually check, and those are the ones that come back wrong at delivery. This skill splits one piece of work by the kind of thinking each part needs (gathering, deciding, producing, checking), not by the order things happen in, then runs each part through four tests in order: can the user say what correct looks like, does it need context that was never written down, how expensive is an unnoticed error, and does doing this part keep the user good at their job. Every part that leaves the user's hands leaves with a named check, a stop condition, and what's lost if the check gets skipped - and the marginal-case rule is explicit: if the check costs more to run than the part costs to do, it doesn't get delegated. It ends on a filled allocation table, never bare advice.

The failure this exists to prevent: **handing over the part you cannot verify, and finding out at delivery.**

Part of the **Working with agents** group in this repository.

## Who this is for

For anyone working alongside an AI agent day to day: deciding what to hand off, carrying context between sessions, and catching an expensive request before it runs.

## What this needs

Works with nothing but a description of the work. Gets better with what the output is for and who sees it, which is what sets how hard the checks have to be.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the delegate skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/delegate,
zip the delegate folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/delegate`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
