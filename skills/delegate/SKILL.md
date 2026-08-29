---
name: delegate
description: >
  Decides what to hand to an AI agent and what to keep, for one specific piece
  of work. Trigger when the user says "should I delegate this", "can AI do
  this", "should I automate this", "what should I hand off", "give this to an
  agent", "is this worth automating", "who should do this", "can Claude do this
  part", or describes a task and asks whether to run it themselves. Also trigger
  when a user is about to hand over work whose output they would not be able to
  check. Splits the work into parts, allocates each to the user, another person
  or a model, and attaches a verification step and a stop condition to every
  part that leaves the user's hands. Ends on a filled allocation table, not on
  advice. Use a process or SOP skill for documenting a repeatable procedure, and
  a ritual or automation-charter skill for a recurring team ceremony. This one
  is for a single piece of work.
---

# Delegate

Most delegation advice sorts tasks by whether a model can do them. That is the wrong sort. A model can do plenty of things whose output nobody in the room is able to check, and those are the ones that come back to bite.

The failure this exists to prevent: **handing over the part you cannot verify, and finding out at delivery.**

This skill takes one piece of work, splits it, and decides where each part goes. Every part that leaves the user's hands leaves with a check attached. It ends on a filled table.

---

## What this needs

**Minimum: a description of the piece of work.** One or two sentences is enough. No connector, no workspace, no file access.

**Better with** what the output is for and who sees it. The verification bar moves with the consequence, not with the task, so this changes the answer more than anything else the user could add.

**Best with** one line on what the user has handed over before and what came back wrong. That turns generic checks into the specific ones that catch this user's actual failures.

Where the user gives only the task and nothing else, run anyway and ask the three questions in Step 1 as part of the output rather than blocking on them.

---

## When this runs

Runs when there is a specific piece of work on the table and the question is how to run it.

**Does not run for:**

- A recurring team ritual or a standing ceremony. That is a ritual inventory, and an automation-charter skill handles it.
- Documenting a repeatable procedure. That is an SOP, and a process-documentation skill handles it.
- Delegating to people as a management or development question. This skill allocates work, it does not develop anyone.
- Writing the prompt. This skill stops at the allocation.

---

## Step 1: Name the work and set the bar

Three questions, one line each. Ask them before splitting anything.

1. **What is the output?** A document, a decision, a list, a piece of code, a message to someone. Name the artefact, not the activity.
2. **Who sees it, and under whose name?** Work that goes out under the user's name, to a client, or into a decision someone else makes has a higher bar than work only the user reads.
3. **What happens if it is wrong and nobody notices?** This is the question that sets the verification bar. An embarrassing draft and a wrong number in an invoice are not the same risk, and they do not get the same checks.

Write the answer to question 3 down. Every check later in this skill is calibrated against it.

## Step 2: Split the work at the seams

Split by the kind of thinking each part needs, not by the order things happen in. Chronological splits produce parts that all need the same judgement, which is no split at all.

The usual seams:

- **Gathering.** Finding, retrieving, collecting, transcribing.
- **Deciding.** Choosing what matters, what to cut, what the angle is.
- **Producing.** Turning the decision into the artefact.
- **Checking.** Confirming the artefact is right.

A part is small enough to allocate when the user can say in one sentence what correct looks like for it. If they cannot, it is still two parts, or it is a part they do not understand well enough to hand over yet. Both of those are findings, and both go in the output.

## Step 3: Allocate each part

Three destinations: the user, another person, a model. Take each part through four tests in order, and stop at the first one that decides it.

**1. Can the user say what correct looks like?**
If not, the part stays with the user. Not because a model would fail it, but because nobody would know if it did. This is the test that does the most work and the one most delegation advice skips.

**2. Does it need context that has never been written down?**
Judgement built on years of knowing a client, a codebase or a market does not transfer in a prompt. Where the context exists but is scattered, that is a different answer: the part can be delegated once the context is assembled, and assembling it becomes its own row.

**3. Is an error recoverable, and how cheaply?**
A draft that reads badly costs a rewrite. A wrong figure in something already sent costs the relationship. Where recovery is expensive, either keep the part or delegate it with a check that runs before anything is irreversible.

**4. Is doing this part the thing that keeps the user good at their job?**
Some work is its own training. Handing over all of it is a real cost, paid later and quietly. This test loses to the first three, but where two allocations are otherwise equal it decides.

## Step 4: Attach a check to everything that leaves

No row goes to a model or another person without three things filled in.

- **The check.** The specific thing the user looks at to catch this being wrong. "Review it" is not a check. "Confirm every figure in the summary appears in the source file" is.
- **The stop condition.** What makes the user take the part back rather than fix it in place. Usually a threshold: more than two errors found, or any error of a particular kind.
- **What is lost if the check is skipped.** Written down, because this is what makes the check survive a busy week.

**The rule that decides the marginal case: if the check costs more than doing the part, do not delegate the part.** Verification is work. A part that takes twenty minutes to do and forty minutes to check properly has not been delegated, it has been made more expensive.

One caution to state in the output where it applies. Confidence in the tool tends to move in the opposite direction to scrutiny, and it is strongest where the user knows the domain least. The parts a user feels most comfortable handing over unchecked are often the ones they are least equipped to check. Where a part sits outside the user's own expertise, the check gets stricter, not looser.

## Step 5: If it recurs, ask the second question

Only where the user says this piece of work comes round again. Same four tests, plus two more.

- **How often, and is the input stable?** A monthly task whose inputs change shape every month is not a candidate for running unattended, whatever its judgement content.
- **What does drift look like, and when is it noticed?** Anything that runs without a person notices its own failures late. Set a date to look at it again, and put that date in the table.

Recurring work that passes all six becomes a candidate for running without the user. Recurring work that fails any of them is still worth allocating, just not worth automating.

## Step 6: Fill the table and hand it over

Fill `assets/allocation-table.md` and give it to the user. One row per part. Nothing goes in the chat that is not in the table, other than the three findings below where they apply:

- Any part where the user could not say what correct looks like.
- Any part where the check would cost more than the work.
- Any part that stays with the user only because of test 4.

---

## Output

A filled allocation table, handed over in full. Columns: the part, where it goes, the check, the stop condition, what is lost if the check is skipped.

Plus, in prose above the table and no longer than four lines: what the verification bar is, taken from Step 1 question 3, and any of the three findings from Step 6 that came up.

If the user asked about a recurring piece of work, the table carries a review date.

---

## Failure modes

**Splitting by chronology.** First, then, next. Every part needs the same judgement and nothing can be allocated separately. Split by the kind of thinking instead.

**Delegating the checking along with the doing.** The most common way this goes wrong. A model that produced the work is not a check on the work, and a second model reading the first one's output is a weaker check than it looks. The check has to be something the user or another person can carry out.

**Allocating the whole piece of work to one destination.** If every row says the same thing, the split in Step 2 did not happen. Go back to it.

**Treating "a model can do this" as "a model should do this".** Capability is test zero, and this skill never asks it. Every test in Step 3 is about whether the user can live with the output, not whether the output can be produced.

**Over-keeping.** The opposite failure, and real. This skill is not an argument for doing everything yourself. Where a part passes all four tests, allocate it and say so plainly. A process that never hands anything over is a process nobody runs twice.

**Quoting a time saving.** No credible figure exists for how much time delegation to a model saves on knowledge work, and the widely circulated ones do not survive tracing. Do not put one in the output.

---

## What this does not do

- **Not a capability assessment.** It does not test what models can do, and it goes out of date if it tries.
- **Not prompt engineering.** It says which parts go to a model. It does not write the instructions.
- **Not a procurement or tool decision.** Which model or which tool is a separate question, and a tool-vetting skill answers it.
- **Not a guarantee.** A filled table means the decision was made deliberately with the checks named. It does not mean the work will be right.

---

## Supporting files

- `assets/allocation-table.md` - the table this skill fills in and hands over
- `references/what-agents-get-wrong.md` - failure modes by task type, and the check that catches each one
- `references/worked-example.md` - one piece of work taken through all six steps
