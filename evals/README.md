# Evaluations

One file per skill. Each one records which prompts made the skill fire, which ones correctly did not, and what happened on the cases where two skills could both claim the trigger.

A skill that never fires is indistinguishable from a skill that was never written. Everything else in this repository is checked by `validate-skills.py` or by a person reading a diff. Neither of those can tell you whether the description does its one job.

---

## How to run a pass

1. Collect the `description` field of every skill in the repository, verbatim, as it appears in the frontmatter.
2. Give a model those descriptions and nothing else. Do not give it the body of any skill. Routing happens on the description alone, because the body is not loaded until after the skill has been chosen.
3. Put each case from the skill's eval file to it, and ask for one skill name or `none`, with a confidence and a one-line reason.
4. Repeat on Haiku, Sonnet and Opus. Anthropic's authoring guidance asks for at least three evaluations tested across models, on the grounds that what works for Opus can need more detail for Haiku, and this repository has now seen that happen.
5. Record the result in the skill's file, including the disagreements. A pass with the failures edited out is not a pass.

## What a pass looks like

- **Should fire:** all three models pick the skill. Two out of three is a finding, not a pass.
- **Should not fire:** no model picks the skill. Which other skill they pick does not matter unless it is wrong for that skill too.
- **Conflict:** there is no pass or fail. Record what each model did and decide, in writing, whether the split is acceptable. Some are: two skills that answer different halves of a question both lead somewhere useful.
- **Output check:** the skill produces the artefact it promises, filled in, rather than advice. This is checked by hand on one case per skill.

## The three kinds of case

**Should fire.** Phrases someone would actually type. Take them from how the job gets described out loud, not from the description, or the test is circular.

**Should not fire.** Near misses belonging to a neighbouring skill, and the exclusions the skill names in its own description. These are the cases that earn their keep: they are the only way to find out whether a deferral clause works.

**Conflict.** Prompts where two skills in this repository could both plausibly claim the trigger. Name the expected winner, or record deliberately that there is not one.

---

## What these cannot tell you

**Whether the description survives in a real installation.** Every pass here shows the model all descriptions in full. Claude Code loads a listing of names and descriptions, shortens descriptions to fit a character budget scaling at 1% of the model's context window, and when the listing overflows it drops descriptions starting with the skills invoked least. A newly published skill has no invocation history, so it is first to lose its text. That is a property of the installation, and this harness cannot see it.

**Whether anything fires in the wild.** Every case here is a constructed message written by the same person who wrote the skill.

**Anything stable across rewordings.** A result is a result for one rendering of the descriptions. Run 1 and run 2 of the `delegate` cases disagreed on one case, and the descriptions had been reworded between them, so the two runs are not comparable. Record the exact description text alongside any result you intend to compare against later.

---

## When to rerun

- A description changes, anywhere in the repository. Routing is competitive, so a change to one skill can move a case belonging to another.
- A skill is added or removed.
- A model is added to the set.

## Adding a skill

`CONTRIBUTING.md` requires an eval file before a new skill merges. Three cases is the floor. `delegate.md` is the reference implementation.


## Run log

### 5 Nov 2026, all 29 descriptions together

Haiku, Sonnet and Opus were each shown only the verbatim descriptions of every skill in this repository (26) and in meeting-design (3), snapshot `c4b8a8cfab44`, and asked for one skill name or `none` for each of 521 constructed messages. Each model was run as a subagent with an instruction to use only the listed descriptions, one sample per case, so a single flipped pick can be noise (see the rerun below).

| | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- |
| Matched the expected answer (474 cases with one expected answer) | 456 (96.2%) | 461 (97.3%) | 463 (97.7%) |

All three models gave the same pick on 498 of 521 cases. All three matched the expected answer on 453 of 474, and all three missed on 8. Many misses are stale expectations written before the sibling skills were installed together, or overlaps where either answer helps; each file lists its misses with a reading. Cases with a conflict or a free-text expectation were recorded, not scored.

The first pass had 31 cases that shared a number with another case in the same file (second tables restarting at 1). Their answers collided, so those 55 cases were rerun with unique ids and the rerun is what is recorded.

### The protect-my-focus rewording

The run found "My calendar is full of meetings that eat my focus time" going to `meeting-audit` on Sonnet and Opus. The `protect-my-focus` description was reworded to claim that phrase (snapshot `c87b3b32e884`) and the 43 cases that touch `protect-my-focus` or `meeting-audit` were rerun on all three models. Picks that changed:

| Case | Message | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- |
| plan-my-week#8 | "My calendar is full of meetings that eat my focus time. What do I do?" | protect-my-focus | meeting-audit → protect-my-focus | meeting-audit → protect-my-focus |
| build-a-habit#29 | "Our weekly all-hands is a waste of time. Fix it." | meeting-audit | meeting-audit → meeting-design | meeting-audit → meeting-design |
| find-my-method#20 | "I'm always distracted. What should I do?" | protect-my-focus | protect-my-focus → find-my-method | protect-my-focus |
| find-my-method#17 | "Is this weekly status meeting worth having, or should it be an email?" | meeting-audit → meeting-or-message | meeting-audit | meeting-audit |
| protect-my-focus#12 | "Our weekly status meeting is useless and runs an hour. How do we fix i" | meeting-audit | meeting-design → meeting-audit | meeting-design |
| start-a-focus-session#41 | "Block off two hours on my calendar for deep work every morning." | protect-my-focus → start-a-focus-session | none → protect-my-focus | none → protect-my-focus |
| start-a-focus-session#28 | "Our weekly team meeting wastes everyone's time. Fix it." | meeting-design → meeting-audit | meeting-design | meeting-design |
| protect-my-focus#41 | "I'm drowning in everything, work, home, emails." | sort-my-tasks → balance-my-life | sort-my-tasks | sort-my-tasks |

The target case, plan-my-week#8, now goes to `protect-my-focus` on all three models. The other changes are mostly meeting-complaint cases moving between `meeting-design`, `meeting-audit` and `meeting-or-message`, all defensible; a few changed without any related wording change, which is the run-to-run noise to expect from a single sample. The per-skill files have since been refreshed with the second run.

### What this does not show

It does not show how a skill performs once chosen. It does not include Claude Code's listing-budget truncation, which can shorten or drop descriptions in a real installation. All cases were written by the same author as the skills.


### 5 Nov 2026, second run: Work Design as a consultant (4.2.0)

The `work-design` description was rewritten from a menu into a consultant that claims open-ended asks ("how can I work better"). A broad description can pull messages away from the specific skills, so the whole suite was rerun: 551 cases (the earlier 521 plus 30 new `work-design` cases) on Haiku, Sonnet and Opus, snapshot `731601fe12b6`, one sample per case.

| | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- |
| Matched the expected answer (504 cases with one expected answer) | 489 (97.0%) | 490 (97.2%) | 490 (97.2%) |

- **No routing theft.** Of 1563 picks on the earlier cases, 1 moved to `work-design` (protect-my-focus#26 on opus), and the 16 near misses in `evals/work-design.md` all stayed with their specific skills on all three models.
- **The consultant fires.** All 9 open-ended cases went to `work-design` on all three models.
- **Run-to-run noise.** 101 of 1563 picks on the earlier cases differ from the first run (6.5%), most on ambiguous or overlapping cases. Treat a single flipped pick as noise, and a pattern across models as a finding.
- The per-skill result tables in the eval files now show this second run. The first run's totals are in the section above.
