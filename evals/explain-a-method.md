# Evaluation: explain-a-method

Routing cases for `explain-a-method`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 19. All three models matched on 19; Haiku 19, Sonnet 19, Opus 19.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used. Skills named below that are written concurrently (`find-my-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life`, `build-my-system`) must be present in the description set for the near misses to be meaningful.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "How does the Eisenhower matrix work?" | Should fire | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 2 | "Is Pomodoro actually worth it?" | Should fire | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 3 | "Time blocking vs task batching: what's the difference?" | Should fire | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 4 | "Walk me through the Ivy Lee method." | Should fire | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 5 | "Explain the Flibbertigibbet 4-3-2 productivity method to me." | Should fire (method not real; should say so) | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 6 | "Which productivity method should I use? Nothing works for me." | Near miss | find-my-method | find-my-method | find-my-method | find-my-method |
| 7 | "Plan my day using time blocking. I have a 9am meeting and a deadline at 5." | Near miss | plan-my-day | plan-my-day | plan-my-day | plan-my-day |
| 8 | "Review last week and plan the next one." | Near miss | plan-my-week | plan-my-week | plan-my-week | plan-my-week |
| 9 | "Here is my list. Sort it with Eisenhower." | Near miss | sort-my-tasks | sort-my-tasks | sort-my-tasks | sort-my-tasks |
| 10 | "Start a Pomodoro with me for this essay." | Near miss | start-a-focus-session | start-a-focus-session | start-a-focus-session | start-a-focus-session |
| 11 | "My team's pings and meetings are wrecking my focus. What do I do?" | Near miss | protect-my-focus | protect-my-focus | protect-my-focus | protect-my-focus |
| 12 | "Help me build a daily writing habit I can actually keep." | Near miss | build-a-habit | build-a-habit | build-a-habit | build-a-habit |
| 13 | "I work too much and see my kids too little. Help me balance things." | Near miss | balance-my-life | balance-my-life | balance-my-life | balance-my-life |
| 14 | "Set up Getting Things Done for me in Notion." | Near miss | build-my-system | build-my-system | build-my-system | build-my-system |
| 15 | "I'm stuck on this chapter." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 16 | "Where do I start on the grant application?" | Near miss | plan-the-work | plan-the-work | plan-the-work | plan-the-work |
| 17 | "Should I use time blocking, or would something else suit me better?" | Ambiguous | find-my-method | find-my-method | find-my-method | find-my-method |
| 18 | "Tell me about GTD, then tell me if I should use it. I'm a freelance designer." | Ambiguous | explain-a-method | explain-a-method | explain-a-method | explain-a-method |
| 19 | "How do I use the Pomodoro technique?" | Ambiguous | explain-a-method | explain-a-method | explain-a-method | explain-a-method |

---

## Notes on the cases

**1 to 4, should fire.** A named method and an explanation, evaluation or comparison. Case 4 is "walk me through one method", which is explicitly this skill's.

**5, method not real.** Routing is explain-a-method. The body must say it does not recognise the method and must not invent steps. This is checked by reading the output, not by routing.

**6, find-my-method.** No method named, a recommendation requested. The overlap is the word "method".

**7, plan-my-day.** The user names a method but wants today planned.

**8, plan-my-week.** A week to plan.

**9, sort-my-tasks.** A pasted list to rank. The method name is a parameter, not the question.

**10, start-a-focus-session.** "Start a Pomodoro with me" asks for a session now, not an explanation. Overlap on the word Pomodoro.

**11, protect-my-focus.** Interruptions from others.

**12, build-a-habit.** One habit to design.

**13, balance-my-life.** Time across life areas.

**14, build-my-system.** A setup in a named tool. A named method plus "set up" means a build, not an explanation.

**15 and 16, existing neighbours.** A stalled task and a start. No method named.

**17, ambiguous.** A named method with "or something else suit me better" asks for a recommendation. `find-my-method` is the predicted winner; a split is acceptable if the answer explains the method and hands off.

**18, ambiguous.** Two jobs in one message: explain GTD, then recommend. Predicted explain-a-method with a hand-off to `find-my-method`. Decide in writing after a run.

**19, ambiguous.** "How do I use" could be a walk-through (here) or `start-a-focus-session`. Predicted explain-a-method because no session is starting.

---

## Output check

One case to be checked by hand once a model is available: case 2. The output should contain what it is, a 10-minute start, a worked example, an evidence label from {Strong, Some, Mixed, Practice only} with one sentence, at least two ways it backfires, and a try-it-today step. It should contain no study by author or year and no percentage.

Case 5 check: the output states the method is not recognised, offers the closest real methods, and asks where the user heard of it.

Case 3 check: a comparison table and a pick-by-situation line.

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

No misses on cases with a single expected answer.
