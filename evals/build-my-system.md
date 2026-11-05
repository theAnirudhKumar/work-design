# Evaluation: build-my-system

Routing cases for `build-my-system`, written alongside the skill. **No results are recorded.** The Haiku, Sonnet and Opus columns read "not yet run" because these cases have not been put to any model. Only the expected routing is filled in, and it is a prediction from reading the descriptions, not a finding.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used. Skills named below that are not in the repository must be present in the description set. Near misses name skills that are being added alongside this one (`find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`); their descriptions must be in the set.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Set up my productivity system. I have notes everywhere and I keep dropping things." | Should fire | build-my-system | not yet run | not yet run | not yet run |
| 2 | "Organise my life. I use a paper planner, three apps and sticky notes." | Should fire | build-my-system | not yet run | not yet run | not yet run |
| 3 | "Make me hyper-productive. Build me a workflow from scratch." | Should fire | build-my-system | not yet run | not yet run | not yet run |
| 4 | "I'm a freelancer with a phone and a spreadsheet. Where should my tasks, notes and ideas live?" | Should fire | build-my-system | not yet run | not yet run | not yet run |
| 5 | "I keep starting new systems and abandoning them. Help me build one I'll keep." | Should fire | build-my-system | not yet run | not yet run | not yet run |
| 6 | "Here is my my-system.md. Update it, I'm dropping my task app." | Should fire | build-my-system | not yet run | not yet run | not yet run |
| 7 | "Which productivity method should I use? I'm always behind." | Near miss | find-my-method | not yet run | not yet run | not yet run |
| 8 | "How does Pomodoro work? Is it worth trying?" | Near miss | explain-a-method | not yet run | not yet run | not yet run |
| 9 | "Plan my day: meeting at 10, report due, gym at 6." | Near miss | plan-my-day | not yet run | not yet run | not yet run |
| 10 | "Plan my week and do my weekly review." | Near miss | plan-my-week | not yet run | not yet run | not yet run |
| 11 | "I have too much on my list and don't know what to do first." | Near miss | sort-my-tasks | not yet run | not yet run | not yet run |
| 12 | "Start a 25 minute focus session with me." | Near miss | start-a-focus-session | not yet run | not yet run | not yet run |
| 13 | "Meetings and Slack eat my day. How do I stop the interruptions?" | Near miss | protect-my-focus | not yet run | not yet run | not yet run |
| 14 | "I want to read every night but I keep forgetting." | Near miss | build-a-habit | not yet run | not yet run | not yet run |
| 15 | "I work too much and never see my family. Where does my time go?" | Near miss | balance-my-life | not yet run | not yet run | not yet run |
| 16 | "I'm about to start the annual report, where do I start?" | Near miss | plan-the-work | not yet run | not yet run | not yet run |
| 17 | "Should I use Notion or Obsidian? Which is worth paying for?" | Near miss | before-you-install | not yet run | not yet run | not yet run |
| 18 | "I'm switching from Todoist to a paper system. What do I lose?" | Near miss | before-you-switch | not yet run | not yet run | not yet run |
| 19 | "Which of my subscriptions overlap? I pay for four task apps." | Near miss | audit-my-tools | not yet run | not yet run | not yet run |
| 20 | "Summarise this chat so I can continue it tomorrow." | Near miss | continue-in-new-chat | not yet run | not yet run | not yet run |
| 21 | "I'm drowning, I need a system for work and home." | Ambiguous | build-my-system or balance-my-life | not yet run | not yet run | not yet run |
| 22 | "I use GTD and it's not working. What should I change?" | Ambiguous | build-my-system or find-my-method | not yet run | not yet run | not yet run |
| 23 | "Help me get organised for the new semester." | Ambiguous | build-my-system or plan-my-week | not yet run | not yet run | not yet run |

---

## What each case tests

**1 to 6, should fire.** Trigger phrases across a general worker, a messy multi-tool user, a freelancer with no app, a repeat abandoner and a returning user with a pasted profile. Case 6 tests that an existing my-system.md leads to an audit, not a rebuild.

**7 to 14, the new neighbours.** Each asks for one narrow thing: a method choice, a method explanation, today, this week, a ranked list, one focus hour, interruptions, one habit. The word "system" or "workflow" is absent from them.

**15, balance-my-life.** Time across life, not tools.

**16 to 20, existing skills.** Case 17 is a tool-choice question (`before-you-install`), case 18 is a leaving question (`before-you-switch`), case 19 is overlapping subscriptions (`audit-my-tools`). The word "task app" is the risk.

**21 to 23, ambiguous.** Case 21 overlaps balance-my-life through "work and home". Case 22 asks about a named method and its fit, which find-my-method also covers; build-my-system should win only if the user wants the whole structure reviewed. Case 23 could be a semester plan or a system. Decide in writing after a run whether the split is acceptable.

**Output checks by reading, not routing.** The reply must tell the user to save my-system.md and paste it into future chats, cap new methods at three, show a rhythm table with minutes that adds up, and never require buying anything.
