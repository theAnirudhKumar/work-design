# protect my focus

**Find what is actually interrupting you, negotiate the real source, and test one fix for two weeks.**

"Just turn off notifications" is the usual advice, and it fails when you are a nurse, a support lead or a parent working from home. This skill audits six sources (notifications, chat, email, drop-ins, meetings, self-interruptions), ranks them by how often they hit, how hard they are to recover from, and how much you can change, then picks one to three countermeasures that fit your job. It writes the actual messages: short, specific, with an offer, as a two-week trial. It ends on an experiment with one measure and a day-14 review date.

If interruption is part of your job, it designs for interruptible work, with resume notes, cover windows and a first-line rota, instead of pretending it away.

The failure this exists to prevent: **telling someone to "just turn off notifications" in a job where that is impossible, or never negotiating the real source of the interruptions.**

**Reach for it:** when interruptions are a pattern, not a bad afternoon. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Examples

*Illustrative. The people and organisations are invented, and the exact output varies with what you give it.*

**A support lead.** You type: `Chat pings all day, my manager pulls me into calls, I can't get the weekly report done.`

You get (shortened):

```
Placement: mixed. Support is interruptible by design, but the report is not.
Top source: chat, then manager pull-ins. Self-interruptions: probably third.
Measure: a 90-minute report window on Tuesdays, with a named cover on the
queue and your phone open to a single escalation route.
Message to your manager: "Hi Priya, for two weeks I'd like to hold Tuesday
9:00 to 10:30 for the report. Dev has the queue; if a major incident
lands, ring me. I'll note how many windows I complete and we review on
the 19th."
Experiment: windows held out of two. Review on day 14.
```

**An engineer in an open office.** You get a maker's-schedule ask for two mornings, a headphones signal with an agreed meaning, and a hand-off: `meeting-audit` for the three recurring meetings that take most of the afternoon.

**A parent working from home.** You get notification batching with a short allow-list (school, one family member), a note that "off" is not an option while a child is at school, and a five-minute resume note before each interruption.

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Place the job | Interruptible, interrupting or mixed, from your words |
| Audit six sources | Counts, recovery cost, controllability |
| Rank | Top three and the real source named |
| Choose countermeasures | One to three, each with who must agree and when it backfires |
| Write the messages | Ready to send, with an offer and a fallback ask |
| Set the experiment | One measure, one number, a day-14 review |

---

## Who this is for

Anyone whose attention is sliced up: engineers, writers, managers, nurses, support staff, teachers, freelancers with clients, parents at home. It works whether the interruptions come from software, colleagues or family.

---

## What this needs

**Minimum:** your job and what interrupts it.

**Better with:** a typical day, who interrupts, and what your manager expects about response times.

**Best with:** a pasted calendar week and notification summary, so meetings and alerts are counted. Claude cannot see your calendar or phone, so you paste or read off numbers.

Missing context never blocks this skill. It labels estimates as estimates. It cannot remember across chats or remind you: put the day-14 review date where you will see it.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other skills in the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the protect-my-focus skill from https://github.com/theAnirudhKumar/work-design: copy its skills/protect-my-focus folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/protect-my-focus` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, `references/countermeasures.md` has the nine countermeasures with when each backfires and message templates, and `assets/interruption-audit.md` is a one-page audit you can fill in alone.

---

## Where this comes from

The maker's schedule idea is described in an essay by Paul Graham. The other countermeasures are widely used practice with little direct testing in the form you would use them, and the reference file labels each one's evidence. Studies of interrupted work generally find that getting back into a task costs effort, but the size varies; this skill does not quote a number and asks you to measure your own.

---

## What this does not do

- **Not meeting clean-up.** `meeting-audit` in the sibling meeting-design set cancels, shortens and fixes recurring meetings. This skill counts their cost and hands off by name.
- **Not one focus block.** `start-a-focus-session` runs a single block.
- **Not a licence to disappear.** It designs the exception route for anything that must get through.
- **Not therapy.** If overload is bigger than your calendar, it says once that someone who can help is worth talking to.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
