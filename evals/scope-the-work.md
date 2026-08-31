# Evaluation: scope-the-work

Routing cases for `scope-the-work`, run against the eight descriptions in this repository as they stand with this skill added. Written alongside the skill, per `CONTRIBUTING.md`.

**Run on:** 31 Aug 2026, against Haiku, Sonnet and Opus.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Before I start this redesign, what should I actually commit to and what should I leave out?" | fire | scope-the-work | scope-the-work | scope-the-work |
| 2 | "This client project keeps growing every week, I need to draw a line on what's actually in scope." | fire | scope-the-work | scope-the-work | scope-the-work |
| 3 | "Should I hand this whole report off to Claude or keep the analysis part myself?" | delegate | delegate | delegate | delegate |
| 4 | "Should I just message the team about this or do we need a call?" | pick-the-medium | pick-the-medium | pick-the-medium | pick-the-medium |
| 5 | "Should I sign up for Notion for our team?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 6 | "What counts as done for this onboarding project? I don't want to be revising it forever." | fire | scope-the-work | scope-the-work | scope-the-work |
| 7 | "How long will this project realistically take based on similar work we've done before?" | none | none | none | none |
| 8 | "We are evaluating a document platform for the whole company, six figures, and procurement needs a recommendation." | none | none | none | none |

Eight of eight agree across all three models. No split, no disagreement.

---

## Cases 1, 2 and 6, the skill's own territory

Three shapes of the same job: naming what's in and out before starting, redrawing a line on work that already grew, and pinning a done condition so revision doesn't run forever. All three fired `scope-the-work` cleanly on every model, including case 2's "already grown once" framing, which the description names as its own explicit trigger alongside the before-it-starts case.

## Case 3, 4 and 5, the neighbours hold

Case 3 (hand off to Claude or keep it) went to `delegate`, case 4 (message or call) went to `pick-the-medium`, case 5 (adopt a new tool) went to `before-you-install`. None pulled toward `scope-the-work` despite each involving a piece of work that could plausibly need scoping too. `scope-the-work`'s own description draws this exact line from its side ("Use pick-the-medium for how to communicate something and delegate for who does work already scoped; this is what the work actually is, before either question comes up"), and the eval confirms it holds from the neighbouring skills' side as well.

## Case 7, the gap this skill deliberately leaves open

Built to check whether `scope-the-work` would overreach into estimating how long the work takes, since a boundary note and a time estimate can feel like the same artifact. It did not: all three models declined every skill, and two named the reason directly, that `scope-the-work` draws boundaries, not schedules. This is the same boundary the skill's own "What this does not do" section states plainly. No skill in this repository covers duration estimation as of this eval; that gap is closed by the next skill in this category.

## Case 8, a repeat of a known gap

The six-figure procurement case from `evals/before-you-install.md` and `evals/stack-audit.md`, rechecked with `scope-the-work` in the mix. Still declines on all three models. `scope-the-work` is for the shape of a piece of work, not a vendor decision with a buying committee, and nothing in its description reaches toward that territory.

---

## Not tested here

Whether `optimize-tokens`, `chat-context` or `switch-cost` compete with `scope-the-work`. None of their trigger vocabularies overlap with scoping, boundaries or done conditions, and none of their own recorded cases mention project scope, so no case was constructed. Worth a check the day any of those descriptions change again.

**Output behaviour.** Whether the out list actually gets specific rather than generic, whether the done condition holds up as genuinely checkable by a third party, and whether "who moves the line" gets a named person rather than a group. All output checks, not routing.

**Real sessions.** Every case here is constructed, same limitation as every other file in this directory.

---

## Field test, 2026-08-31

One real case, not constructed: closing two blank entries in a professional profile document that had been bundled under one open-ended active-project note alongside three unrelated follow-ups. Result: pass, both failure modes checked clean (out list had three named items, done condition was third-party checkable). Not a live `Skill` tool run, the skill is not installed in this account; the shipped `SKILL.md` was applied by hand against the real case instead. Case detail is internal and not reproduced here.
