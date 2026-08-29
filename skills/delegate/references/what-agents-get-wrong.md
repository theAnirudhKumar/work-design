# What agents get wrong, by task type

Load this when writing the check column. The point of the table is that the check has to match how that kind of task actually fails, not how tasks fail in general.

Two things to hold onto while using it.

**A failure mode is not a prohibition.** Every row here describes work that is worth handing over. The column that matters is the last one.

**The check has to be something a person can carry out.** A second model reviewing the first model's output shares most of the first one's blind spots, and it produces a confident second opinion either way. Where a check can only be done by another model, treat the part as unchecked and allocate accordingly.

---

## By task type

| Task type | How it fails | The check that catches it |
| :--- | :--- | :--- |
| Summarising a document | Quietly drops the exception, the caveat and the dissenting paragraph, because summaries reward the main thread | Read the source for what is missing, not the summary for what is wrong. Check the last page especially, where conditions live |
| Research and fact finding | Produces a plausible source that does not say what it is cited for, or does not exist | Open every link. Confirm the specific claim appears in the specific source, not that the source is broadly about the topic |
| Anything needing recent facts | States a superseded fact with full confidence, and the confidence does not drop with age | Check the date on anything that can change: prices, roles, policies, versions, availability |
| Numbers and calculation | Arithmetic that looks right, units that quietly change, a total that does not reconcile to its parts | Re-add the column. Confirm the total equals the sum of the rows and that units are the same throughout |
| Data transformation | Handles the common rows and mangles the edge cases: blanks, duplicates, dates, names with punctuation | Compare row counts before and after. Look at the first, last and any row you know is awkward |
| Drafting from a template | Carries a field from the last one through, or leaves a placeholder in | Search the output for the previous subject's name and for every bracket character |
| Writing in someone's voice | Averages towards a generic register and loses whatever made it recognisable | Read it aloud. Compare against something the person actually wrote, not against a description of their style |
| Personalised outreach | Gets the detail wrong in a way that is worse than not personalising at all | Verify each personal detail against a source. One wrong detail undoes the whole message |
| Code | Runs, passes the happy path, and fails on the case nobody wrote a test for | Run it on real input, including the input you expect to break it |
| Judgement calls | Answers rather than declining, because the shape of the request is an answer | Ask what would have to be true for the opposite call. A part that cannot answer that was not a judgement it should have made |
| Multi-step work | Drifts from the brief across the steps, ending somewhere reasonable and not what was asked | Reread the original request against the final output. Skip the middle |

---

## The pattern underneath

Most of the table is one failure wearing different clothes: **the output is shaped like a correct answer whether or not it is one**, and the confidence attached to it does not vary with how likely it is to be right. Human work signals its own uncertainty through hedging, mess and visible gaps. Delegated work often does not, so the check has to supply what the signal would have.

That has a direct consequence for allocation. The parts where a user is least able to notice a wrong answer are the parts where they most need a check, and they are also the parts where a check is hardest to write. Where both are true, the honest answer is usually that the part is not ready to be handed over yet.

---

## The evidence, and its strength

State the strength when citing any of this in an output. The literature here is young and much of it is first-party.

| Finding | Source | What it is |
| :--- | :--- | :--- |
| Higher confidence in the AI predicts less critical thinking; higher confidence in one's own expertise predicts more | Lee et al., CHI 2025, [ACM](https://dl.acm.org/doi/10.1145/3706598.3713778) | Peer reviewed, self-report survey of knowledge workers |
| Advanced users are considerably more likely to pause before starting to decide what goes to AI and what goes to a person, 53% against 33%. 86% treat output as a starting point. 50% name quality control of output as increasingly critical | Microsoft Work Trend Index, 5 May 2026, [WorkLab](https://www.microsoft.com/en-us/worklab/work-trend-index/agents-human-agency-and-the-opportunity-for-every-organization) | Vendor first-party survey, 20,000 workers across 10 countries |
| Perceived productivity gains exceed measured gains | NBER Working Paper 34984, March 2026, [NBER](https://www.nber.org/papers/w34984) | Working paper, roughly 750 executives, not peer reviewed |
| Automation bias and skill erosion are documented across human-AI collaboration | [AI and Society review, 2025](https://dl.acm.org/doi/10.1007/s00146-025-02422-7) | Review literature |

---

## Claims not to make

Each of these was traced to its source and failed. They are listed because they are common enough that they will otherwise turn up in an output.

- **Any percentage for time saved by delegating to a model.** Nothing credible was found at any scope.
- **"AI makes developers 19% slower."** The study behind it was revised by its own authors on 24 February 2026 on selection-bias grounds, and is being redesigned ([METR](https://metr.org/blog/2026-02-24-uplift-update/)). Citing it as current is citing a superseded result.
- **"95% of enterprise AI pilots fail."** The underlying funnel showed 20% reaching pilot and 5% reaching production. The 95% appeared in roughly one sentence with no supporting data.
- **"It takes 23 minutes to refocus after an interruption."** No published source. The study usually credited measured something else and reports a standard deviation twice its own mean.
