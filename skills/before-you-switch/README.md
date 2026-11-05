# before you switch

**Find out what breaks before you're already gone.**

The decision to leave a tool gets made on the reasons to leave. The cost of leaving shows up afterward - the export turns out to be a PDF nobody can reuse, or an integration nobody remembers building stops firing silently weeks after cancellation. By then the decision is final and the discovery is just damage.

This skill checks that cost first. It names what's actually stored - content, configuration, integrations, history, other people's access - then checks whether each item exports in a format the destination can use (a CSV of contacts works, a PDF of a project board doesn't), names what's lost outright, estimates the move in hours rather than money since no credible switching-cost dataset exists, and checks the exit terms: notice period, contract minimum, data retention after cancellation. It runs in researched or guided mode, the same distinction `before-you-install` makes, and ends on one of three calls.

The failure this exists to prevent: **finding out what you lose on the way out, after you have already committed to leaving.**

**Reach for it:** every quarter, or whenever the moment comes up. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it.*

You type: `What breaks if I move our team wiki to a markdown notes app?`

You get (shortened; figures invented):

```
Mode: guided. Total: about 9 to 14 hours.
Call: SWITCHING COST WITH CONDITIONS

Stored: 212 pages, 14 automations, 6 shared links, 9 teammates.
Exports: pages as Markdown (usable). Automations do not export: rebuild
by hand. Page history is lost.
Lost outright: page history, comment threads, the 6 shared links.
Hours: reshape pages 3 / rebuild automations 4 to 8 / re-point links 1 /
re-onboard teammates 1 to 2.
Conditions: export the automation rules before cancelling (not included in
the Markdown export); confirm data deletion in writing.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Name what's actually stored | Content, configuration, integrations, history, and other people's access - the inventory everything else checks against |
| Check what exports, and in what shape | Whether each item exports at all, in a usable format, and whether the named destination can actually import it |
| Name what's lost outright | A plain list of what has no export path under any format - separate from what merely takes work to move |
| Estimate the move in hours | Built from the specific inventory found, or from the reader's own past migration, never from a category-wide guess |
| Check the exit terms | Contract minimum, cancellation notice, and what happens to the data after cancellation |
| The call | Low switching cost, switching cost with conditions, or high switching cost - with conditions written as actions |

---

## Who this is for

Anyone weighing a move between two tools, or checking the exit cost on a tool a `audit-my-tools` already marked for cancellation, before anyone acts on that verdict. It's for what happens on the way out - not whether to leave (`audit-my-tools`) and not whether to adopt something new in the first place (`before-you-install`).

You don't need to be technical. The tool's name is enough to start, and it works from a chat window with or without web access.

---

## What this needs

**Minimum:** the tool's name. Nothing else - it tells you what to go check and marks every gap it couldn't fill.

**Better with:** what's actually stored in it - content, configuration, integrations, history, other people's access. A general answer about a category of tool isn't the same as an answer about this one, in this state.

**Best with:** the destination named. Switching cost isn't a property of the tool being left - it's a property of the gap between the tool being left and the tool being moved to. "What breaks if I leave Notion" is a weaker question than "what breaks if I move from Notion to Obsidian," and only the second one has a real answer.

Missing context never blocks this skill. Without web access it runs in guided mode - handing you the exact export page, cancellation terms and account settings to check - and names every check it couldn't run.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other eight skills):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the before-you-switch skill from https://github.com/theAnirudhKumar/work-design: copy its skills/before-you-switch folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/before-you-switch` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/evidence.md` explains why the skill argues from mechanism rather than a statistic, and `assets/exit-checklist.md` is the checklist it fills in and hands over.

---

## Where this comes from

This skill deliberately does not cite a switching-cost statistic, and `references/evidence.md` documents why: two sources were checked directly while writing it - Zylo's own SaaS statistics roundup, which contains no figures on lock-in or migration time, and an industry piece claiming specific migration-hour figures with no disclosed source or methodology, read as opinion rather than measurement and not used. No credible, sourced dataset on SaaS switching cost was found anywhere in that pass. So Step 4 builds its hours estimate from the specific inventory the skill itself gathers, or from the reader's own past migrations, instead of a borrowed industry number - a weaker-sounding claim, and the only one that survives being checked.

---

## What this does not do

- **Not a migration guide.** It names what breaks and what it costs. It doesn't walk through the mechanics of the move itself.
- **Not a renegotiation skill.** Whether to leave, or what to pay to stay, is `audit-my-tools`'s job or a direct conversation with the vendor.
- **Not legal advice.** Data-retention and contract-term findings are reported from what the terms say. Anything contractual or regulated goes to someone qualified.
- **Not a guarantee.** A low-switching-cost call means nothing found in this check makes leaving expensive. It doesn't mean nothing will go wrong in the move itself.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
