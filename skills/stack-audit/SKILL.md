---
name: stack-audit
description: >
  Audits the tools the user already pays for: what overlaps, what nobody has
  opened in ninety days, and what to cancel. Trigger when the user says
  "audit my subscriptions", "what are we paying for", "review our software
  spend", "what tools do we actually use", "SaaS audit", "stack audit",
  "what should I cancel", "are we paying for duplicates", or asks to review,
  clean up or rationalize a list of tools or subscriptions already in use.
  Builds an inventory table with cost, last use, overlap and a verdict per
  row, sorted worst first. Use before-you-install instead for a single new
  tool the user has not adopted yet; this one is for the tools already on
  the books.
---

# Stack Audit

The failure this exists to prevent: **paying every month for a decision made once, on a tool nobody has opened since, because nobody put a date on revisiting it.**

Subscriptions are the easiest spend in a business or a personal budget to lose track of, because the bill is the only thing that recurs. The decision to keep paying does not recur unless something forces it to. This skill forces it.

---

## What this needs

**Minimum: a list of tool names from memory.** Nothing else required. The audit runs, and it says plainly that anything not on the list was not covered.

**Better with** a card or bank statement export, or an app-store subscription list, pasted in. This turns the inventory from what the user remembers paying for into what they are actually being billed for, which are reliably different lists.

**Best with** a one-phrase answer for what each tool was actually hired to do. That is what makes overlap detection possible. Two tools in the same vendor category are not necessarily doing the same job, and two tools in different categories sometimes are.

Where the user gives only a list of names, run anyway. Ask for the job each tool does as part of Step 3, inline, rather than blocking on it upfront.

---

## When this runs

Runs when the user wants to review, clean up or account for the tools already in use, individually or across a team.

**Does not run for:**

- A single new tool not yet adopted. That is a before-purchase question, and `before-you-install` answers it.
- What breaks on leaving one specific tool already marked for cancellation. That is a migration question, a different skill from this one.
- Negotiating a better price on a tool the user is keeping. This skill decides keep or cancel, not what to pay for keep.

---

## Step 1: Build the inventory

List every tool being paid for, personally or through the organization. Where a statement, export or subscription list is available, use it as the source list rather than asking the user to recall from memory. Memory reliably omits the tools nobody opens, which are exactly the ones this audit exists to find.

Where nothing is available, ask for a list from memory and say plainly, in the output, that the audit only covers what was listed.

## Step 2: Fill cost and last use

Per tool, in one row: the cost as actually billed, the billing cycle, and when it was last used.

For cost, use what is actually charged, not the plan's sticker price. Per-seat tools bill for seats purchased, which is frequently more than seats active. Where the user does not know seats active against seats paid, ask, since this gap is one of the most common sources of waste and Step 4's verdict depends on it.

For last use, take the user's own estimate if they have one. Where they do not, write "not known" rather than a guessed date. A guessed date that turns out wrong is worse than an honest gap, because it gets treated as a fact later.

## Step 3: Group by the job, not the category

Ask, in one phrase, what each tool was actually hired to do. Group tools by that phrase, not by the vendor's category.

This catches what a category-based scan misses. Two tools both filed under "project management" are not necessarily doing the same job if one is actually used for time tracking and the other for internal docs. Two tools in different categories can still overlap if both ended up doing the same job in practice, which happens more often than a clean category list would suggest.

Overlap is two or more tools whose one-phrase job is the same. Note it against every row it applies to.

## Step 4: Verdict, one of four

Every row gets exactly one:

- **Keep.** Used, and either no overlap or the strongest tool in its overlap group.
- **Cancel.** Not used in the window the user can speak to, or clearly the weaker of an overlapping pair.
- **Downgrade.** Used, but on a paid tier the user is not using the paid features of, or with paid seats sitting empty.
- **Consolidate.** Merge into another row already marked keep, once the losing tool's cancel is confirmed safe (see Failure modes).

State the reason in the same row. "Cancel" with no reason is not a verdict, it is a guess written down.

## Step 5: Total it and lead with the number

Before showing the table, state the total monthly or annual amount a cancel, downgrade or consolidate verdict would free up, and how many of the rows that total comes from. This is the number that makes the audit worth having done, and it belongs at the top, not buried in the last row of a table nobody finishes reading.

Put a recheck date on the table, three to six months out. An audit run once and never repeated has the same failure mode as the spend it was meant to catch.

---

## Output

Fill `assets/stack-inventory.md` and hand it over. One row per tool: the tool, the job it does, cost and cycle, last used, overlap group, verdict, reason.

Above the table, no longer than three lines: the total recoverable amount, how many rows it comes from, and the recheck date.

---

## Failure modes

**Auditing by category instead of by job.** Two tools filed under different vendor categories that do the same job in practice survive a category scan untouched. Step 3 exists because of this.

**Treating silence as evidence of use.** A tool nobody complains about is not necessarily a tool being used. It is just as often a tool nobody remembers exists. Last use is a fact to gather, not an inference from the absence of complaints.

**Confirming cost from the sticker price.** The plan price and the actual bill diverge whenever seats, usage tiers or add-ons are involved. Ask what is actually charged, not what the pricing page says.

**Cancelling before confirming what a consolidate verdict depends on.** Where a row is marked consolidate, the tool it is merging into has to actually cover the job first. Confirm that before marking the losing tool cancel, not after.

**Running this once.** The recheck date in Step 5 is not optional decoration. A stack audited once and never again drifts back to exactly the state that made the first audit worth running.

---

## What this does not do

- **Not a procurement or negotiation skill.** It decides keep or cancel. What to pay for a kept tool is a separate conversation.
- **Not a vetting skill for a tool not yet adopted.** That is `before-you-install`.
- **Does not cancel anything itself.** It hands over a table with a verdict per row. Acting on it is the user's call.
- **Not proof that unused means unnecessary.** Some tools are correctly paid for and rarely opened by design, such as a disaster-recovery or compliance tool. Note this as an exception on its row rather than defaulting it to cancel.

---

## Supporting files

- `assets/stack-inventory.md` - the table this skill fills in and hands over
- `references/evidence.md` - the sourced figures behind why this audit is worth running, and what not to claim from them
