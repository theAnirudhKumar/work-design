# Evaluation: work-design

Routing cases for `work-design`, the consultant. Written alongside the rewrite that turned the menu into a consultant. **Run on:** 5 Nov 2026, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 here plus 3 in meeting-design), snapshot `731601fe12b6`. A cell is the skill that model picked; **bold** means it differs from the expected answer. One sample per case. Result: all three models gave an acceptable answer on all 30 cases (25 have one expected answer; 5 are ambiguous with two acceptable answers, and the models split on two of them, which is fine). No near miss was pulled to `work-design`. The overall log is in `evals/README.md`.

**Method.** Show a model the verbatim descriptions of all 29 skills (the 26 here plus the 3 in meeting-design) and ask for one skill name or `none`. Pin the description text used.

The risk this file exists to check is routing theft: a broad description such as "how can I work better" can pull messages away from the specific skills. The near misses are the important rows.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "work-design" | Should fire | work-design | work-design | work-design | work-design |
| 2 | "How can I work better? I feel like I'm always busy but never getting anywhere." | Should fire | work-design | work-design | work-design | work-design |
| 3 | "I run a small team and we're always behind. What should I change?" | Should fire | work-design | work-design | work-design | work-design |
| 4 | "Look at how I work and tell me what to try." | Should fire | work-design | work-design | work-design | work-design |
| 5 | "Ask work design: how should I organise my week as a freelancer?" | Should fire | work-design | work-design | work-design | work-design |
| 6 | "I'm not sure what I need help with, I just feel disorganised." | Should fire | work-design | work-design | work-design | work-design |
| 7 | "Coach me on my workflow." | Should fire | work-design | work-design | work-design | work-design |
| 8 | "How should I manage my team's work? We have six people and no process." | Should fire | work-design | work-design | work-design | work-design |
| 9 | "What should I change about how I work?" | Should fire | work-design | work-design | work-design | work-design |
| 10 | "Where do I start on this report?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 11 | "I'm stuck on my thesis chapter." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 12 | "Plan my day: I have six tasks and two meetings." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 13 | "Plan my week." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 14 | "I have too much to do, help me prioritise this list." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 15 | "Is this email good enough to send?" | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 16 | "Should this be a meeting or a message?" | Near miss | meeting-or-message | meeting-or-message | meeting-or-message | meeting-or-message |
| 17 | "How does time blocking work?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 18 | "Set up my productivity system for me." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 19 | "I want to start running every morning but I keep quitting." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 20 | "I'm working too much and I never see my family." | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 21 | "Help me focus for an hour on this proposal." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 22 | "How long will this migration realistically take?" | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 23 | "What could go wrong with my launch plan?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 24 | "I get interrupted all day and can't do deep work." | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 25 | "What productivity method should I use? I can never get started on things." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 26 | "I've tried everything and nothing sticks. Help me." | Ambiguous | find-my-method or work-design | find-my-method | find-my-method | find-my-method |
| 27 | "Any tips for being more productive?" | Ambiguous | work-design or find-my-method | work-design | work-design | work-design |
| 28 | "How should I approach this big project?" | Ambiguous | plan-the-work or work-design | plan-the-work | plan-the-work | plan-the-work |
| 29 | "How do I run better one-on-ones with my team?" | Ambiguous | meeting-design or work-design | work-design | meeting-design | work-design |
| 30 | "Remind me what skills I have for work." | Ambiguous | work-design or none | none | work-design | work-design |

---

## What each group tests

**1 to 9, should fire.** Open-ended asks for help with how someone works, including a team lead and a freelancer, and the bare name. None names a specific method or skill.

**10 to 25, near misses.** Every sibling's own trigger phrase. The consultant must step aside on all of them. A miss here is routing theft and the first thing to fix, by tightening the consultant's description, not by widening the sibling's.

**26 to 30, ambiguous.** Cases two skills could claim. A split is acceptable where both answers lead somewhere useful.

## Output check (by hand)

Put case 3 to the skill with a calendar showing mostly meetings. The Read should: list what it looked at; ask before opening any calendar; give at most three suggestions with the first marked "try this week"; carry an evidence label from the library on each; name what to leave alone; and end with what it assumed. It must not write, send or schedule anything.
