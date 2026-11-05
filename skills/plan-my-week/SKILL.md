---
name: plan-my-week
description: >
  "plan my week", "weekly review", "Monday morning plan", "what should this week look like", "set up my ideal week", "what did I get done last week and what now", "my week is already a mess". Runs a short review of last week (wins, slips, carry-overs: carry, delegate or drop each), then picks at most 3 outcomes for the week, places them on an ideal-week skeleton with protected focus blocks, assigns theme days only if the work allows, names the one risk with an if-then, and adds one personal item. Works from what the user types. Not for a single day (plan-my-day), ranking a long list (sort-my-tasks), the balance of a whole life (balance-my-life) or building the review habit and tools (build-my-system).
---

# Plan My Week

A weekly plan usually turns into a longer to-do list. Twenty items are copied across, nothing says which three matter, and no hour of the week is protected, so by Wednesday the calendar belongs to other people and the list is a record of what did not happen.

The failure this exists to prevent: **a week that is a longer to-do list, with no outcomes and no protected time.**

Review first, choose few outcomes, then put them on the calendar before anything else can take the hours.

---

## What this needs

**Minimum: a few lines on last week and what is coming.** Typed from memory is enough: what went well, what did not move, what is due. No calendar, no tool, no files.

**Better with** the week's fixed commitments (meetings, shifts, school runs, travel), the last week's plan if one exists, and the person's rough peak time.

**Best with** a pasted `my-system.md`: read its kind of work, peak focus hours, hard constraints, the methods marked trying or keeping, and any weekly rhythm already written. Do not ask for it if the person has none. If a method is chosen (for example a weekly review in GTD style, theme days, or a weekly Ivy Lee list), use it.

Claude cannot see the calendar, keep time or remember across sessions. Say so once: the person pastes or types the fixed commitments, puts the blocks in their own calendar, and saves the plan. If they bring last week's plan back next week, the review will be better.

---

## When this runs

Runs when the person wants to plan the coming week, or review the last one and move on. Typical moments: Sunday evening, Monday at 8:55, Friday afternoon.

**Does not run for:**

- One day. `plan-my-day` builds it, and it is what this plan feeds.
- A long list that needs ranking before anything can be planned. `sort-my-tasks` first.
- How work and the rest of life are shared over months. `balance-my-life` handles that; here the week gets one personal item and nothing deeper.
- Setting up the tools and habit of reviewing. `build-my-system` designs it. This skill performs one review.
- One large project with no plan. `plan-the-work`. Here it becomes an outcome and some blocks.
- A deadline that cannot be met. `fit-to-deadline`.

---

## Step 1: Review last week, in five minutes

Work from what the person gave. If they gave nothing about last week, ask for three lines at once: what got done, what did not, what is still hanging. Do not ask more.

Write the review as:

- **Wins**: two or three things that actually happened. If the person lists none, look for them in what they said and name them; a week with no wins is rare and worth saying aloud.
- **Slips**: what did not happen, and the likeliest reason in a few words (too much, interrupted, unclear, waiting on someone, not important, avoided). One reason each, labelled as a guess.
- **Carry-overs**: every unfinished item gets a verdict, never a silent rollover:
  - **Carry**: it goes into this week, and takes a place in the plan or on the not-this-week list with a date.
  - **Delegate**: it goes to a person (or an AI; see `delegate`), with the one-line ask.
  - **Drop**: it is deleted, and one line says why it is safe to drop.
  If an item has been carried twice, say so and make the person pick delegate or drop, or hand it to `get-unstuck` by name.

Keep the review under half a screen. It is a short look back, not a retrospective. For a full retrospective on a finished piece of work, the person wants `lessons-learned`.

## Step 2: Pick at most three outcomes

An outcome is a result you could point to on Friday, not an activity. "Draft chapter 2 sent to my supervisor" is an outcome; "work on thesis" is not. Choose **three at most**; two or one is fine. A person with one big project this week should have one outcome.

Each outcome gets one line on why it is this week's and what is true when it is done. If the person offers six, ask which three would make the week a success, then move the rest to the not-this-week list. Do not accept six by merging them into "themes". If everything feels equal weight, run the cut, and name `sort-my-tasks` for the longer list.

Check capacity before accepting: about two thirds of the available hours are plannable, and the rest is slack (a rule of thumb, not a measured fact; raise the slack for jobs with inbound demands). Three outcomes that need 50 hours in a 30-hour week are one outcome too many. Say so and cut.

## Step 3: Build the ideal-week skeleton

Lay out the week as days by blocks, in this order:

1. **Fixed commitments**, exactly as given.
2. **Protected focus blocks** for each outcome: named, with a day, a start and a length, placed in the person's peak time and before meetings fill the days. Two or three blocks of 60 to 120 minutes carry most weeks; a heavy-meeting week may hold only one or two. Say which outcome each block serves. If peak time is unknown, assume the morning and label it.
3. **Meeting and admin windows**: where messages, small calls and admin happen so they stop leaking into the focus blocks.
4. **Slack**: at least one block per day or a half-day on Thursday or Friday, left deliberately unplanned.
5. **Shutdown and review slots**: a short Friday close-out and a Sunday or Monday planning slot, so next week's review has an obvious home.

Tell the person the blocks are not real until they are in a calendar, and that Claude cannot place them there.

## Step 4: Theme days, only if the work allows

Offer a theme for a day (for example writing on Tuesday, calls on Thursday) **only if the person's work lets them hold it**. Ask yourself: can this person defer inbound requests for a day? Nurses on a ward, support agents, teachers during term, on-call engineers and parents of young children mostly cannot. For them, use theme **half-days** or none, and say why. A theme that gets broken every week is worse than none. Never force themes into a person whose day is set by others.

## Step 5: Name the one risk, with an if-then

Pick the single thing most likely to wreck the plan (a meeting that always grows, a dependency on someone's reply, a child's sick days, a deadline from outside). Write one line: **"If [observable thing] by [day or time], then [concrete action]."** The cue must be something the person will actually notice. Example: "If Wednesday 12:00 passes and Hana has not sent the figures, then I draft the report without them and mark the gap." One risk only; a list of six is a worry, not a plan. For a deeper stress test, `what-could-go-wrong` can run on the whole plan.

## Step 6: Add one personal item

Add one thing for the person that is not work, placed on the skeleton as a real block: a walk, a call to a friend, a class, a meal with someone, an hour of a hobby. It gets a day and time like any other block. If the person has none in mind, offer two or three options based on what they said and let them pick; do not assign one that sounds like homework. If the week is genuinely a crisis week, a smaller version (a 20-minute walk) still counts. This is a gesture, not a life audit; `balance-my-life` does the audit.

## Step 7: Hand days to the day planner

End by saying that each morning `plan-my-day` can turn one day of this skeleton into a time-blocked plan, with the outcome blocks already placed.

---

## Output

Use `assets/week-plan.md`. In this order, short:

1. **Last week**: wins, slips, and every carry-over with its verdict.
2. **This week's outcomes** (three at most) with what done looks like.
3. **Ideal-week skeleton**: a table of days by blocks, with focus blocks, windows, slack, the personal item and the review slots.
4. **Themes** (or "none, because ...").
5. **Not this week**: each item with a landing date or "drop".
6. **The one risk** and its if-then.
7. **What I had to assume.**

Fit the whole plan on one screen where possible.

---

## Failure modes

**A longer to-do list.** The output is twenty tasks sorted by day. If the plan has no outcomes and no named blocks, Step 2 and Step 3 were skipped.

**Four to six outcomes.** Cut to three, or one. More is a wish list.

**Silent rollover.** Last week's unfinished items reappear with no verdict. Every one is carried, delegated or dropped, in words.

**Protected time that is not placed.** "Block out time for deep work" with no day, hour or length. Name the block.

**Theme days for jobs that do not allow them.** Ask first, then offer half-days or none.

**Planning to 100%.** Every hour is assigned, so any interruption breaks the week. Keep slack.

**A risk list.** One risk with one if-then, not a table of worries.

**A personal item that is homework.** "Exercise 5 times" is a project. Pick one real thing the person would look forward to.

**Review as confession.** The review is three short lists. Do not interrogate the person about why a week went badly; one reason per slip, labelled as a guess.

**Claiming to see the calendar.** Claude cannot. Ask for fixed commitments and say which blocks are provisional.

**Motivational filler.** None.

---

## Supporting files

- `references/methods-cheatsheet.md` - the methods this skill applies, with how each is used and when it backfires.
- `assets/week-plan.md` - the Week Plan template: review, outcomes, skeleton, risk and the personal item.
