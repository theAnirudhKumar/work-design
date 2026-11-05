# balance my life

**Put work and the rest of your life on one page, find the biggest gap, and change one thing.**

Most productivity advice makes work output bigger. Meanwhile the people, health and interests you say matter shrink a little each month, because nobody decided it. And the usual fix, a perfect ideal week, breaks by Wednesday.

This skill scores 6 to 8 life areas (you can rename them): how much each matters, how satisfied you are, the hours you really give it, and whether it gives or drains energy. Rough numbers are fine. It finds the largest gap between what matters and where time goes, then offers the trade-off out loud: more of one thing means less of another, which do you pick this month? You choose ONE small shift, with a fallback and a review date. It sketches an ideal week with your personal anchors placed first, checks that it fits the hours that exist, and writes the words for a boss, partner or family member.

It says plainly that balance is not an equal split and that seasons differ: a new baby, a launch and exams each justify a lopsided week for a while.

The failure this exists to prevent: **optimising work output while the things that matter quietly shrink, or drawing a fantasy ideal week that does not survive contact with real life.**

**Reach for it:** when work is crowding out the rest, or you need to say no to someone. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. Output varies with what you give it. The person is invented.*

You type: `I'm a nurse on rotating shifts. I never see my friends and I haven't exercised in months. Where does my time go?`

You get (shortened):

```
Season: demanding but ordinary. Shifts are fixed; review in 4 weeks.

Area             Matters  Satisfied  Hours/wk  Energy
Work             4        3          42        drains
Health and body  5        1          1         gives
Friends          4        1          1         gives
Rest and sleep   5        2          49        neutral
(+ family, admin, learning, purpose: "faith/choir", 2 hrs)

Largest gap: health and friends matter a 4 or 5 and get about 2 hours
between them. Nothing in the week is placed for either.

Trade-off: a regular run means about 3 hours less of rest or admin.
Which do you pick this month?

ONE shift: a 25-minute walk with a friend after the first day shift of
each block. Fallback: a phone call. Review in 4 weeks.

Script to a friend (soft): "I've been bad at keeping in touch. Can we
walk after my first day shift each rota? I'll send my dates."
```

The full template is in [`assets/balance-check.md`](assets/balance-check.md).

---

## What it does not do

- **Not therapy or medical advice.** If you describe severe distress, burnout symptoms or health problems, it says once, kindly, that a professional is worth talking to. It does not diagnose, and carries on with the practical part only if you want it.
- **Not a week planner.** Placing this week's tasks is `plan-my-week`.
- **Not a habit tracker.** One behaviour you want to keep is `build-a-habit`.
- **Not a method picker or an interruption fix.** That is `find-my-method` and `protect-my-focus`.
- **Not a guarantee.** A chosen shift is a trial. You review it in a few weeks.

---

## What this needs

**Minimum:** your week described in your own words.

**Better with:** the areas you care about, rough hours, and fixed constraints (shifts, caregiving, a commute).

**Best with:** a pasted calendar for a typical week, and your `my-system.md` from `build-my-system` if you have one. Claude cannot see your calendar or remember earlier chats, so you paste what you want used and save what you want kept.

Nothing is required. Missing context changes what it has to assume, which it lists at the end.

---

## Install

As a plugin in Claude Code or Cowork:

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the balance-my-life skill from https://github.com/theAnirudhKumar/work-design: copy its skills/balance-my-life folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/balance-my-life` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill.

**Or just read it.** `SKILL.md` is the method, `assets/balance-check.md` is the template and `references/life-areas.md` is the cheat-sheet.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
