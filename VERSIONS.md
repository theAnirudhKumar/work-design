# Versions

What changed, and when.

## 4.2.1

**Fact-checked the method library.** All 137 cards were checked against web sources for attribution, dates and how strongly the evidence line is worded. About 56 edits resulted: attributions corrected or made more precise (the 20-20-20 rule, Wheel of Life, OKRs, SMART, Eat the frog, Feynman technique, SQ3R, Cornell notes and others), evidence sentences softened or grounded where they overreached (habit tracking, micro-breaks, Personal retrospective, Wins log, Deliberate practice), and one definition corrected: the radical candor card said candor without care is "just criticism", which contradicts the framework (its author calls that obnoxious aggression). One label changed: Habit stacking went from Some to Practice only, because its own sentence admitted there is little direct testing. The library now reads 4 Strong, 24 Some, 10 Mixed, 99 Practice only.

**Added a plugin icon and one-step install lines** (`/plugin install work-design --marketplace theAnirudhKumar/work-design`, Claude Code 2.1.275 or later). Anthropic's plugin validator warns without an icon, and the listing icon is set only the first time a plugin is saved or submitted.

**Refreshed the per-skill eval tables** with the second routing run, so every file shows the same description snapshot.

**Caveats.** The check used web search; many primary sources (publishers, author sites, Wikipedia) were not reachable from the sandbox, so some corrections rest on secondary sources. Still weakest: Flowtime's attribution to Zoe Read-Bivens, the 1941 versus 1946 date for SQ3R, the 1950s date for Cornell notes, Grove's 1983 date for one-on-ones, the exact Bezos letter for two-way doors, and the 2014 date for 52/17. Evidence labels were not re-derived from the studies, only checked for overstatement.

## 4.2.0

**Work Design is now a consultant.** The `work-design` skill used to be a menu that asked which stage you were at. It now reads the context your AI tool already holds (the conversation, loaded notes or memory, a pasted `my-system.md`), notices patterns, and suggests one to three methods, working styles or management practices, each with the reason, an honest evidence label and the skill that runs it. It asks before looking at a connected calendar or task list, reads one week read-only, says what it looked at, and never writes anything. It tells you what to leave alone, and defers at once when your message already names a specific skill's job.

**Added a signals table and a guard for it.** `skills/work-design/references/signals-to-methods.md` maps 30 observable signals ("calendar is mostly meetings", "same task moved three times", "unclear who owns what") to methods. `validate-skills.py` now fails if any method name or evidence label in that table does not match its card in the library.

**Added ten management methods.** One-on-ones, weekly team planning, team retrospective, WIP limits, team Kanban board, situational leadership, radical candor, skip-level meetings, written weekly updates and team pre-mortem. The library is now 137 methods. All ten are rated Practice only, and the cards say where a model is popular but weakly tested.

**Caveats.** Making a skill broad risks stealing routing from the specific ones, so the full suite (551 cases) was rerun on Haiku, Sonnet and Opus against the new description. All 9 open-ended cases went to the consultant, all 16 near misses stayed with their specific skills, and 1 of 1,563 earlier picks moved to it. Matches on the 504 single-answer cases were 97.0%, 97.2% and 97.2%; about 6% of picks differ between two runs of the same case, so single flips are noise. Details are in `evals/README.md`. Evidence labels and attributions on the new cards were written from memory.

## 4.1.0

**Added a second half: get more done.** Ten skills that help a person pick a productivity method that fits, set it up and follow it: `find-my-method`, `explain-a-method`, `plan-my-day`, `plan-my-week`, `sort-my-tasks`, `start-a-focus-session`, `protect-my-focus`, `build-a-habit`, `balance-my-life` and `build-my-system`. They install separately as the `get-more-done` plugin, and `work-design` (the menu skill) now knows about them.

**Added a library of 127 methods.** Pomodoro, time blocking, task batching, Eisenhower, Ivy Lee, Getting Things Done, Tiny Habits and 120 more, each with a 10-minute start, a 7-day trial, a "skip it when" line and an evidence label. Ratings are deliberately conservative: 4 Strong, 25 Some, 10 Mixed, 88 Practice only. The cards are in `skills/find-my-method/references/`, with an index, and `METHODS.md` lists them all.

**Introduced the `my-system.md` profile.** `build-my-system` writes it and the other skills read it when it is pasted, so the methods a person chose carry across conversations. Claude does not remember between conversations; the user saves the file.

**Caveats.** Attributions and evidence labels were written from memory and are the first thing to check; a few are marked as disputed on the card. The thresholds in the trial scorecard (keep at 5 of 7 days, drop under 3) and the slack and caps in the planning skills are rules of thumb, labelled as such. Every skill has an eval file, and all of them were run once on 5 Nov 2026 against Haiku, Sonnet and Opus with all 29 descriptions shown together (one sample per case; the log is in `evals/README.md`). On the 474 cases with a single expected answer the models matched 96.2%, 97.3% and 97.7% of the time, and many misses are stale expectations or overlaps where either answer helps. The run found one real collision (`protect-my-focus` against `meeting-audit` on meeting-heavy calendars), which the 4.1.0 wording fixes.

## 4.0.0

**Refocused on the quality of the work itself.** The first nine skills covered tools, hand-offs and setup. The set now follows one piece of work from start to finish, because quality is decided at a few predictable moments: a vague start, an unbounded scope, an untested plan, getting stuck, a draft nobody really reads, and lessons nobody keeps. Six new skills cover them: `plan-the-work` (a one-page Work Card, the flagship), `fit-to-deadline`, `what-could-go-wrong`, `get-unstuck`, `review-my-work` and `lessons-learned`. A seventh, `work-design`, is a menu that names the right skill when someone cannot remember one.

**Renamed twelve skills so the name is the sentence you would say.** `how-long-will-it-take` (was `estimate-from-precedent`), `meeting-or-message` (was `pick-the-medium`), `before-you-switch` (was `switch-cost`), `audit-my-tools` (was `stack-audit`), `continue-in-new-chat` (was `chat-context`), `cut-token-cost` (was `optimize-tokens`). `scope-the-work`, `delegate` and `before-you-install` keep their names. Anyone who installed a skill by its old name needs to reinstall under the new one. Recorded eval results in the older eval files were gathered under the old names and descriptions.

**Reorganised the README by moment, not by theme.** A "which one do I need" table keyed on what you are thinking, a start-here set of three, and a Work Card example at the top.

**Fixed version drift for good.** `validate-skills.py` now fails if `plugin.json`, `marketplace.json` and the newest heading here disagree. The manifests had said 2.0.0 while this file said 3.0.0.

**Caveats.** None of the new skills has been run against Haiku, Sonnet or Opus. Their eval files carry the prompts and the expected routing, and every results column reads "not yet run". Routing between near neighbours (`get-unstuck` and `plan-the-work`, `what-could-go-wrong` and `review-my-work`) is the first thing to test. `chat-context` and `optimize-tokens` are also copied in a separate workspace template; this repository is the canonical source, so refresh those copies from here.

## 3.0.0

**Added three skills to Tool lifecycle and Working with agents.** `delegate` (#3), splitting a single piece of work into an allocation table across you, another person or a model, each part carrying a check and a stop condition. `audit-my-tools` (#13), auditing tools already paid for into a keep, cancel, downgrade or consolidate verdict. `before-you-switch` (#19), checking what breaks on the way out of a tool already in use, closing the Tool lifecycle category as scoped.

**Opened a third category, Deciding how work runs.** `meeting-or-message` (#21) picks the channel for one piece of communication before it happens and hands off to a meeting-design skill the moment a meeting is the answer; its boundary against `meeting-design` was resolved by reading that skill's actual shipped description in the sibling `theAnirudhKumar/meeting-design` repository rather than assuming one. `scope-the-work` (#23) draws the in/out/done boundary of a piece of work before it starts. `how-long-will-it-take` (#25) corrects a time estimate against a reference class of ordinary past cases, built on the planning fallacy (Buehler, Griffin & Ross, 1994) and reference class forecasting (Flyvbjerg, 2006), and closes the duration-estimate gap `scope-the-work`'s own eval named.

**Added the evaluations harness and backfilled it across every skill.** `evals/README.md` plus one file per skill, each run against Haiku, Sonnet and Opus with results recorded honestly, including disagreements (#5). Every skill added since carries its own eval from the day it shipped.

**Fixed two routing bugs.** `cut-token-cost`'s proactive trigger fired inconsistently across models; rewritten to name request shapes instead of asking the model for a judgement call. A cost-shaped complaint was falling through every skill instead of reaching `continue-in-new-chat` (#11).

**Rewrote the README.** Replaced the three-paragraph, citation-heavy opening with plain what/why/how text, moved the academic citation into its own Research section at the bottom (#15). Regrouped the flat skills table into the three category tables that now structure the whole document (#17), and kept them in sync as each new skill shipped.

## 2.0.0

**Renamed from `skills` to `work-design`.** The old name said nothing about what was inside, and what was inside was two unrelated groups of skills. GitHub keeps a permanent redirect, so the old repository URL still resolves.

The marketplace is now `work-design-marketplace` and the plugin is `work-design`, replacing `cowork-skills` and `workflow-skills`. Reinstall with the strings in the README.

**Added `before-you-install`,** moved from the `tool-decisions` repository, which has been retired into this one. Vets a tool before signup across five checks and ends on install, install with conditions, or do not install.

**Removed `call-recap-follow-up` and `email-critic`.** Both are maintained in `CSPulse/customer-success-skills`, which is where anyone looking for customer-facing skills should land. Two copies of a skill drift; one does not.

**Added the contribution surface.** `validate-skills.py`, a GitHub Actions workflow running it on every pull request, `CONTRIBUTING.md`, issue and pull request templates, and a gitignore. The structural rules were previously enforced only by a local hook, so anyone arriving by fork had nothing to run.

**Fixed.** The H1 in `continue-in-new-chat` did not match its folder. The description on `call-recap-follow-up` was 1,096 characters against the 1,024 limit, putting its trigger phrases in the range assistants truncate; that skill has moved, and the copy in the customer success library is the one to fix.

## 1.0.0

First release, as `skills`. Four skills: `call-recap-follow-up`, `continue-in-new-chat`, `email-critic`, `cut-token-cost`.
