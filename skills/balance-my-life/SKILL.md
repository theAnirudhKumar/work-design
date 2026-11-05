---
name: balance-my-life
description: >
  Trigger on "work-life balance", "I'm working too much", "I neglect my family", "where does my time go", "I never see my friends", "I have no life outside work", "I feel out of balance", "how do I fit in health and hobbies", "help me say no to my boss", "protect my evenings". Scores 6 to 8 life areas for how much each matters, how satisfied the user is and the hours really given, finds the biggest gap between what matters and where time goes, picks ONE small shift with an explicit trade-off, sketches an ideal week with protected personal anchors, and writes boundary scripts for a boss, partner or family member. Not for planning one week's tasks, which is plan-my-week, for starting a single habit, which is build-a-habit, or for work interruptions, which is protect-my-focus.
---

# Balance My Life

Most productivity effort goes into getting more work out. Meanwhile the things that matter outside work shrink a little each month and nobody decides that. This skill puts work and the rest of life on one page, finds the biggest gap, and makes one small, realistic change.

The failure this exists to prevent: **optimising work output while the things that matter quietly shrink, or drawing a fantasy ideal week that does not survive contact with real life.**

---

## What this needs

**Minimum: the user describing a normal week in their own words.** "Work 9 to 6, commute an hour, kids to bed at 8, I mostly collapse after" is enough. Draft the whole check from that and label every guess.

**Better with** the areas they care about, rough weekly hours per area, and any fixed constraints (shifts, caregiving, a commute, a visa, exams).

**Best with** a pasted calendar for a typical week and the user's `my-system.md` if they have one. Claude cannot see a calendar or remember earlier chats, so the user pastes what they want used.

Nothing is a prerequisite. Rough hours are fine. Missing detail changes how many lines appear under "What I had to assume", never whether the check runs. A short cheat-sheet of default areas, season guidance and script patterns is in `references/life-areas.md`.

---

## When this runs

Runs when the user feels work is crowding out other things, wants to know where their time goes across all of life, or needs words for a limit with a boss, partner or family member.

**Does not run for:**

- Planning this week's tasks and outcomes. That is `plan-my-week`.
- Starting or keeping one habit such as running or reading. That is `build-a-habit`. This skill may end by naming it.
- Interruptions and meetings at work. That is `protect-my-focus`.
- Choosing a productivity method. That is `find-my-method`.
- Building the whole organising system. That is `build-my-system`.

---

## Step 1: Say what balance is, in two lines

Say once, briefly: balance is not an equal split, and the right mix changes by season (a new baby, a launch, exams, a caring role, a job change). The aim is that the things the user says matter get time on purpose, for now. Then move on. No lecture.

## Step 2: Safety check, once

If the user describes severe distress, hopelessness, burnout symptoms (exhaustion that rest does not touch, dread, numbness, not coping), sleep or health problems, or anything that sounds like a crisis, say once, kindly, that a professional who can help (a doctor, therapist or a local helpline) is worth talking to. Do not diagnose, do not name conditions, do not repeat it later. Then ask whether they want the practical part, and continue only if they do. If they describe immediate danger, point to local emergency services and stop the exercise.

## Step 3: Pick the areas

Offer 6 to 8 areas and let the user rename, drop or add. Default set: work or study, health and body, family and partner, friends and community, money and life admin, learning and growth, rest and fun, and a purpose area (faith, creative work, volunteering, a cause; the user names it). Choose the set from what they said and show it in one line. Fewer than six hides the trade-offs; more than eight cannot be acted on.

## Step 4: Score each area

Draft the table straight away from the user's description, then let them correct it. For each area:

- **Matters:** 1 to 5, how much it matters to them now, in this season.
- **Satisfied:** 1 to 5, how they feel about it today.
- **Hours:** rough hours per week actually given (include thinking about it only if the user does).
- **Energy:** gives, neutral or drains.

Mark guessed numbers (assumed). Ask nothing before the first draft. After it, ask at most three questions, each naming the number it would change.

## Step 5: Find the largest gap

Compare what matters with where time goes. The gap is an area with high Matters and low Satisfied or low Hours, ranked against the share of the week going elsewhere. Name one area as the largest gap and say why in two sentences. Also name the area that is taking time while scoring low on Matters, if there is one. Never call it a failure; say what the numbers show and what they cannot show.

## Step 6: Offer the trade-off, then choose ONE shift

Time is fixed, so a gain somewhere is a loss somewhere. State it plainly: "More of X means less of Y. Which do you pick this month?" Offer two or three candidate shifts of different cost, each with its price, and let the user choose. Then write the chosen one as a small shift:

- What changes, in one sentence ("Home by 6:30 on Tuesdays and Thursdays").
- The hours it moves, and from where.
- The date it starts and when to look again (two to four weeks).
- A smaller fallback if the week goes wrong.

One shift only. If the user wants three, keep one as the shift and park the others under "Later".

## Step 7: Sketch the ideal week

Build a week as blocks, not a timetable. Start by placing the **personal anchors** first: fixed, named, protected slots for the things from Step 6 and the top-scoring areas (a weekly dinner, a gym session, a call with a parent, one evening off). Then place work around them, then flexible time. Give each anchor a trigger and a floor version ("Thursday 7pm run, 20 minutes if tired"). Use the layout in `assets/balance-check.md`.

Check the sketch against reality before showing it: commute, sleep, fixed hours, caregiving. If the total exceeds the hours that exist, cut and say what was cut. A sketch that adds to more than the week is a fantasy and is not shown. Say that the first two weeks will not match it, and ask the user to compare, not to feel guilty.

## Step 8: Write the boundary scripts

Only for the limits the shift needs. Write each as words the user could say or send, short and plain, in the person's own register: a boss or client, a partner, a family member or friend. Each script has: the fact, the limit, what the user can offer instead. Offer a softer and a firmer version. Patterns are in `references/life-areas.md`. Do not script a confrontation the user did not ask for, and do not write anything that deceives the other person. If the limit may carry a real job risk (a contract, a visa, shifts), say so and keep the script factual.

## Step 9: Close with one next action and one hand-off

Give one action under 15 minutes ("Block Thursday 6 to 8 in your calendar now"). Then one line naming the single most useful sibling, if any: `plan-my-week` to place the shift into next week, `build-a-habit` if the shift is one repeating behaviour, `build-my-system` to put a place for personal commitments into a wider system. If the named skill is not installed, say what the step would be in a sentence and carry on.

---

## Output

In this order, plain text the user can paste or save. Layout in `assets/balance-check.md`.

1. Season line (one sentence on what season this looks like)
2. Life-areas table (Matters, Satisfied, Hours, Energy)
3. The largest gap, in two sentences
4. The trade-off question and the ONE shift chosen
5. Ideal-week sketch with personal anchors marked
6. Boundary scripts (soft and firm)
7. Next action, review date, hand-off line
8. What I had to assume

---

## Failure modes

**An equal split.** Eight hours each does not exist and is not the goal. Compare to what matters now.

**Many shifts.** A life overhaul that lasts a week. One shift, one fallback, one review date.

**Scores that flatter.** The user rates everything 4. Ask which one they would give up first if forced; use that to separate Matters scores.

**Work-only answers.** Producing a better work schedule and calling it balance. Anchors are placed before work.

**An ideal week that exceeds 168 hours or ignores sleep.** Check the arithmetic before showing it.

**Guilt framing.** "You should." Describe, price and let the user choose.

**Scripts that blame.** Lead with the fact and the offer, not the grievance.

**Diagnosing.** Naming burnout, depression or anxiety. Describe what was said, refer once, and stay practical.

**Repeating the referral.** Say it once.

**Inventing hours.** A guessed number is marked (assumed) and corrected on first reply.

A completed check means the trade-off was chosen on purpose. It does not mean the week will go to plan, and it is not advice about health, relationships or employment rights.

---

## Supporting files

- `assets/balance-check.md` - the fill-in template in output order
- `references/life-areas.md` - default areas with prompts, season notes, script patterns and referral wording

## What I had to assume

End every reply with this section, never empty. List each guessed score, hour, constraint or season, with the line it would change if wrong. Also list what could not be checked: the user's calendar, the other person's view, a contract or leave entitlement.
