# stack audit

**Force the decision that only the bill keeps making on its own.**

Subscriptions are the easiest spend to lose track of, because the bill is the only thing that recurs. The decision to keep paying doesn't - a tool gets adopted, used for a month, and sits on the books for two years because nobody had a reason to look again. Nobody decided to keep paying. The renewal just never got interrupted.

This skill interrupts it. It builds an inventory pulled from an actual statement or export where one exists, since memory omits exactly the tools nobody opens, then fills in what's actually billed (not the sticker price), last use, and the job each tool was hired to do. It groups by that job rather than vendor category, since two tools in the same category aren't always doing the same work. Every row gets one verdict - keep, cancel, downgrade, or consolidate - with a reason, and it leads with the number: the total a cancel, downgrade or consolidate verdict would free up, stated before the table.

The failure this exists to prevent: **paying every month for a decision made once, on a tool nobody has opened since, because nobody put a date on revisiting it.**

Part of the **Tool lifecycle** group in [work-design](../../#readme).

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Build the inventory | Every tool being paid for, pulled from a statement or export where one exists rather than relied on from memory alone |
| Fill cost and last use | What's actually billed, not the sticker price - plus last-used, honestly marked "not known" rather than guessed |
| Group by the job | Tools clustered by what they're actually hired to do, catching overlap a category scan would miss |
| Verdict, one of four | Keep, cancel, downgrade, or consolidate - every row, with a stated reason, never a bare guess |
| The total, up front | The recoverable amount and how many rows it comes from, stated before the table |
| A recheck date | Three to six months out, because an audit run once drifts straight back to the state that made it worth running |

---

## Who this is for

Anyone accounting for tools already in use - personally or across a team - who wants to know what's overlapping, what nobody's opened in months, and what to actually cancel. For a single new tool not yet adopted, `before-you-install` is the right skill instead; this one is for what's already on the books.

You don't need connected billing or an admin console. A list of tool names from memory is enough to start, though the audit says plainly what it couldn't cover from that alone.

---

## What this needs

**Minimum:** a list of tool names from memory. The audit runs and says plainly that anything not on the list wasn't covered.

**Better with:** a card or bank statement export, or an app-store subscription list, pasted in - this turns the inventory from what you remember paying for into what you're actually billed for, which are reliably different lists.

**Best with:** a one-phrase answer for what each tool was actually hired to do, which is what makes overlap detection possible at all.

Missing context never blocks this skill. Where only a list of names is given, it asks for the job each tool does inline, as part of the audit, rather than stalling on it upfront.

---

## Install

**The easy way: one paste**

```
I want to install the stack-audit skill from
https://github.com/theAnirudhKumar/work-design. Download or clone the
repository, then copy the skills/stack-audit folder into
~/.claude/skills/ (or .claude/skills/ if this is for one project only),
keeping its own folder name. Tell me the exact folder path it landed in
when you are done.
```

**In the Claude app (no terminal needed)**

1. Download this repository as a ZIP, or clone it
2. Zip the `skills/stack-audit` folder on its own
3. In Claude, go to Customize, then Skills, then Create skill, then Upload skill
4. Upload the ZIP

**As a plugin, in Claude Code or Cowork**

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

**Want the whole set?** The [main README's install section](../../#readme) installs all 9 skills at once.

**Or just read it.** `SKILL.md` is the method, `references/evidence.md` is the sourced figures behind why this audit is worth running, and `assets/stack-inventory.md` is the inventory table itself.

---

## Where this comes from

The case for running the audit at all is grounded in Zylo's 2026 SaaS Management Index - built on more than 40 million licences and $75 billion of tracked spend, published 29 January 2026 - which found organizations leave an average of 36% of their SaaS licences unused. The skill is explicit about the limits of that number: it's aggregate industry data, not a prediction for any one user's result, and `references/evidence.md` states plainly not to quote it as this user's waste, not to extrapolate the enterprise growth figures to a solo user or small team, and not to treat the industry average as a substitute for actually running the audit. The only dollar figure that belongs in the output is the one Step 5 calculates from the user's own rows.

---

## What this does not do

- **Not a procurement or negotiation skill.** It decides keep or cancel. What to pay for a kept tool is a separate conversation.
- **Not a vetting skill for a tool not yet adopted.** That's `before-you-install`.
- **Does not cancel anything itself.** It hands over a table with a verdict per row - acting on it is the user's call.
- **Not proof that unused means unnecessary.** Some tools are correctly paid for and rarely opened by design, like a disaster-recovery tool - that's noted as an exception on its row, not defaulted to cancel.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
