# review my work

**Read it as the person who has five minutes and a reason to doubt it.**

Fluent, formatted, confident-sounding work is cheap to produce now, especially with an AI draft, and cheap to send without anyone having really checked it. The reader pays for that: they have to work out what it claims, whether it is true and what they are meant to do. The Harvard Business Review article "Why People Create AI Workslop and How to Stop It" (January 2026) names the pattern: polished output that moves the real work onto the recipient.

This skill is the review before the recipient has to do it. Paste in the draft, say who reads it if you can, and it reads as that person. You get a verdict (ship, fix then ship, rework), whether the point lands in the first 30 seconds, the three worst problems with the exact passage quoted, and a Substance Test that marks passages that sound fluent but carry no checkable claim, decision, number or example. It lists exactly what to verify, says which claims it could not check itself, predicts what the reader will skip or misread, and orders fixes by value per minute. It also says what is good, so the fixes do not erase the strengths.

The failure this exists to prevent: **sending polished, plausible-looking work that nobody, including its author, has actually checked, so the reader finds the gaps instead.**

**Reach for it:** before anything leaves your hands under your name. Part of [work-design](https://github.com/theAnirudhKumar/work-design).

---

## Example

*Illustrative. The company, people and figures are invented, and the exact output varies with what you give it.*

You type:

```
Would you put your name on this? It's the Q3 update to our board. Reader
is the board chair, who is wary after the Q2 miss. [draft pasted]
```

You get (shortened):

```
Verdict: Fix then ship.

Reader assumed: board chair, five minutes, looking for whether Q3 repeats
the Q2 miss.
30-second test: partly. The opening is two lines of context before the
word "revenue" appears.

Worst problems
1. "We continue to see strong momentum across the pipeline." No number,
   and this reader is looking for the number. Put the Q3 figure and the
   Q2 comparison in line one.
2. "Churn is expected to normalise." Expected by whom, by when, based on
   what? The chair will ask. Add the basis or cut it.
3. The hiring slip appears only in the last paragraph. The chair will
   find it anyway and wonder why it was placed there.

Substance Test
Filler: "As we look ahead to the coming period..." / "It is worth noting
that..." Needs support: "up 14 percent on Q2" (check against the finance
close). Could not check: every figure in the draft. I took them as given.

Keep: the one-line cash position and the plain account of the Q2 lesson.
```

The same skill, differently pointed:

- **A grant section:** "Our approach is innovative and will transform outcomes" is filler. The reviewer wants the sample size, the comparison and what the money buys. It flags the missing ones.
- **A legal clause summary for a non-lawyer:** the summary says the supplier "may" end the contract. The clause says "at any time without cause, on seven days' notice". The reader will misread "may". It quotes both.
- **A sales email:** the first three lines are about the sender. The buyer's problem is in paragraph four. It tells you to cut the first three.
- **A lab report abstract:** the abstract states a conclusion the methods section does not support. It quotes both passages and lists what to confirm.
- **An AI-generated market summary:** every sentence reads well and half cite no source. The verification list names each claim to trace, and the review says it did not trace any.

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Fix the reader | One line on who reads this, what they know, what they must do, why they might doubt it |
| The 30-second test | Whether the opening, headings and close alone tell the reader the point and the next step |
| The three worst problems | Ranked, each with the exact passage quoted, why it matters to this reader and a one-line fix |
| The Substance Test | Filler marked, claims needing support marked, a verification list, and a plain statement of what could not be checked |
| Skip and misread | What the reader is likely to skip or take the wrong way, with the passage |
| Fix list | Ordered by value per minute, with rough times, cuts included |
| What is good | A short list of what to keep |
| Targeted rewrites | The worst passages only, unless you ask for more |

---

## Who this is for

Anyone about to send, submit, publish or present something and unsure it holds up: a manager, a founder, a researcher, a lawyer, a teacher, an analyst, a grant writer. It works for text in any field because it asks what the reader needs, not whether the prose is good.

It is the natural reviewer for work that came back from a person or a model you handed it to. Bring the output and say what you asked for.

You do not need the source files. If you have them, include them and the claim checks get sharper. If you do not, the skill says which claims it could not check.

---

## What this needs

**Minimum:** the draft, pasted in.

**Better with:** what it is for and who reads it.

**Best with:** the source material behind the claims.

Missing context never blocks this skill. If the purpose or reader is missing, it states its assumption and runs, with at most one question.

---

## Install

As a plugin in Claude Code or Cowork (installs this and the rest of the set):

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

Just this skill, pasted into Claude Code or Cowork:

```
Install the review-my-work skill from https://github.com/theAnirudhKumar/work-design: copy its skills/review-my-work folder into ~/.claude/skills/, keeping the folder name, and tell me the path it landed in.
```

In Claude.ai, zip the `skills/review-my-work` folder and upload it under Customize, then Skills, then Create skill, then Upload a skill. The [main README](https://github.com/theAnirudhKumar/work-design#install) has the other routes.

**Or just read it.** `SKILL.md` is the method, and `assets/review-sheet.md` is the template it fills in.

---

## What this does not do

- **Not fact-checking.** It cannot verify figures, citations, quotations, links or internal data. It lists what to verify and says which claims it took as given.
- **Not a plan review.** For a plan that has not happened yet, use `what-could-go-wrong`. This is for finished or nearly finished work.
- **Not hand-off design.** `delegate` decides what to hand over and what check to attach. This skill is a good way to carry out that check on what comes back.
- **Not a copyedit.** It does not start with typos or style. A clean surface on an empty draft is the problem it looks for.
- **Not a rewrite.** It offers targeted rewrites of the worst passages. A full rewrite is a separate request.
- **Not independent of its own work.** If the draft was written by the same model earlier in your chat, the review shares its blind spots. Someone else should check the facts.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
