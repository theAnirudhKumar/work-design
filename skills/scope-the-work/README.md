# scope the work

**Write down what's out, before "one more thing" makes it in.**

Most scope creep isn't a stakeholder changing their mind mid-project. It's a boundary that was never written down, so there's nothing to point back to when the request quietly grows. Every addition looks reasonable in isolation - because nobody ever said, in writing, that it was outside the work to begin with.

This skill writes that boundary before the work starts. It pushes past the topic ("redesign the onboarding flow") to the actual ask ("cut onboarding drop-off by fixing the three screens where people quit"), because only a boundary drawn around a specific ask has an edge. It writes an in list specific enough to check a deliverable against, an out list naming what's adjacent but excluded, a checkable done condition, and names who - a person, not "we" - can move the line if something on the out list turns out necessary. Short enough to reread in under a minute, because that's when it actually gets used.

The failure this exists to prevent: **work that keeps absorbing "one more thing" because nobody ever said what was outside it, so every addition looks reasonable in isolation.**

**Reach for it:** every project. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The exact output varies with what you give it.*

You type: `Before I start redesigning our client onboarding emails, what am I actually committing to?`

You get (shortened):

```
The ask: fewer clients going quiet in week 2, by fixing the three emails
sent in days 1-10. ("Redesign onboarding" is a topic, so I scoped to this
ask. Assumed: the drop-off happens in those emails. Correct me if not.)

In:   rewrite the 3 emails sent in days 1-10 / one revised send schedule
Out:  the welcome call script / the pricing page / the product tour /
      any email after day 10
Done: the three revised emails are live in the sending tool and the old
      versions are retired.
Who moves the line: the account lead. Anything on the Out list that turns
out to be needed gets added by them, in writing.
```

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Name the actual ask | The specific need behind the topic - a boundary has no edge until the ask is specific |
| Write the in list | What this piece of work actually commits to, specific enough to check a finished deliverable against |
| Write the out list | The adjacent things a reasonable person might assume are included, named explicitly as not - so when one comes up later, it's not a surprise |
| Write the done condition | One checkable sentence, not "it looks good" or "everyone's happy" |
| Name who moves the line | A named person or role who can move something from out to in on purpose, so it can't slide in unnoticed |
| The boundary note | In, out, done, who decides - short enough to reread in under a minute mid-work |

---

## Who this is for

Anyone about to start or hand off a piece of work and wants to nail down what they're actually committing to before it starts - especially work that's already grown once, where the goal now is drawing the line before it grows again.

You don't need a project tracker or a client relationship for this. A description of the work and roughly what finished looks like is enough to get a real boundary note out of it.

---

## What this needs

**Minimum:** what the work is and roughly what "finished" would look like.

**Better with:** who asked for this and what they actually need it for - the done condition is only honest if it matches what the request is for, not just what was said.

**Best with:** a case where this same piece of work grew before, so the out list can name the specific thing that crept last time rather than a generic one.

Missing context never blocks this skill. It produces the in/out lists and the done condition from what it's given, and marks plainly what it had to assume.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the other eight skills):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the scope-the-work skill from https://github.com/theAnirudhKumar/work-design: copy its skills/scope-the-work folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/scope-the-work` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, and `assets/boundary-note.md` is the one-page fill-in template - the ask, in, out, done condition, who moves the line.

---

## What this does not do

- **Not who performs the work.** Once the work is scoped, that's `delegate`'s job, working from this skill's own in list.
- **Not a statement of work, contract, or legal terms.** This is a working boundary for the person actually doing or overseeing the work, not a client-facing legal document.
- **Not an estimate.** How long the work takes is a separate concern from what it covers - `estimate-from-precedent` answers that question.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
