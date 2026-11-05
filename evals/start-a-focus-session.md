# Evaluation: start-a-focus-session

Routing cases for `start-a-focus-session`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 41. All three models matched on 39; Haiku 41, Sonnet 40, Opus 39.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The set must include the skills built alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `balance-my-life`, `build-my-system`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`) and, for the meeting cases, `meeting-audit` from the sibling meeting-design repository, or the near misses are not meaningful. `meeting-design` is the set that contains `meeting-audit`. An Expected value written as A or B means either routing is defensible.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Help me focus for an hour, I have to finish the methods section of my dissertation." | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 2 | "Start a Pomodoro for me, I need to clear my expense receipts." | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 3 | "Pomodoro or a 90-minute block for writing a chapter? Set me up." | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 4 | "I keep sitting down at my desk and not actually working. Can you structure the next two hours?" | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 5 | "Done. Got through the whole outline." | Should fire (debrief) | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 6 | "I got interrupted at about 40 minutes by a phone call from the bank." | Should fire (debrief) | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 7 | "I didn't finish. I only got half the slides done and kept checking Slack." | Should fire (debrief) | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 8 | "I can never start tasks even when I want to. Can we do a 15-minute block together on my tax return?" | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | **get-unstuck** |
| 9 | "I'm working in an open office and need 90 minutes on the brand deck." | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 10 | "I want to write song lyrics for a couple of hours, but timers kill my flow." | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 11 | "I'm on a quiet shift and have 25 minutes before handover. Help me use it to finish my charting." | Should fire | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 12 | "I'm constantly interrupted at work. Slack, people at my desk, meetings. Fix it." | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 13 | "Plan my day. I have a dentist at 2 and a pile of work." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 14 | "Plan my week, I have a launch on Thursday." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 15 | "I have 40 things on my list and no idea what to do first. Rank them." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 16 | "I can't get started on my proposal, I don't even know why." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 17 | "Which productivity method should I use? I've tried a few and none stuck." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 18 | "How does the Pomodoro technique work and is it worth it?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 19 | "Set up my whole productivity system: capture, planning, focus, review." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 20 | "I never see my family and work every evening. Help me find some balance." | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 21 | "I want to start meditating every morning and make it stick." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 22 | "Which of these three tasks is worth my time, and which should I hand to an agent?" | Near miss | delegate | delegate | delegate | delegate |
| 23 | "I have two days to finish the report. What should I cut?" | Near miss | fit-to-deadline | fit-to-deadline | fit-to-deadline | fit-to-deadline |
| 24 | "Before I start this project, what is in scope and what counts as done?" | Near miss | scope-the-work | scope-the-work | scope-the-work | scope-the-work |
| 25 | "I have to write a market analysis. Where do I start?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 26 | "How long will this chapter take me to write? I think about three hours." | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 27 | "Should we have a call about this or can I just message them?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 28 | "Our weekly team meeting wastes everyone's time. Fix it." | Near miss | meeting-audit (meeting-design set) | meeting-audit | meeting-design | meeting-design |
| 29 | "Review this email draft before I send it." | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 30 | "What could go wrong with my study plan?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 31 | "That's done, what did I learn from it?" | Near miss | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 32 | "Hand off this chat so I can continue in a new one." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 33 | "Make my prompts use fewer tokens." | Near miss | cut-token-cost | cut-token-cost | cut-token-cost | cut-token-cost |
| 34 | "Audit our software subscriptions, which should I cancel?" | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 35 | "Should I install this focus app? Check their privacy policy." | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 36 | "What breaks if I switch from this timer app to another?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 37 | "Which work-design skill should I use for my next task?" | Near miss | work-design | work-design | work-design | work-design |
| 38 | "I need to concentrate this afternoon, and also I'm drowning in tasks." | Ambiguous | start-a-focus-session or sort-my-tasks | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 39 | "Help me get started on this essay. Maybe a timer would help." | Ambiguous | start-a-focus-session or get-unstuck | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 40 | "Meetings and Slack kill my focus time. I need a focus session this afternoon." | Ambiguous | start-a-focus-session or protect-my-focus | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 41 | "Block off two hours on my calendar for deep work every morning." | Ambiguous | start-a-focus-session or plan-my-week | start-a-focus-session | **none** | **none** |

---

## What each case tests

**1, should fire.** A named task and a time box, in an academic field. The core trigger.

**2, should fire.** Literal 'Pomodoro' with a shallow admin task. Tests the 25/5 choice.

**3, should fire.** Format choice by task. The user wants a pick and a card, not an explanation of the methods, which would be explain-a-method.

**4, should fire.** The failure the skill names: no defined task, no end. Two hours means the skill splits into blocks.

**5, should fire (debrief).** A bare status message after a session. Only fires if a Focus Card exists in the chat; without one, the skill should ask for the task and done-line. Mark a failure if it plans the week.

**6, should fire (debrief).** An interruption status. The debrief should name the stopping point and offer a restart, with no blame.

**7, should fire (debrief).** A 'didn't finish' status. Tests whether the done-line was too big and whether attention drift is handled with one adjustment.

**8, should fire.** Difficulty starting framed as strategies (shrink the step, body doubling, short block). The output must not diagnose or name a condition.

**9, should fire.** Shared workspace handling: signal to others and a fallback place. Daily interruption as a pattern goes to protect-my-focus, but this is one block.

**10, should fire.** A task not suited to timers. Expected: a longer block or flowtime, with an output-based done-line.

**11, should fire.** Interruptible job. Expects a short block and an exception route, not hiding.

**12, near miss.** A recurring pattern across sources. The word 'focus' is absent; the problem is systemic, not one block.

**13, near miss.** Deciding what the day contains, with fixed commitments. A focus block may appear in the plan, but the request is the whole day.

**14, near miss.** Weekly planning with outcomes and a skeleton.

**15, near miss.** Prioritising a list. No block is requested.

**16, near miss.** A stall with an unknown cause. get-unstuck diagnoses first. If the user adds 'help me focus for an hour on it', expect start-a-focus-session.

**17, near miss.** Method selection for a person, not a session. 'Pomodoro' may be one of the answers but is not requested.

**18, near miss.** A question about a method, not a request to run one. The word 'Pomodoro' is the overlap risk.

**19, near miss.** A full system. Focus time is one part of it.

**20, near miss.** Life balance, not a work block.

**21, near miss.** Establishing a recurring behaviour, not a single session.

**22, near miss.** Allocation of work, not focus.

**23, near miss.** Scope against a fixed deadline. No block is being set up.

**24, near miss.** Boundary of the whole project, before work starts. 'Done' overlaps with the card's done-line, but the scale differs.

**25, near miss.** Framing a non-trivial piece of work. The card is for a session, not a project.

**26, near miss.** An estimate check, not a block.

**27, near miss.** Channel choice.

**28, near miss.** A recurring meeting problem; belongs to the sibling repository, so this skill should not fire.

**29, near miss.** A finished draft needs a reader.

**30, near miss.** Stress-testing a plan, not running a block.

**31, near miss.** A retro on finished work. 'Done' appears, but the user is closing out a project, not a block.

**32, near miss.** Chat handoff.

**33, near miss.** Token economy.

**34, near miss.** Spend review.

**35, near miss.** A tool vetting request. The topic is focus but the task is vetting; no block is being set up.

**36, near miss.** Exit cost of a tool.

**37, near miss.** The menu request.

**38, ambiguous.** 'Concentrate' points to a block; 'drowning in tasks' points to prioritising. A chain (sort, then focus) is the likely good outcome.

**39, ambiguous.** Starting trouble plus a timer idea. get-unstuck diagnoses; this skill sets up a block. Decide after a run whether the split is acceptable.

**40, ambiguous.** Immediate need plus a pattern. Expected best behaviour: run the block, mention protect-my-focus once.

**41, ambiguous.** A recurring time-blocking request. Calendar edits depend on connectors, which are not required; the skill cannot see or change the calendar.

---

## Output check

Two cases to be checked by hand once a model is available.

**Case 3 (Pomodoro or 90 minutes).** The output should choose one format with a one-line reason and the runner-up, include a Focus Card with one task, a done-line, a first action, a parking lot, phone and notification handling and a break plan, and state once that Claude cannot keep time and the user sets the timer. It should not list formats as a menu or promise to remind the user.

**Case 8 (difficulty starting).** The output should offer strategies (shrink the first step, body doubling, a shorter block) framed as things to try. It should not name or suggest any condition. If the user's wording mentions an existing label, the output should still not diagnose.

**Case 5 (a bare 'Done').** With no card in the chat, the output should ask for the task and the done-line, then run the four-item debrief. It should not invent a session.


---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

| Case | Message | Expected | Haiku | Sonnet | Opus | Reading |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| start-a-focus-session#8 | "I can never start tasks even when I want to. Can we do a 15-minute block togethe" | start-a-focus-session | start-a-focus-session | start-a-focus-session | **get-unstuck** | Opus chose get-unstuck for "I can never start tasks". Overlap; both are defensible. |
| start-a-focus-session#41 | "Block off two hours on my calendar for deep work every morning." | start-a-focus-session or plan-my-week | start-a-focus-session | **none** | **none** | Calendar blocking is not a skill here. Acceptable. |
