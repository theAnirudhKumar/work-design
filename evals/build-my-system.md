# Evaluation: build-my-system

Routing cases for `build-my-system`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 23. All three models matched on 23; Haiku 23, Sonnet 23, Opus 23.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used. Skills named below that are not in the repository must be present in the description set. Near misses name skills that are being added alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`); their descriptions must be in the set.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Set up my productivity system. I have notes everywhere and I keep dropping things." | Should fire | build-my-system | build-my-system | build-my-system | build-my-system |
| 2 | "Organise my life. I use a paper planner, three apps and sticky notes." | Should fire | build-my-system | build-my-system | build-my-system | build-my-system |
| 3 | "Make me hyper-productive. Build me a workflow from scratch." | Should fire | build-my-system | build-my-system | build-my-system | build-my-system |
| 4 | "I'm a freelancer with a phone and a spreadsheet. Where should my tasks, notes and ideas live?" | Should fire | build-my-system | build-my-system | build-my-system | build-my-system |
| 5 | "I keep starting new systems and abandoning them. Help me build one I'll keep." | Should fire | build-my-system | build-my-system | build-my-system | build-my-system |
| 6 | "Here is my my-system.md. Update it, I'm dropping my task app." | Should fire | build-my-system | build-my-system | build-my-system | build-my-system |
| 7 | "Which productivity method should I use? I'm always behind." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 8 | "How does Pomodoro work? Is it worth trying?" | Near miss | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 9 | "Plan my day: meeting at 10, report due, gym at 6." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 10 | "Plan my week and do my weekly review." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 11 | "I have too much on my list and don't know what to do first." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 12 | "Start a 25 minute focus session with me." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 13 | "Meetings and Slack eat my day. How do I stop the interruptions?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 14 | "I want to read every night but I keep forgetting." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 15 | "I work too much and never see my family. Where does my time go?" | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 16 | "I'm about to start the annual report, where do I start?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 17 | "Should I use Notion or Obsidian? Which is worth paying for?" | Near miss | before-you-install | before-you-install | before-you-install | before-you-install |
| 18 | "I'm switching from Todoist to a paper system. What do I lose?" | Near miss | before-you-switch | before-you-switch | before-you-switch | before-you-switch |
| 19 | "Which of my subscriptions overlap? I pay for four task apps." | Near miss | audit-my-tools | audit-my-tools | audit-my-tools | audit-my-tools |
| 20 | "Summarise this chat so I can continue it tomorrow." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 21 | "I'm drowning, I need a system for work and home." | Ambiguous | build-my-system or balance-my-life | build-my-system | build-my-system | build-my-system |
| 22 | "I use GTD and it's not working. What should I change?" | Ambiguous | build-my-system or find-my-method | build-my-system | build-my-system | build-my-system |
| 23 | "Help me get organised for the new semester." | Ambiguous | build-my-system or plan-my-week | build-my-system | build-my-system | build-my-system |

---

## What each case tests

**1 to 6, should fire.** Trigger phrases across a general worker, a messy multi-tool user, a freelancer with no app, a repeat abandoner and a returning user with a pasted profile. Case 6 tests that an existing my-system.md leads to an audit, not a rebuild.

**7 to 14, the new neighbours.** Each asks for one narrow thing: a method choice, a method explanation, today, this week, a ranked list, one focus hour, interruptions, one habit. The word "system" or "workflow" is absent from them.

**15, balance-my-life.** Time across life, not tools.

**16 to 20, existing skills.** Case 17 is a tool-choice question (`before-you-install`), case 18 is a leaving question (`before-you-switch`), case 19 is overlapping subscriptions (`audit-my-tools`). The word "task app" is the risk.

**21 to 23, ambiguous.** Case 21 overlaps balance-my-life through "work and home". Case 22 asks about a named method and its fit, which find-my-method also covers; build-my-system should win only if the user wants the whole structure reviewed. Case 23 could be a semester plan or a system. Decide in writing after a run whether the split is acceptable.

**Output checks by reading, not routing.** The reply must tell the user to save my-system.md and paste it into future chats, cap new methods at three, show a rhythm table with minutes that adds up, and never require buying anything.

## Misses and how to read them

No misses on cases with a single expected answer.
