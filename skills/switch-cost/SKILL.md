---
name: switch-cost
description: >
  Checks what breaks before you leave a tool: what exports and in what
  format, what is lost outright, and what the move actually costs in
  hours. Trigger when the user says "what happens if I leave this tool",
  "what breaks if I switch", "should I switch from X to Y", "how locked in
  am I", "can I get my data out of", "before I cancel", "before I migrate
  off", or names two tools and asks about moving between them. Also
  trigger when a stack-audit verdict of cancel, or a before-you-install
  decision between two tools, needs the actual exit cost checked before
  anyone acts on it. Ends on a verdict: low switching cost, switching cost
  with conditions, or high switching cost, naming what makes it so. Use
  before-you-install for a tool not yet adopted, and stack-audit to decide
  whether a tool should be cancelled in the first place; this one is for
  what happens after that decision, on the way out.
---

# Switch Cost

The decision to leave a tool gets made on the reasons to leave. The cost of actually leaving shows up afterward, when the export turns out to be a PDF nobody can reuse, or the integration nobody remembers building stops firing silently.

The failure this exists to prevent: **finding out what you lose on the way out, after you have already committed to leaving.** Not whether to leave. What leaving actually costs, named before the decision is final rather than discovered during the move.

---

## What this needs

**Minimum: the tool's name.** Nothing else. It will tell you what to go and check, and mark every gap it could not fill.

**Better with** what is actually stored in it: content, configuration, integrations, history, other people's access. A general answer about a category of tool is not the same as an answer about this one, in this state.

**Best with** the destination named. Switching cost is not a property of the tool being left; it is a property of the gap between the tool being left and the tool being moved to. "What breaks if I leave Notion" is a weaker question than "what breaks if I move from Notion to Obsidian," and the second is the one with a real answer.

### Two modes, and say which one you ran

**Researched mode.** Web access is available. Check the tool's actual export documentation, its stated data-retention policy after cancellation, and its contract or terms for notice periods and minimum terms.

**Guided mode.** No web access. Hand over the exact things to check: the export or data-portability page, the cancellation terms, and the account settings screen that shows what the tool actually holds. Take back what the reader finds, and read that.

Name the mode in the first line of the output, for the same reason `before-you-install` does: a guided answer and a researched one look identical unless the skill says which it gave.

---

## Step 1: Name what is actually stored

Before anything else, list what is in the tool, in the reader's own words: the content itself, configuration and custom setup, integrations and automations that depend on it, historical data (analytics, logs, version history), and other people's access to it (shared links, team seats, things other people were notified through).

This list is what Steps 2 through 4 check against. A switching-cost answer with no inventory behind it is a guess wearing a verdict.

## Step 2: Check what exports, and in what shape

For each item in the Step 1 inventory, check whether it exports at all, and if so, in a format the destination can actually use, or only as a backup nobody will reopen. A CSV of contacts is usable. A PDF of a project board is not. Configuration and automations frequently do not export at all and have to be rebuilt by hand; say so plainly where that is the case rather than assuming it under a general "data export" claim.

Where the destination has been named, check whether it has an import path for what actually exported. An export with nowhere to land is not a migration, it is an archive.

## Step 3: Name what is lost outright

Some things do not export under any format: other people's notifications and their history of interacting with the content, the tool's own analytics and usage history, anything tied to the account rather than the content (SSO logs, audit trails), and URLs or embeds that point at content living inside the tool, which break wherever they were shared even after a successful export elsewhere.

State this as a plain list, not folded into the export check. A reader deciding whether to leave needs to see what is simply gone, separately from what merely takes work to move.

## Step 4: Estimate the move in hours, not money

Time is the honest unit here; no credible dataset exists on switching-cost dollar figures across tools; see `references/evidence.md`. Build the estimate from what Steps 1 through 3 actually found: rebuilding each lost integration or automation, re-inviting and re-training anyone who used the tool, and re-pointing anything that linked to content now moved. Where the reader has done a comparable migration before, ask what that one took and use it as the reference point rather than guessing from the tool's category.

## Step 5: Check the exit terms

Contract minimum term, cancellation notice period, and what happens to the data after cancellation: deleted immediately, retained for a window, or retained indefinitely unless deletion is requested. This last one matters most for anything under a confidentiality or compliance obligation, and the skill should say so where it applies rather than treating it as a generic line item.

---

## Step 6: Make the call

Finish on one of three. Anything else is a summary pretending to be a verdict.

| The call | What it means |
| :--- | :--- |
| **Low switching cost** | Clean export, nothing found in Step 3 that cannot be replaced cheaply, no meaningful notice period |
| **Switching cost with conditions** | Leaving is fine once specific things happen first: export a named item before cancelling, give a named integration owner notice, confirm data deletion in writing |
| **High switching cost** | What Step 3 or Step 5 found is not fixable by a setting. Name what decides it, and say plainly whether that is a reason to stay or just a cost worth paying anyway |

Conditions have to be actions, the same rule `before-you-install` holds itself to. "Back up your data first" is not a condition. "Export the automation rules from Settings before cancelling, because they are not included in the CSV export" is.

---

## Output

Fill `assets/exit-checklist.md` and hand it over: the inventory from Step 1, an export verdict per item, what is lost outright, the hour estimate and what it is built from, the exit terms, and the final call.

Above the checklist, no more than three lines: which mode ran, the total hour estimate, and the one finding most likely to change the reader's mind either way.

---

## Failure modes

**Answering about the tool's category instead of this account.** "Project management tools generally export to CSV" is not an answer about whether this account's custom fields, automations and history export. Check the account, not the category.

**Treating "it exports" as "it is done."** An export that lands nowhere useful, or that has to be manually reshaped before the destination can read it, still costs the hours in Step 4. Do not let a clean export line hide the rebuild work behind it.

**Quantifying switching cost in dollars.** No credible source exists for this across tools; see `references/evidence.md`. Hours are honest. A dollar figure invites a false precision this skill cannot back up.

**Skipping Step 5 because the reader is not planning to cancel yet.** Notice periods and retention terms change the timeline of any decision, not just a finished one. Check them even when the reader is only weighing the option.

---

## What this does not do

- **Not a migration guide.** It names what breaks and what it costs. It does not walk through the mechanics of the move itself.
- **Not a renegotiation skill.** Whether to leave, or what to pay to stay, is `stack-audit`'s or a direct conversation with the vendor, not this skill's job.
- **Not legal advice.** Data-retention and contract-term findings are reported from what the terms say. Anything contractual or regulated goes to someone qualified.
- **Not a guarantee.** A low-switching-cost call means nothing found in this check makes leaving expensive. It does not mean nothing will go wrong in the move itself.

---

## Supporting files

- `assets/exit-checklist.md` - the checklist this skill fills in and hands over
- `references/evidence.md` - why this skill argues from mechanism rather than a statistic, and what was checked and found wanting
