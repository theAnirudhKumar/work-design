# Contributing

The most useful thing you can send is not a new skill. It is a vetting you ran that came out differently from what these skills would have predicted.

These checks were built from reviewing tools for people who do not code. That is one person's sample. If a check misses something in your industry, on your platform, or under your regulator, that is a defect and worth an issue.

---

## The three things worth contributing

**1. A check is wrong, or it missed something.** Open an issue saying what you found and where the skill would have led you astray. Specific beats general. "The privacy check is thin" is hard to act on. "Under GDPR, the retention clause that matters is the one about backups, and the skill never asks for it" is a fix.

**2. A skill is missing from the set.** This repository is for deciding about a tool: whether to adopt it, whether you already pay for something that does it, and what breaks when you leave. `switch-cost` is planned. If there is another, describe the job, how often it recurs, and what a good output looks like.

**3. You have written one.** Open a pull request. Read the rest of this first.

---

## The two rules

**Nothing may be a prerequisite.** A skill that fails because you lack a connector, a file or a terminal gets uninstalled. Every skill states the least it can run on, then says what each extra input would add. Missing context changes what a skill can honestly claim, never whether it runs.

**Every skill names the failure it exists to prevent.** One sentence, near the top. If it cannot say what goes wrong without it, it is a template rather than a skill.

---

## Writing a skill

### Structure

```
skills/<skill-name>/
  SKILL.md              the method
  references/           detail the method points at, one level deep only
  assets/               templates the skill fills in and hands over
```

### SKILL.md

- **Under 500 lines.** Detail moves into `references/`
- **Frontmatter carries `name` and `description`.** The `name` matches the folder exactly
- **The description goes under 1,024 characters and leads with literal trigger phrases.** Assistants truncate the tail of a description when the listing grows, so the words someone would actually type go first and the explanation goes last
- **References are one level deep.** A reference pointing at another reference gets partially read
- **Third person throughout.** "The user", not "you", and never a named person

### Ship an eval, not just a skill

A skill that never fires is indistinguishable from a skill that was never written, and routing happens on the description alone. Every new skill arrives with a file in `evals/` carrying at least three cases: prompts that should fire it, near misses that should not, and any prompt where it and an existing skill could both claim the trigger.

Run them on Haiku, Sonnet and Opus. Record the disagreements rather than the average. Two of three is a finding, not a pass. `evals/README.md` has the procedure and `evals/delegate.md` is the reference.

This has already earned itself. The first full pass found that one skill's proactive trigger fires on two models out of three, and that a cost-shaped complaint never reaches the skill that would actually solve it.

### Ship an asset, not just advice

The difference between a skill people install and one they do not is whether it hands something over. A checklist, a template, a rubric, a filled document. A skill that returns advice is competing with the assistant's own general knowledge, and losing.

### Say what you could not check

Every skill here has somewhere in its output format for the gaps. Use it. Naming what you could not confirm is what makes the rest credible, and it is the thing almost nothing else in this category does.

---

## House style

- **No em dashes.** A comma, a colon, a spaced hyphen or a full stop
- **No speculation presented as finding.** Quote the clause, name the thread, date what you found. "The terms grant a licence to reproduce and modify uploaded content" beats "the terms are aggressive"
- **Separate the claim from the verification.** "The maker states X" and "X is independently audited" are different sentences and must never be merged
- **No real customer, employer or personal names**, in worked examples too. Where a worked example needs a company, invent one and make it obviously invented
- **Name a tool only where the finding is durable.** A dated review can name its subject because a reader can check whether it still holds. A reference file in this repository cannot make that promise, and a stop that ages badly is unfair to a product that fixed the problem

---

## Before you open a pull request

Run the validator. It catches everything structural, so the review can be about judgement instead.

```
python3 validate-skills.py
```

Then check the things a script cannot see:

- [ ] There is a file in `evals/` with at least three cases, run on three models, disagreements recorded
- [ ] The skill states the least it needs to run, and nothing is a prerequisite
- [ ] The failure it prevents is named
- [ ] It ships at least one asset, or there is a reason it does not
- [ ] Any worked example uses an invented company, or a product described rather than named
- [ ] Claims are separated from verification
- [ ] No real customer, employer or personal names anywhere
- [ ] The README is updated if this adds or removes a skill

---

## What happens next

Pull requests get read as a diff before merging, because that is where a stray name or a broken claim actually shows up. Expect questions on anything stating a fact without saying where it came from. That standard applies to the maintainer as much as to anyone else.
