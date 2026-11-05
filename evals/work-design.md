# Evaluation: work-design

Routing cases for `work-design`, the consultant. Written alongside the rewrite that turned the menu into a consultant. **Nothing has been recorded yet.** The Haiku, Sonnet and Opus columns read "not yet run" until the harness in `evals/README.md` is run; only the expected routing is filled in, and it is a prediction.

**Method.** Show a model the verbatim descriptions of all 29 skills (the 26 here plus the 3 in meeting-design) and ask for one skill name or `none`. Pin the description text used.

The risk this file exists to check is routing theft: a broad description such as "how can I work better" can pull messages away from the specific skills. The near misses are the important rows.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "work-design" | Should fire | work-design | not yet run | not yet run | not yet run |
| 2 | "How can I work better? I feel like I'm always busy but never getting anywhere." | Should fire | work-design | not yet run | not yet run | not yet run |
| 3 | "I run a small team and we're always behind. What should I change?" | Should fire | work-design | not yet run | not yet run | not yet run |
| 4 | "Look at how I work and tell me what to try." | Should fire | work-design | not yet run | not yet run | not yet run |
| 5 | "Ask work design: how should I organise my week as a freelancer?" | Should fire | work-design | not yet run | not yet run | not yet run |
| 6 | "I'm not sure what I need help with, I just feel disorganised." | Should fire | work-design | not yet run | not yet run | not yet run |
| 7 | "Coach me on my workflow." | Should fire | work-design | not yet run | not yet run | not yet run |
| 8 | "How should I manage my team's work? We have six people and no process." | Should fire | work-design | not yet run | not yet run | not yet run |
| 9 | "What should I change about how I work?" | Should fire | work-design | not yet run | not yet run | not yet run |
| 10 | "Where do I start on this report?" | Near miss | plan-the-work | not yet run | not yet run | not yet run |
| 11 | "I'm stuck on my thesis chapter." | Near miss | get-unstuck | not yet run | not yet run | not yet run |
| 12 | "Plan my day: I have six tasks and two meetings." | Near miss | plan-my-day | not yet run | not yet run | not yet run |
| 13 | "Plan my week." | Near miss | plan-my-week | not yet run | not yet run | not yet run |
| 14 | "I have too much to do, help me prioritise this list." | Near miss | sort-my-tasks | not yet run | not yet run | not yet run |
| 15 | "Is this email good enough to send?" | Near miss | review-my-work | not yet run | not yet run | not yet run |
| 16 | "Should this be a meeting or a message?" | Near miss | meeting-or-message | not yet run | not yet run | not yet run |
| 17 | "How does time blocking work?" | Near miss | explain-a-method | not yet run | not yet run | not yet run |
| 18 | "Set up my productivity system for me." | Near miss | build-my-system | not yet run | not yet run | not yet run |
| 19 | "I want to start running every morning but I keep quitting." | Near miss | build-a-habit | not yet run | not yet run | not yet run |
| 20 | "I'm working too much and I never see my family." | Near miss | balance-my-life | not yet run | not yet run | not yet run |
| 21 | "Help me focus for an hour on this proposal." | Near miss | start-a-focus-session | not yet run | not yet run | not yet run |
| 22 | "How long will this migration realistically take?" | Near miss | how-long-will-it-take | not yet run | not yet run | not yet run |
| 23 | "What could go wrong with my launch plan?" | Near miss | what-could-go-wrong | not yet run | not yet run | not yet run |
| 24 | "I get interrupted all day and can't do deep work." | Near miss | protect-my-focus | not yet run | not yet run | not yet run |
| 25 | "What productivity method should I use? I can never get started on things." | Near miss | find-my-method | not yet run | not yet run | not yet run |
| 26 | "I've tried everything and nothing sticks. Help me." | Ambiguous | find-my-method or work-design | not yet run | not yet run | not yet run |
| 27 | "Any tips for being more productive?" | Ambiguous | work-design or find-my-method | not yet run | not yet run | not yet run |
| 28 | "How should I approach this big project?" | Ambiguous | plan-the-work or work-design | not yet run | not yet run | not yet run |
| 29 | "How do I run better one-on-ones with my team?" | Ambiguous | meeting-design or work-design | not yet run | not yet run | not yet run |
| 30 | "Remind me what skills I have for work." | Ambiguous | work-design or none | not yet run | not yet run | not yet run |

---

## What each group tests

**1 to 9, should fire.** Open-ended asks for help with how someone works, including a team lead and a freelancer, and the bare name. None names a specific method or skill.

**10 to 25, near misses.** Every sibling's own trigger phrase. The consultant must step aside on all of them. A miss here is routing theft and the first thing to fix, by tightening the consultant's description, not by widening the sibling's.

**26 to 30, ambiguous.** Cases two skills could claim. A split is acceptable where both answers lead somewhere useful.

## Output check (by hand)

Put case 3 to the skill with a calendar showing mostly meetings. The Read should: list what it looked at; ask before opening any calendar; give at most three suggestions with the first marked "try this week"; carry an evidence label from the library on each; name what to leave alone; and end with what it assumed. It must not write, send or schedule anything.
