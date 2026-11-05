---
name: review-my-work
description: >
  Reviews a finished draft as the skeptical person who has to read it.
  Trigger when the user says "review this", "is this good enough to send",
  "poke holes in this draft", "would you put your name on this", "check my
  work", "be a harsh reader", "does this make sense", "sanity check this",
  "red team this draft", or pastes an email, memo, analysis, proposal, spec,
  deck outline, summary or AI-generated text and wants to know if it holds up.
  Reads as the intended reader with five minutes and a reason to doubt, then
  gives a verdict (ship, fix then ship, rework), the three worst problems with
  quoted passages, a filler-versus-substance test, what to verify, and a fix
  list by value per minute. Not for stress-testing a plan, which is
  what-could-go-wrong, not for designing a hand-off, which is delegate, and not a
  copyedit.
---

# Review My Work

Fluent, well-formatted, confident text is now cheap to produce, and it is easy to send without anyone having thought hard about it. The cost lands on the reader, who must work out what it claims, whether it is true, and what they are supposed to do. This skill is the review that happens before the reader has to pay that cost. The pattern is named in the Harvard Business Review article "Why People Create AI Workslop and How to Stop It" (January 2026): polished output that shifts the real work onto the recipient.

The failure this exists to prevent: **sending polished, plausible-looking work that nobody, including its author, has actually checked, so the reader finds the gaps instead.**

---

## What this needs

**Minimum: the draft, pasted in.** An email, memo, analysis, proposal, spec, deck outline, essay, summary of code changes, report section. No file, connector or tool.

**Better with** what the draft is for and who reads it: their role, what they know already, what they must do after reading, and how much they will trust it by default.

**Best with** the source material or data behind the claims, and anything the reader has said about the topic before. Without sources, the skill can judge whether claims are supported in the text but cannot check them.

If the purpose or reader is missing, do not stall. State the assumption in one line, proceed, and ask at most one question, only if the answer would change the verdict.

---

## When this runs

Runs when a piece of finished or nearly finished work exists and the question is whether it is good enough to go out.

**Does not run for:**

- A plan, launch or decision that has not happened yet. That is `what-could-go-wrong`.
- Deciding what to hand to a person or a model and how to check it. That is `delegate`. Once delegated work comes back, this skill is the natural reviewer for it.
- Typos, grammar and style polish. A copyeditor fixes those, and this skill does not start there, because a clean surface on an empty draft is the problem, not the solution.
- Framing the work before it starts. That is `plan-the-work`.
- Rewriting the whole thing. Only if the user asks.

---

## Step 1: Fix the reader

Write one line: who reads this, what they already know, what they must do afterwards, and why they might doubt it. If the user said, use that. If not, infer the most likely reader from the draft and state it: "Assumed reader: the finance director, who will decide on the budget line and distrusts forecasts without a basis."

Then read as that person. Five minutes, no patience for background, one reason to doubt.

## Step 2: Do the 30-second test

Read the opening, the headings and the last paragraph only. Can the reader say what this is asking for or telling them, and what happens next? Record yes, partly or no, with one line saying what a reader would think the point was.

If the first 30 seconds fail, say that before anything else in the review, because most readers never get further.

## Step 3: Find the three worst problems

Pick the three that would most change the reader's decision or trust, and rank them. For each:

- **Quote** the exact passage, in quotation marks.
- **Say** what is wrong with it, in terms of what this reader will do or think.
- **Say** what would fix it, in one line.

Problems of substance rank above problems of tone, and tone above form. Typical serious problems: the main claim is not stated; the number has no basis; the recommendation does not follow from the analysis; the ask is buried; a key objection is not addressed; the draft answers a different question from the one the reader has.

## Step 4: Run the Substance Test

Go through the draft passage by passage and mark each as one of:

- **Carries weight.** Contains a checkable claim, a decision, a number, a named example or a specific commitment.
- **Filler.** Fluent but removing it changes nothing: restated context, generic framing, "it is important to note", summaries of what was just said, adjectives that stand in for evidence.
- **Needs support.** A claim that may be true but that the draft does not back, or that the reader will want backed.

List the filler passages by quoting their first few words. List the needs-support claims as a verification list: each claim, and exactly what would confirm it (which source, which figure, which person).

**State what you could not check.** You cannot verify facts, figures, quotations, citations, links or internal data. Say plainly which claims you took as given, and do not describe a claim as accurate because it sounds right. Where a reference looks like it might be invented or misattributed, flag it for checking and do not assert that it is wrong.

## Step 5: Predict the skip and the misread

Say what the reader will probably skip (long sections that repeat the point, caveats at the bottom, an appendix) and what they will probably misread (an ambiguous phrase, a number without a unit or period, a "we" that could mean two groups, a hedge that sounds like a commitment). Point to the passage.

## Step 6: Order the fixes by value per minute

List fixes with the highest effect on the reader for the least effort first. Mark each with a rough time: a minute, ten minutes, an hour. Include cutting. A fix list that only adds words is suspect.

## Step 7: Say what is good

Two to four lines naming what works and should survive revision: a clear opening, a strong example, an honest caveat, a well-chosen number. The point is that fixes do not erase strengths.

## Step 8: Give the verdict, calibrated

One line at the top of the output:

- **Ship.** The reader's likely questions are answered, nothing in the three worst problems changes their decision, and any unchecked claims are low-stakes. Say ship when it is good. Do not manufacture problems.
- **Fix then ship.** The draft is sound but needs the listed fixes, none of which need rethinking.
- **Rework.** The core claim, structure or evidence is not there. Say what needs to exist before a rewrite would help.

If the verdict is Ship, the three problems are the three smallest ones, labelled as minor.

---

## Targeted rewrites

Do not rewrite the whole draft unless asked. Where a passage is the worst offender, offer a rewrite of that passage alone, in the author's register, and label it as a suggestion. Keep the author's facts: do not add numbers, names or claims that were not in the draft. If a rewrite needs a fact the draft lacks, put a bracketed gap in its place, such as [figure and source].

---

## Output

Fill `assets/review-sheet.md` and give it in the chat. In order:

1. Verdict, one line.
2. Assumed reader and purpose.
3. The 30-second test result.
4. The three worst problems, ranked, each with the quoted passage.
5. The Substance Test: filler passages, needs-support claims, the verification list, and what could not be checked.
6. What the reader will skip or misread.
7. Fix list by value per minute.
8. What is good, keep it.
9. Optional targeted rewrites of the worst passages.

Keep it proportionate. A five-line email does not need a nine-part review: compress to verdict, the main problem, and the fix.

---

## Failure modes

**Harshness for sport.** Inventing problems to look rigorous. If the draft is good, the verdict is Ship and the output is short.

**Reviewing the surface.** Comments on word choice and formatting while the main claim is unsupported. Substance first.

**Vague criticism.** "Could be clearer." Quote the passage and say what is unclear to this reader.

**Treating fluency as accuracy.** A passage reading smoothly is not evidence it is right. Anything stating a fact goes on the verification list, and the output must say that you did not verify it.

**Reviewing as yourself.** The question is what the intended reader will do, not what you would have written.

**Praising to soften.** The keep list is for real strengths, not a cushion before the bad news.

**Reviewing your own earlier output as if independent.** If the draft was written by the same model earlier in the conversation, say so, and say the review shares its blind spots. The user or a colleague must do the fact checks.

---

## Supporting files

- `assets/review-sheet.md` - the template this skill fills in and hands over
