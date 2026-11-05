# Signals to methods

What to notice, where it shows up, what to suggest, and which skill runs it. Method names and evidence labels match the library in `find-my-method`; a check in `validate-skills.py` fails the build if they drift. Evidence labels: **Strong** = repeated controlled studies support the core mechanism; **Some** = supportive but small or indirect; **Mixed** = studies conflict or effects depend on the person; **Practice only** = widely used, little direct testing.

Rules for using this table: match a signal only on evidence from the context, suggest at most three things, make the first one small, and never read a row as a diagnosis of the person. A signal points to a candidate. The user's constraints decide.

## Time and attention

| Signal | Seen in | Suggest | Run it with |
| :--- | :--- | :--- | :--- |
| Calendar is mostly meetings; no free block over 90 minutes | Calendar, or "I never get time to think" | Meeting-free blocks (Practice only); Maker's schedule (Practice only) | `protect-my-focus` |
| Days start reactive, driven by the inbox | Conversation, tasks | Most Important Tasks (Practice only); Time blocking (Some) | `plan-my-day` |
| Many small admin tasks scattered through the day | Tasks, conversation | Task batching (Some) | `plan-my-day` |
| Distracted by phone and notifications | Conversation | Notification batching (Some); Phone-away rule (Mixed) | `start-a-focus-session` |
| Hard task keeps not getting started | Conversation, tasks | Five-minute rule (Practice only); Implementation intentions (Strong) | `get-unstuck` |
| Same task moved more than twice | Task list | Tiny first step (Practice only); Eat the frog (Practice only) | `get-unstuck` |
| Work expands to fill time; deadlines slip | Conversation | Timeboxing (Practice only); Parkinson's-law deadlines (Mixed) | `fit-to-deadline` |
| Energy drops at predictable times | Conversation | Prime-time scheduling (Some); Energy audit (Practice only) | `plan-my-day` |
| Long stretches at a desk, fatigue by afternoon | Conversation | Micro-breaks (Some); Walking breaks (Some) | `start-a-focus-session` |

## Lists, systems and planning

| Signal | Seen in | Suggest | Run it with |
| :--- | :--- | :--- | :--- |
| List is long and everything is urgent | Task list | Eisenhower matrix (Practice only); Ivy Lee method (Practice only) | `sort-my-tasks` |
| Ideas, tasks and notes scattered across places | Notes, conversation | Brain dump (Some); Getting Things Done (Practice only) | `build-my-system` |
| Has a system but never reviews it | Memory, `my-system.md` | Weekly review (Practice only) | `plan-my-week` |
| Has tried many systems and none stuck | Conversation, memory | Minimum viable habit (Practice only); Habit tracking (Some) | `find-my-method` |
| Goals vague, year drifting | Conversation | SMART goals (Some); Annual theme (Practice only) | `plan-my-week` |
| Projects overrun their scope | Conversation, past projects | Milestone mapping (Practice only); Working backwards (Practice only) | `plan-the-work` |
| Always firefighting, never learning from it | Conversation | Personal retrospective (Some); Wins log (Some) | `lessons-learned` |
| Self-employed with irregular hours | Conversation | Day theming (Practice only); Ideal week (Practice only) | `plan-my-week` |

## Habits, life and learning

| Signal | Seen in | Suggest | Run it with |
| :--- | :--- | :--- | :--- |
| Starts several habits at once and drops them | Conversation | Habit stacking (Some); Minimum viable habit (Practice only) | `build-a-habit` |
| Works late most evenings; no stopping point | Conversation, calendar | Work stop time (Some); Shutdown ritual (Some) | `balance-my-life` |
| Work crowds out health, family or friends | Conversation | Wheel of Life (Practice only); Weekly time together (Practice only) | `balance-my-life` |
| Personal admin piling up | Conversation | Life admin hour (Practice only); Errand batching (Practice only) | `build-a-habit` |
| Big decisions stall | Conversation | Weighted decision matrix (Some); Two-way door decisions (Practice only) | `explain-a-method` |
| Studying or learning without retaining | Conversation | Spaced repetition (Strong); Active recall (Strong) | `explain-a-method` |

## Leading a team

| Signal | Seen in | Suggest | Run it with |
| :--- | :--- | :--- | :--- |
| Unclear who owns what; handoffs drop | Conversation, team notes | RACI (Practice only); Directly responsible individual (Practice only) | `delegate` |
| Leader is the bottleneck; little delegated | Conversation | Delegation levels (Practice only); Situational leadership (Practice only) | `delegate` |
| Many status meetings | Calendar | Async-first (Practice only); Written weekly updates (Practice only) | `meeting-audit` (separate meeting-design set) |
| Decisions keep being reopened | Conversation, meeting notes | Decision log (Practice only) | `meeting-close` (separate meeting-design set) |
| One-to-ones missing or turning into status reports | Calendar, conversation | One-on-ones (Practice only) | `meeting-design` (separate meeting-design set) |
| Team starts everything, finishes little | Conversation, board | WIP limits (Practice only); Team Kanban board (Practice only) | `explain-a-method` |
| Team week has no shared plan | Conversation | Weekly team planning (Practice only) | `plan-my-week` |
| The same problems recur project after project | Conversation | Team retrospective (Practice only) | `lessons-learned` |
| A risky launch with a confident plan | Conversation | Team pre-mortem (Practice only) | `what-could-go-wrong` |
| Feedback avoided or harsh | Conversation | Radical candor (Practice only) | `explain-a-method` |
| Leader out of touch with the people two levels down | Conversation | Skip-level meetings (Practice only) | `explain-a-method` |
