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
