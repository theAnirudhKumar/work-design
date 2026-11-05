---
name: sort-my-tasks
description: >
  "I have too much to do", "prioritize this list", "what should I do first", "everything feels urgent", "here's my brain dump, sort it out", "help me cut this list", "which of these actually matter", "rank these projects". Takes a messy list, cleans it (merges duplicates, rewrites vague items as actions), picks the prioritisation method that fits this list and says why (Eisenhower, Ivy Lee, 1-3-5, RICE or impact/effort, MoSCoW, Hell yeah or no), then gives a ranked list with no ties, the first physical action for the top 3, a Delete/Defer/Delegate list with a reason each, and a not-doing list. Not for scheduling a day (plan-my-day) or a week (plan-my-week), fitting scope to a deadline (fit-to-deadline) or one stuck item (get-unstuck).
---

# Sort My Tasks

The usual output of "help me prioritise" is a tidier list in which everything is still priority one. High, medium and low are applied to forty items, thirty land on high, and the person is exactly where they started with nicer colours.

The failure this exists to prevent: **a prioritised list in which everything is priority one.**

Force a rank, give three items a first physical action, and move the rest out of sight with a reason attached.

---

## What this needs

**Minimum: the list, as messy as it is.** A brain dump typed in one go, a pasted note, an exported list. Fragments, duplicates and half-sentences are fine. No tool, no calendar, no file.

**Better with** a deadline or two, who is waiting on what, and the horizon being sorted for (today, this week, this quarter).

**Best with** a pasted `my-system.md`: read the methods marked trying or keeping, and use one of them if it fits the list. Ignore methods marked dropped. If there is no such file, do not ask for it.

If a fact is missing (a deadline, an effort, a value), assume it, label it, and say which ranking it would change. Claude cannot see any task tool, remember past sessions or know the person's real deadlines; say so briefly, and give the output in a form that can be pasted back into whatever the person uses.

---

## When this runs

Runs when the person has a list or a pile of things and wants it ranked, cut or made sense of.

**Does not run for:**

- Turning today into a schedule. `plan-my-day` does that, usually after this skill.
- Planning a week around outcomes. `plan-my-week`.
- A list that is really one project too big for its deadline. That is `fit-to-deadline`; hand off in Step 6.
- One item the person cannot start. `get-unstuck`.
- A single decision about whether to hand something to an AI or a person. `delegate`.
- Choosing a whole productivity method or system. `find-my-method` and `build-my-system` handle that. This skill only picks a ranking method for one list.

---

## Step 1: Clean the list

Do this first and silently, then show the cleaned list in the output.

- **Merge duplicates and near-duplicates.** "Email Priya", "reply to Priya about invoice" and "invoice thing" are one item.
- **Split compound items.** "Sort taxes and call Mum" is two. Anything joined by "and" with two different outcomes is split.
- **Rewrite vague items as actions.** Verb plus object, with the stopping point if it is obvious: "taxes" becomes "Gather the 2025 receipts into one folder". If the meaning cannot be guessed, keep the original wording and mark it (unclear).
- **Tag the facts that change the rank where known:** a hard deadline, who is waiting, a rough time, what happens if it is skipped.
- **Mark items waiting on someone else** and show them separately in the final list; they cannot be done by the person.

State the count: "47 lines became 31 items." Then state the horizon assumed and why.

## Step 2: Choose the method for this list, and say why in one line

Pick one. Do not apply several at once.

| The list is | Use | Because |
| :--- | :--- | :--- |
| A mixed daily or weekly list of work and life items | **Eisenhower** (urgent/important) | Separates what is on fire from what matters, and exposes the urgent-but-not-important that eats days |
| An end-of-day cut for tomorrow, or "just tell me the order" | **Ivy Lee** (top 6 in rank order, do in sequence) | Forces a strict order and a ceiling of six |
| A day's shape with mixed sizes | **1-3-5** (1 big, 3 medium, 5 small) | Caps the day and mixes sizes so it can be done |
| Competing projects or options with measurable value | **RICE** if reach, impact and confidence can be estimated; **impact/effort** if not | Compares value to cost so the loud project does not win |
| Scope against a deadline (what is in this release, this trip, this event) | **MoSCoW** (must, should, could, won't) | Fixes the must-haves first and names what is out |
| Commitments and invitations (should I say yes) | **Hell yeah or no** | A yes needs enthusiasm; anything else is a no |

Write one line, for example: "Method: Eisenhower, because this is a mixed list of work and home items with a few real deadlines." Details and when each backfires are in `references/methods-cheatsheet.md`. If the person has a chosen method and it fits, use it and say so. If it does not fit this list, say why and use the one that does.

## Step 3: Rank, with no ties

Apply the method, then produce **one ranked list numbered from 1 with no ties**. Rules:

- No item gets a label that means "important" for more than a small share of the list. If the ranking starts to read "everything is Do first", stop, and apply a cap: at most **3 items in the top tier**, and at most about a fifth of the list in the top two tiers combined. The cap is a rule of thumb. Say what it forced.
- When two items tie, break it with one question: which hurts more if it slips by a day? Say so in a few words.
- Show only the first 10 to 12 in full if the list is long. Group the rest as "ranked after 12" in one block, ordered, so the person is not buried.
- Put waiting-on items in their own short block with who and the date to chase.

## Step 4: First physical action for the top 3

For each of the top three, write the first action as something done with hands or eyes in under about 10 minutes: **"Open the March invoice sheet and filter for overdue"**, not "deal with invoices". It starts with a verb, names the object, and ends at a point where the next step is obvious. If the first action is not obvious, that item may be stuck; name `get-unstuck` for it after the output.

## Step 5: Sort the rest into Delete, Defer, Delegate, and the not-doing list

Every item outside the top group goes in exactly one of these, with a **reason** of one line:

- **Delete**: no longer needed, already done, or someone else's problem. "Expired: the event was in March."
- **Defer**: will do, but not now. Give a **date or trigger**: "When the Q4 numbers land (about the 20th)."
- **Delegate**: someone else should do it. Name who and the one-line ask. If an AI could take it, name `delegate` for the verification and stop conditions.
- **Not doing**: a real, valid item that is **deliberately not being done in this horizon, and not being scheduled**. Each line states the cost accepted: "Not redesigning the newsletter this quarter; the cost is another quarter of the old layout." Revisit only if a named thing changes.

Do not let Defer become a dumping ground. An item deferred without a date or trigger moves to Delete or Not doing, and a line says which.

Ask for nothing before showing this. The person corrects the reasons that are wrong.

## Step 6: Hand off where the list reveals something bigger

After the output, add at most one or two lines:

- The top items add up to more work than the time before a deadline: "These add up to more than you have before [date]. Fitting it is `fit-to-deadline`."
- One item has sat for weeks or the first action is not obvious: `get-unstuck`.
- The person wants today planned from the top items: `plan-my-day`. The week: `plan-my-week`.
- The list is one project in disguise: `plan-the-work`.

Do not run those skills inside this one.

---

## Output

Use `assets/sorted-list.md`. In this order:

1. **Cleaned**: the count, the horizon, and the method with its one-line reason.
2. **Ranked list**: 1 to N, no ties, waiting-on items separate.
3. **First actions** for the top 3.
4. **Delete / Defer / Delegate**, each with a reason.
5. **Not doing**, each with the cost accepted.
6. **Hand-off** line, only if one applies.
7. **What I had to assume.**

---

## Failure modes

**Everything is priority one.** The top tier holds half the list. Apply the cap in Step 3.

**Labels instead of a rank.** High, medium and low are not a ranking. Number the list.

**A method chosen by habit.** Eisenhower used on three competing projects with measurable value, or RICE on a Tuesday to-do list. Match the method to the list and say why.

**Stacked methods.** Two or three methods applied at once. Pick one.

**Cleaning that changes the meaning.** A vague item rewritten into something the person never meant. Mark guesses (unclear) rather than inventing.

**Defer as a graveyard.** Dozens of "later" items with no date. Defer needs a date or trigger.

**Delete without nerve.** Nothing is ever deleted, so the list never shrinks. If an item has been on a list for months and nobody asked, say it is probably a delete.

**First actions that are plans.** "Plan the proposal" is not a physical action. Say what the hands do.

**Pretending to know the deadlines.** Assumed dates are labelled. A wrong assumed deadline changes the whole rank.

**Motivational filler.** None.

---

## Supporting files

- `references/methods-cheatsheet.md` - the six ranking methods plus the four-way sort, with when each backfires.
- `assets/sorted-list.md` - the Sorted List template.
