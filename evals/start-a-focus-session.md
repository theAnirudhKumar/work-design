# Evaluation: start-a-focus-session

Routing cases for `start-a-focus-session`, written alongside the skill. **No results are recorded.** The Haiku, Sonnet and Opus columns read "not yet run" because these cases have not been put to any model. Only the expected routing is filled in, and it is a prediction from reading the descriptions, not a finding.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. The set must include the skills built alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `balance-my-life`, `build-my-system`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`) and, for the meeting cases, `meeting-audit` from the sibling meeting-design repository, or the near misses are not meaningful. `meeting-design` is the set that contains `meeting-audit`. An Expected value written as A or B means either routing is defensible.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Help me focus for an hour, I have to finish the methods section of my dissertation." | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 2 | "Start a Pomodoro for me, I need to clear my expense receipts." | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 3 | "Pomodoro or a 90-minute block for writing a chapter? Set me up." | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 4 | "I keep sitting down at my desk and not actually working. Can you structure the next two hours?" | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 5 | "Done. Got through the whole outline." | Should fire (debrief) | start-a-focus-session | not yet run | not yet run | not yet run |
| 6 | "I got interrupted at about 40 minutes by a phone call from the bank." | Should fire (debrief) | start-a-focus-session | not yet run | not yet run | not yet run |
| 7 | "I didn't finish. I only got half the slides done and kept checking Slack." | Should fire (debrief) | start-a-focus-session | not yet run | not yet run | not yet run |
| 8 | "I can never start tasks even when I want to. Can we do a 15-minute block together on my tax return?" | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 9 | "I'm working in an open office and need 90 minutes on the brand deck." | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 10 | "I want to write song lyrics for a couple of hours, but timers kill my flow." | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 11 | "I'm on a quiet shift and have 25 minutes before handover. Help me use it to finish my charting." | Should fire | start-a-focus-session | not yet run | not yet run | not yet run |
| 12 | "I'm constantly interrupted at work. Slack, people at my desk, meetings. Fix it." | Near miss | protect-my-focus | not yet run | not yet run | not yet run |
| 13 | "Plan my day. I have a dentist at 2 and a pile of work." | Near miss | plan-my-day | not yet run | not yet run | not yet run |
| 14 | "Plan my week, I have a launch on Thursday." | Near miss | plan-my-week | not yet run | not yet run | not yet run |
| 15 | "I have 40 things on my list and no idea what to do first. Rank them." | Near miss | sort-my-tasks | not yet run | not yet run | not yet run |
| 16 | "I can't get started on my proposal, I don't even know why." | Near miss | get-unstuck | not yet run | not yet run | not yet run |
| 17 | "Which productivity method should I use? I've tried a few and none stuck." | Near miss | find-my-method | not yet run | not yet run | not yet run |
| 18 | "How does the Pomodoro technique work and is it worth it?" | Near miss | explain-a-method | not yet run | not yet run | not yet run |
| 19 | "Set up my whole productivity system: capture, planning, focus, review." | Near miss | build-my-system | not yet run | not yet run | not yet run |
| 20 | "I never see my family and work every evening. Help me find some balance." | Near miss | balance-my-life | not yet run | not yet run | not yet run |
| 21 | "I want to start meditating every morning and make it stick." | Near miss | build-a-habit | not yet run | not yet run | not yet run |
| 22 | "Which of these three tasks is worth my time, and which should I hand to an agent?" | Near miss | delegate | not yet run | not yet run | not yet run |
| 23 | "I have two days to finish the report. What should I cut?" | Near miss | fit-to-deadline | not yet run | not yet run | not yet run |
| 24 | "Before I start this project, what is in scope and what counts as done?" | Near miss | scope-the-work | not yet run | not yet run | not yet run |
| 25 | "I have to write a market analysis. Where do I start?" | Near miss | plan-the-work | not yet run | not yet run | not yet run |
| 26 | "How long will this chapter take me to write? I think about three hours." | Near miss | how-long-will-it-take | not yet run | not yet run | not yet run |
| 27 | "Should we have a call about this or can I just message them?" | Near miss | meeting-or-message | not yet run | not yet run | not yet run |
| 28 | "Our weekly team meeting wastes everyone's time. Fix it." | Near miss | meeting-audit (meeting-design set) | not yet run | not yet run | not yet run |
| 29 | "Review this email draft before I send it." | Near miss | review-my-work | not yet run | not yet run | not yet run |
| 30 | "What could go wrong with my study plan?" | Near miss | what-could-go-wrong | not yet run | not yet run | not yet run |
| 31 | "That's done, what did I learn from it?" | Near miss | lessons-learned | not yet run | not yet run | not yet run |
| 32 | "Hand off this chat so I can continue in a new one." | Near miss | continue-in-new-chat | not yet run | not yet run | not yet run |
| 33 | "Make my prompts use fewer tokens." | Near miss | cut-token-cost | not yet run | not yet run | not yet run |
| 34 | "Audit our software subscriptions, which should I cancel?" | Near miss | audit-my-tools | not yet run | not yet run | not yet run |
| 35 | "Should I install this focus app? Check their privacy policy." | Near miss | before-you-install | not yet run | not yet run | not yet run |
| 36 | "What breaks if I switch from this timer app to another?" | Near miss | before-you-switch | not yet run | not yet run | not yet run |
| 37 | "Which work-design skill should I use for my next task?" | Near miss | work-design | not yet run | not yet run | not yet run |
| 38 | "I need to concentrate this afternoon, and also I'm drowning in tasks." | Ambiguous | start-a-focus-session or sort-my-tasks | not yet run | not yet run | not yet run |
| 39 | "Help me get started on this essay. Maybe a timer would help." | Ambiguous | start-a-focus-session or get-unstuck | not yet run | not yet run | not yet run |
| 40 | "Meetings and Slack kill my focus time. I need a focus session this afternoon." | Ambiguous | start-a-focus-session or protect-my-focus | not yet run | not yet run | not yet run |
| 41 | "Block off two hours on my calendar for deep work every morning." | Ambiguous | start-a-focus-session or plan-my-week | not yet run | not yet run | not yet run |

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
