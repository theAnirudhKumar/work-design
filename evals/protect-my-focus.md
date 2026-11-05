# Evaluation: protect-my-focus

Routing cases for `protect-my-focus`, written alongside the skill.

**Run on:** 5 Nov 2026, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `c4b8a8cfab44`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 41. All three models matched on 41; Haiku 41, Sonnet 41, Opus 41. The protect-my-focus description was reworded after this run; see the targeted rerun in `evals/README.md`.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The set must include the skills built alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `balance-my-life`, `build-my-system`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`) and, for the meeting cases, `meeting-audit` from the sibling meeting-design repository, or the near misses are not meaningful. `meeting-design` is the set that contains `meeting-audit`. An Expected value written as A or B means either routing is defensible.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I'm constantly interrupted at work and can't get anything deep done." | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 2 | "My meetings eat my whole day. When am I supposed to do the actual work?" | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 3 | "Slack is killing me. Forty pings an hour and my manager expects instant replies." | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 4 | "People keep dropping by my desk all day. How do I stop it without being rude?" | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 5 | "How do I tell my manager I need two uninterrupted mornings a week?" | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 6 | "I'm a nurse and I'm interrupted every few minutes. Everyone says turn off notifications." | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 7 | "I work from home with two kids and a support queue. I can't concentrate for ten minutes." | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 8 | "My inbox runs my day. I open it forty times and get nothing done." | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 9 | "Give me a two-week experiment to get more focus time at work." | Should fire | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 10 | "Help me focus for an hour on this report." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 11 | "Start a Pomodoro, I have a spreadsheet to finish." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 12 | "Our weekly status meeting is useless and runs an hour. How do we fix it?" | Near miss | meeting-audit (meeting-design set) | meeting-audit | meeting-design | meeting-design |
| 13 | "Audit my recurring meetings and tell me which to cancel." | Near miss | meeting-audit (meeting-design set) | meeting-audit | meeting-audit | meeting-audit |
| 14 | "Should this be a meeting or can I send a message?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 15 | "Plan my day, I have a lot of meetings and tasks." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 16 | "Plan my week around my meetings and my launch." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 17 | "I have too much to do. Prioritise this list for me." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 18 | "I'm stuck on this one report and keep putting it off." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 19 | "I work all the time and never see my family. Help me balance things." | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 20 | "Which productivity method should I use to get more done?" | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 21 | "What's the maker's schedule and does it work?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 22 | "Set up my whole productivity system, including a focus rule." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 23 | "I want to build a habit of checking email only twice a day." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 24 | "Should I give this task to an agent or do it myself?" | Near miss | delegate | delegate | delegate | delegate |
| 25 | "I have two days left for the report. What should I cut?" | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 26 | "Before I begin, what is in and out of scope for this project?" | Near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 27 | "Break this down for me: I have to launch a new service." | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 28 | "How long will this migration actually take?" | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 29 | "What could go wrong with my plan to block mornings for deep work?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 30 | "Review the email I'm about to send to my manager asking for focus time." | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 31 | "Retro on how my focus-time experiment went." | Near miss | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 32 | "Hand off this chat so I can continue later." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 33 | "My prompts cost too many tokens." | Near miss | cut-token-cost | cut-token-cost | cut-token-cost | cut-token-cost |
| 34 | "Audit our software subscriptions: is Slack worth what we pay?" | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 35 | "Is this notification-blocker app safe to install?" | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 36 | "What breaks if we move from Slack to another chat tool?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 37 | "What can work-design do for me?" | Near miss | work-design | work-design | work-design | work-design |
| 38 | "Slack is killing me and I need to write for two hours right now." | Ambiguous | protect-my-focus or start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 39 | "My manager keeps scheduling meetings in my focus time." | Ambiguous | protect-my-focus or meeting-audit | protect-my-focus | protect-my-focus | protect-my-focus |
| 40 | "I get distracted by my own phone, not by other people." | Ambiguous | protect-my-focus or start-a-focus-session or build-a-habit | protect-my-focus | protect-my-focus | protect-my-focus |
| 41 | "I'm drowning in everything, work, home, emails." | Ambiguous | balance-my-life or protect-my-focus or sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |

---

## What each case tests

**1, should fire.** The core trigger, with no field named. Systemic, not one block.

**2, should fire.** Meetings as a source. The skill should count their cost and hand off recurring-meeting cleanup to meeting-audit, not clean them up itself.

**3, should fire.** Chat plus a manager expectation. Expects a response-time norm and a drafted message.

**4, should fire.** Drop-ins. Expects a status signal, a check-in offer and a message to the main interrupter.

**5, should fire.** A negotiation request. The output must include the message itself, short and specific, with an offer and a trial.

**6, should fire.** Interruption is the job. The skill must not recommend 'just turn off notifications'; it should design for interruptible work (cover windows, resume notes).

**7, should fire.** Caregiving plus interruptible work. Expects a realistic design and an exception route.

**8, should fire.** Email and self-interruption. Expects batching windows and a note that self-interruptions are the part under the user's control.

**9, should fire.** Names the experiment directly. Expects one measure and a day-14 review.

**10, near miss.** One block now, with no pattern. The word 'focus' is the overlap risk.

**11, near miss.** A named format for one task.

**12, near miss.** A specific recurring meeting. protect-my-focus counts meeting cost across sources; fixing a meeting belongs to the sibling set.

**13, near miss.** Direct meeting clean-up. Tests that this skill hands off by name rather than doing the audit.

**14, near miss.** Channel choice for one communication.

**15, near miss.** A single day's plan. Meetings are given, not being negotiated.

**16, near miss.** Weekly planning. The week is the object, not the interruption pattern.

**17, near miss.** Overload of tasks, not of interruptions.

**18, near miss.** A single stalled piece of work, a different problem from interruptions.

**19, near miss.** Life balance, not workplace interruption. Both involve boundaries and scripts.

**20, near miss.** Method selection.

**21, near miss.** A question about one method. The maker's schedule is a countermeasure in this skill, so an explanation request must go to the explainer.

**22, near miss.** A full system. A focus rule is one part of it.

**23, near miss.** A behaviour the user wants to establish, framed as a habit. The overlap is real; if the cause is interruptions at work, protect-my-focus fits better.

**24, near miss.** Allocation.

**25, near miss.** Scope against a deadline.

**26, near miss.** Boundaries of one project.

**27, near miss.** Framing a non-trivial task.

**28, near miss.** An estimate.

**29, near miss.** Stress-testing a given plan.

**30, near miss.** A draft exists and needs review. If the user asks protect-my-focus to write it, that is this skill.

**31, near miss.** Closing out finished work. A day-14 review of this skill's own experiment is a case for protect-my-focus; a general retro is not.

**32, near miss.** Chat handoff.

**33, near miss.** Token economy.

**34, near miss.** Spend review. Slack is the overlap risk.

**35, near miss.** Vetting an app, not designing a response.

**36, near miss.** Exit cost of a tool.

**37, near miss.** The menu.

**38, ambiguous.** A pattern and an immediate block. Best behaviour: run the block first or hand off, and mention the other.

**39, ambiguous.** Partly a negotiation (this skill) and partly a meeting-design problem. The expected route is protect-my-focus with a hand-off for recurring meetings.

**40, ambiguous.** Self-interruption. Three skills have a claim. The audit treats it as one source; a single block uses phone-away; a habit is about the long-term behaviour.

**41, ambiguous.** A broad overload statement. Tests that a clarifying question picks the real friction. If the user describes distress beyond work, expect the one-time referral.

---

## Output check

Two cases to be checked by hand once a model is available.

**Case 6 (nurse).** The output must not tell the user to turn off notifications. It should place the job as interruptible, then offer design measures: a resume note before switching, a cover window with a named person, and an exception route. A single message to a colleague or charge nurse should be included, short and with an offer.

**Case 5 (manager request).** The output should contain a ready-to-send message of about three to six sentences with the hours, the channel, an offer in return, a two-week trial, and one thing to measure. It should also include a fallback ask. It should end on an experiment with one measure and a review date, and name that Claude cannot remind the user.

**Case 2 (meetings).** The output should count meetings as one source and hand off recurring-meeting clean-up to `meeting-audit` by name, without trying to cancel or redesign meetings.


---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

No misses on cases with a single expected answer.
