# delegate

**Sort work by whether you can check it, not by whether a model can do it.**

Most delegation advice sorts tasks by capability - can AI do this. That's the wrong sort. A model can produce plenty of things that read as correct whether or not they are: a summary that drops the dissenting paragraph, a citation that doesn't say what it's cited for, a total that doesn't reconcile to its parts. The parts that come back to bite are rarely the ones a model couldn't do - they're the ones nobody was equipped to check.

This skill splits one piece of work by the kind of thinking each part needs, not by the order things happen in, then runs every part through four tests: can you say what correct looks like, does it need context never written down, how expensive is an unnoticed error, and does doing this part keep you sharp. Nothing leaves your hands without a named check, a stop condition, and what's lost if the check is skipped - and if the check costs more than the part itself, it doesn't get delegated. It ends on a filled table, not advice.

The failure this exists to prevent: **handing over the part you cannot verify, and finding out at delivery.**

Part of the **Working with agents** group in [work-design](../../#readme).

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Name the work and set the bar | The output named as an artefact, who sees it and under whose name, and what happens if it's wrong and nobody notices - the line that calibrates every check that follows |
| Split at the seams | The work broken into gathering, deciding, producing and checking - not into first-then-next, which produces parts that all need the same judgement |
| Allocate each part | Four tests, in order, stopping at the first that decides it: can you say what correct looks like, does it need unwritten context, how recoverable is an error, does doing it keep you sharp |
| Attach a check to everything that leaves | A specific check (not "review it"), a stop condition for taking the part back, and what's lost if the check gets skipped |
| The recurring-work pass | If the work comes round again: how stable the input is, what drift looks like, and a review date, added to the table |
| The filled table | One row per part - where it goes, the check, the stop condition, what's lost if skipped - handed over in full, with a review date if the work recurs |

---

## Who this is for

Anyone working alongside an AI agent, or a person, and deciding what to hand over for one specific piece of work - not a recurring team ritual (that's a ritual inventory) and not documenting a repeatable procedure (that's an SOP). This is for the moment a piece of work is on the table and the question is who runs which part of it.

You don't need a workspace, a connector, or file access. A description of the task, typed into a chat, is enough to get a real answer.

---

## What this needs

**Minimum:** a description of the piece of work. One or two sentences.

**Better with:** what the output is for and who sees it - this moves the verification bar more than anything else you could add.

**Best with:** one line on what you've handed over before and what came back wrong, which turns generic checks into the ones that catch your actual failures.

Missing context never blocks this skill. Where you give only the task, it runs anyway and asks the three calibrating questions as part of the output rather than stalling on them.

---

## Install

**The easy way: one paste**

```
I want to install the delegate skill from
https://github.com/theAnirudhKumar/work-design. Download or clone the
repository, then copy the skills/delegate folder into
~/.claude/skills/ (or .claude/skills/ if this is for one project only),
keeping its own folder name. Tell me the exact folder path it landed in
when you are done.
```

**In the Claude app (no terminal needed)**

1. Download this repository as a ZIP, or clone it
2. Zip the `skills/delegate` folder on its own
3. In Claude, go to Customize, then Skills, then Create skill, then Upload skill
4. Upload the ZIP

**As a plugin, in Claude Code or Cowork**

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

**Want the whole set?** The [main README's install section](../../#readme) installs all 9 skills at once.

**Or just read it.** `SKILL.md` is the method, `references/` holds the failure-mode table by task type and a worked example run through all six steps, and `assets/allocation-table.md` is the template the skill fills in.

---

## Where this comes from

The evidence behind the checking logic is named and rated for strength rather than presented as settled fact: Lee et al. (CHI 2025) found that higher confidence in an AI's output predicts less critical thinking, while higher confidence in one's own expertise predicts more - the basis for the skill's rule that checks get stricter, not looser, on parts outside your own expertise. The skill also names the claims it deliberately does not make - no percentage for time saved by delegating, and specifically not the "AI makes developers slower" figure or the "95% of pilots fail" figure, both traced to their sources and found not to hold up - because a skill that repeats an unverifiable statistic is worse than one that names the gap.

---

## What this does not do

- **Not a capability assessment.** It doesn't test what models can do, and it would go out of date if it tried.
- **Not prompt engineering.** It says which parts go to a model. It doesn't write the instructions.
- **Not a procurement or tool decision.** Which model or which tool is a separate question - a tool-vetting skill answers it.
- **Not a guarantee.** A filled table means the decision was made deliberately with the checks named. It doesn't mean the work comes back right.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
