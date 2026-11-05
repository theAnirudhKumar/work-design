# sort my tasks

**Never leave a list in which everything is priority one.**

Ask for help prioritising and you usually get high, medium and low, applied to forty items, thirty of which land on high. The list looks organised and nothing has been decided.

This skill takes the mess as it is, a brain dump included. It cleans it (merges duplicates, splits compound items, rewrites vague ones as actions), then picks the one prioritisation method that fits this list and says why in a line: Eisenhower for a mixed daily list, Ivy Lee for the six-item end-of-day cut, 1-3-5 for a day's shape, RICE or impact/effort for competing projects, MoSCoW for scope under a deadline, Hell yeah or no for commitments. You get a ranked list with no ties, the first physical action for the top three, a Delete/Defer/Delegate list with a reason for each, and a not-doing list with the cost you are accepting.

The failure this exists to prevent: **a prioritised list in which everything is priority one.**

**Reach for it:** at 11pm with a head full of tasks, or when the list has outgrown the page. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The person and business are invented. Output varies.*

You type: `Brain dump: reply to Priya about invoice, invoice thing, taxes, call mum, new website??, fix the van's brake light, update the price list, newsletter redesign, order flour for Saturday, say yes to Luis's podcast invite, accountant docs, renew van insurance.` (Adriana runs a small bakery, Fennel and Rye.)

You get (shortened):

```
Cleaned: 12 lines became 10 items (invoice lines merged; "taxes" and
"accountant docs" merged). Horizon: this week (assumed).
Method: Eisenhower, because this is a mixed list of business and home items
with two real deadlines.

Ranked
  1. Order flour for Saturday (deadline: supplier cutoff tomorrow, assumed)
  2. Renew van insurance (lapses Friday, assumed)
  3. Reply to Priya with the corrected invoice
  4. Fix the van's brake light (safety, and legal to drive)
  5. Gather accountant documents ...

First actions
  1. Open the supplier's order page and enter last Saturday's quantities.
  2. Open the insurer's renewal email and click "renew".
  3. Open the invoice, change the VAT line, save as a new PDF.

Delete / Defer / Delegate
  Say yes to Luis's podcast: DELETE (it is not a hell-yeah; send a kind no)
  Update price list: DEFER to the 1st, when flour costs are known
  Call mum: DEFER to tonight 19:00 (personal, takes 3 minutes)

Not doing
  Newsletter redesign: cost accepted, another month of the old layout.
  New website??: cost accepted, no online orders this quarter.
```

---

## What it actually does

| Section | What you get |
| :--- | :--- |
| Cleaned | Counts, the horizon assumed, and the method with one line on why it fits this list |
| Ranked | One list, numbered, no ties, with a cap on how many can sit at the top |
| First actions | A physical first move for each of the top three, under about 10 minutes |
| Delete / Defer / Delegate | Each item with a one-line reason; Defer needs a date or trigger |
| Not doing | Valid items you are deliberately not doing, each with the cost accepted |
| Hand-off | A pointer if the list reveals a scope or deadline problem, a stuck item, or a day to plan |

---

## Who this is for

Anyone with more on the list than the time: students, nurses, founders, teachers, engineers, parents, freelancers, shift workers. It works on a pasted list, a note or a dictated dump. It also works on a list of projects, where it switches method.

---

## What this needs

**Minimum:** the list, as messy as it is.

**Better with:** deadlines, who is waiting on what, and the horizon (today, this week, this quarter).

**Best with:** a pasted `my-system.md`; if you already chose a prioritisation method it will use it when it fits.

Nothing is a prerequisite. Claude cannot see your task tool or your real deadlines, so any date it guesses is labelled and you correct it.

---

## Where it hands off

- Plan the day from the top items: `plan-my-day`
- Plan the week: `plan-my-week`
- The top items add up to more than a deadline allows: `fit-to-deadline`
- One item has no obvious first action: `get-unstuck`
- Decide who or what takes an item: `delegate`
- One item is really a project: `plan-the-work`

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the sort-my-tasks skill from https://github.com/theAnirudhKumar/work-design: copy its skills/sort-my-tasks folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/sort-my-tasks` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `assets/sorted-list.md` is the template, and `references/methods-cheatsheet.md` holds the six ranking methods with an honest note on when each backfires and an evidence label.

---

## Where this comes from

The ranking methods are named in the cheat-sheet with their origins stated only where they are firmly known. Most are widely used and little tested directly, and the cheat-sheet labels them that way. The cap on the top tier is a rule of thumb, not a measured value. No figure for time saved is claimed.

---

## What this does not do

- **Not a schedule.** It ranks; `plan-my-day` and `plan-my-week` schedule.
- **Not a scope fix.** If the list cannot fit the deadline, that is `fit-to-deadline`.
- **Not a way to avoid a hard item.** A top item with no obvious first move goes to `get-unstuck`.
- **Not a decision made for you.** The reasons are shown so you can overrule them.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
