# Evaluation: get-unstuck

Routing cases for `get-unstuck`, written alongside the skill. **No results are recorded.** The Haiku, Sonnet and Opus columns read "not yet run" because these cases have not been put to any model. Only the expected routing is filled in, and it is a prediction from reading the descriptions, not a finding.

**Method.** Follow the procedure in `evals/README.md`: show a model the verbatim descriptions of every skill in the repository, with no skill bodies, and ask for one skill name or `none`. Pin the description text used, since results do not survive rewording. Skills named below that are not yet in the repository (`plan-the-work`, `fit-to-deadline`, `what-could-go-wrong`, `review-my-work`) must be present in the description set for the near misses to be meaningful.

---

## Cases

| # | Message | Kind | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "I'm stuck on this proposal and I don't know why." | Should fire | get-unstuck | not yet run | not yet run | not yet run |
| 2 | "I keep putting off the quarterly tax paperwork. It's been on my list for weeks." | Should fire | get-unstuck | not yet run | not yet run | not yet run |
| 3 | "I'm going in circles on the supplier choice and can't write the brief until I decide." | Should fire | get-unstuck | not yet run | not yet run | not yet run |
| 4 | "Help me get moving on the thesis chapter, I can't get started." | Should fire | get-unstuck | not yet run | not yet run | not yet run |
| 5 | "I need this report done by Friday but I only have two days. What should I cut?" | Near miss | fit-to-deadline | not yet run | not yet run | not yet run |
| 6 | "What could go wrong with my launch plan?" | Near miss | what-could-go-wrong | not yet run | not yet run | not yet run |
| 7 | "Should I hand this data cleanup to an agent or do it myself?" | Near miss | delegate | not yet run | not yet run | not yet run |
| 8 | "Our weekly sync keeps going in circles. Help me fix it." | Near miss | meeting-design | not yet run | not yet run | not yet run |
| 9 | "What counts as done for this website redesign?" | Near miss | scope-the-work | not yet run | not yet run | not yet run |
| 10 | "Is my first draft any good? I keep rereading it and can't tell." | Near miss | review-my-work | not yet run | not yet run | not yet run |
| 11 | "I can't get started on the product brief because I don't really know what it's for." | Ambiguous | get-unstuck or plan-the-work | not yet run | not yet run | not yet run |
| 12 | "I'm blocked until legal sends the contract. How do I chase them?" | Ambiguous | get-unstuck or meeting-or-message | not yet run | not yet run | not yet run |
| 13 | "I feel overwhelmed and can't do anything lately, not just this project." | Ambiguous, boundary | get-unstuck, with the one-time referral | not yet run | not yet run | not yet run |

---

## What each case tests

**1 to 4, should fire.** Literal trigger phrases and close paraphrases, across unrelated fields (writing, admin, procurement, academic). All four are one named piece of work that has stalled.

**5, fit-to-deadline.** A time budget against too much scope. The user is not stuck; they have more work than time. `fit-to-deadline` fits scope to a budget. `get-unstuck` has "too big to start" as one cause, which is a different problem.

**6, what-could-go-wrong.** Stress-testing a plan that has not failed yet. Nothing has stalled.

**7, delegate.** An allocation question about a task. A user who is stuck on a task and then asks who should do it is a hand-off from `get-unstuck` to `delegate`, not the first route.

**8, meeting-design.** "Going in circles" appears in the trigger list of `meeting-design` as well. This tests that a recurring meeting problem goes there. The word overlap is the risk.

**9, scope-the-work.** Defining done before the work starts. No stall.

**10, review-my-work.** A draft exists and the question is its quality. The phrase "can't tell" may pull toward `get-unstuck`.

**11, ambiguous.** An unclear outcome is the first cause in `get-unstuck` and the whole job of `plan-the-work`. Either routing is defensible. Decide in writing after a run whether the split is acceptable, as with case 10 in `evals/delegate.md`.

**12, ambiguous.** Waiting on a person is a cause in `get-unstuck`, whose move is a drafted message. `meeting-or-message` picks the channel. The two are meant to chain, so a split is probably acceptable.

**13, boundary.** Distress beyond a single task. The skill should say once that a person who can help is worth talking to, and continue the practical part only if wanted. It should not diagnose. This case is about the body of the skill, not routing, and is checked by reading the output.

---

## Output check

One case to be checked by hand once a model is available: case 3. The output should contain a one-sentence diagnosis quoting the user's words, one action of 15 minutes or less with a stopping point, a 5-minute fallback, an if-then, and an assumptions line. It should not contain a plan or a list of steps.

---

## Not tested here

- **Any model behaviour.** Nothing in this file has been run.
- **Whether the description survives the listing budget.** A new skill with no invocation history loses its description first when the listing is truncated.
- **Real sessions.** Every case is constructed.
