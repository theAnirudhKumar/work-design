# Evaluation: lessons-learned

Routing cases for `lessons-learned`, written alongside the skill.

**Run on:** 5 Nov 2026, second run with the 4.2.0 descriptions, Haiku, Sonnet and Opus (run as model subagents), each shown only the verbatim descriptions of all 29 skills (26 in this repository plus the 3 in meeting-design), description snapshot `731601fe12b6`. Judged on the description alone. A cell is the skill that model picked; **bold** means it differs from the expected answer. Cases with a single expected answer: 14. All three models matched on 14; Haiku 14, Sonnet 14, Opus 14.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. Skills named below that are not yet in the repository (`review-my-work`, `what-could-go-wrong`, `get-unstuck`) must be present in the description set for the near misses to be meaningful. `meeting-close` lives in a separate repository and should be included as a description if the case is to mean anything.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "That's done, what did we learn?" | Should fire | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 2 | "Post-mortem on the website migration. We planned 4 weeks and it took 7." | Should fire | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 3 | "Log this: the Q3 audit prep ran two days over because the auditor was late with the sample list." | Should fire | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 4 | "We dropped the loyalty-card project halfway. Can we close it out properly?" | Should fire (abandoned) | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 5 | "How did that go compared to the plan? I budgeted 10 hours for the training deck." | Should fire | lessons-learned | lessons-learned | lessons-learned | lessons-learned |
| 6 | "Is this draft good enough to send?" | Near miss | review-my-work | review-my-work | review-my-work | review-my-work |
| 7 | "This chat is long. Wrap this up so I can start a fresh one." | Near miss | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat | continue-in-new-chat |
| 8 | "How long will the next migration take, given how this one went?" | Near miss | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take | how-long-will-it-take |
| 9 | "Wrap up the meeting: decisions, owners, next steps." | Near miss | meeting-close (meeting-design) | meeting-close | meeting-close | meeting-close |
| 10 | "What could go wrong with the migration plan before we start?" | Near miss | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong | what-could-go-wrong |
| 11 | "I can't finish this report and I don't know why." | Near miss | get-unstuck | get-unstuck | get-unstuck | get-unstuck |
| 12 | "Wrap this up." | Ambiguous | lessons-learned or continue-in-new-chat | lessons-learned | lessons-learned | lessons-learned |
| 13 | "Retro on the sprint we just finished." | Ambiguous | lessons-learned or meeting-close | lessons-learned | lessons-learned | lessons-learned |
| 14 | "Log this" (after an estimate was discussed, no work finished) | Ambiguous | lessons-learned or none | lessons-learned | none | none |

---

## What each case tests

**1 to 5, should fire.** Literal trigger phrases and close paraphrases across unrelated fields (web, finance and audit, retail, training). Case 4 tests that abandoned work is included. Case 5 tests the "planned versus actual" phrasing without the word "retro".

**6, review-my-work.** A draft quality question. The retro reviews the process, not the output.

**7, continue-in-new-chat.** "Wrap up" in the chat sense. The same verb appears in both descriptions, so this is the most likely false positive. It is also the reason case 12 exists.

**8, how-long-will-it-take.** The user wants a forward number. `lessons-learned` writes the log that `how-long-will-it-take` reads. A user who has just finished a retro and then asks this is a chain, not a conflict.

**9, meeting-close.** The meeting-level close. The distinction is a meeting versus a piece of work.

**10, what-could-go-wrong.** Before the work, not after.

**11, get-unstuck.** Work that has stalled, not work that has ended.

**12, ambiguous.** "Wrap this up" with no object. Could close a chat or close a piece of work. A good answer asks, or picks by context. Record what each model does and decide in writing whether the split is acceptable.

**13, ambiguous.** A sprint is both a recurring meeting ritual and a piece of work. `lessons-learned` is for a piece of work with a plan to compare against; a team ritual may be the territory of another skill. Record the split.

**14, ambiguous.** "Log this" is a literal trigger, but with no finished work there is nothing to retro. The right behaviour is likely to ask what is being logged. Checked by reading the output.

---

## Output check

One case to be checked by hand once a model is available: case 2. The output should contain the planned versus actual table, one largest surprise, repeat and stop items, a miss class from the six named, one if-then change, a log entry with type of work, size, planned duration, actual duration and what drove the gap, and a line on what was assumed. It should not report a pattern, since a single case has fewer than five entries.

A second check: given a log file with four entries, the skill must say fewer than five is anecdote, not pattern. Given five, it should offer a pattern read.

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first.
- **Whether the log entry works as a reference case in practice.** The format is built to match the precedent worksheet in `how-long-will-it-take`. Nobody has yet used a real log to correct a real estimate.
- **Real sessions.** Every case is constructed.

## Misses and how to read them

No misses on cases with a single expected answer.
