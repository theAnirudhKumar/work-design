---
name: work-design
description: >
  Opens the work-design menu. Trigger when the user says "work-design", "which
  work-design skill", "what can work-design do", "what skills do I have for
  work", "show me the work-design menu", "I have a piece of work and don't know
  which skill to use", or asks what to run at a given stage of a piece of work
  (before, during, after). Asks at most one question, which stage the work is
  at, then names the one or two skills that fit, with the exact phrase to say.
  Never does the work of those skills itself. Defers immediately when the
  user's message already matches a sibling's own trigger phrases, such as "where
  do I start", "I'm stuck", "how long will this take" or "review this", and
  those skills handle the request directly.
---

# Work Design

A map of the whole set, for the moment someone has work to do and cannot remember what is installed or what it is called.

The failure this exists to prevent: **never starting, or never finishing, because the set is a long list and nobody remembers which skill fits the moment they are in.** This skill does one thing, which is to turn "I have work" into "say this phrase".

---

## What this needs

**Nothing.** It runs from the words "work-design" or from a description of where the work stands. It reads no files and calls no tools.

---

## When this runs

Run when the user asks for the menu, asks which skill to use, or describes a piece of work without a request that matches one skill's own triggers.

Do not run when the message already contains a sibling's trigger phrase. If the user says "I'm stuck", `get-unstuck` owns that message. If the user says "is this good enough to send", `review-my-work` owns it. Step aside rather than add a menu in front of an answer.

---

## Step 1: Place the work on the line

Every piece of work passes the same moments, and quality is mostly decided at six of them. Ask one question only if the stage is not clear from the message: **"Where is this work: not started, planned but not run, in progress, or finished?"**

| Stage | The moment | Say this | Skill |
| :--- | :--- | :--- | :--- |
| **Start** | You have a task and no plan | "Where do I start on this?" | `plan-the-work` |
| **Start** | The ask keeps growing | "What's in and out of this?" | `scope-the-work` |
| **Start** | Time is fixed, the work is bigger | "I only have until Friday" | `fit-to-deadline` |
| **Start** | You need a duration | "How long will this take?" | `how-long-will-it-take` |
| **Start** | Plan exists, you want it tested | "What could go wrong with this?" | `what-could-go-wrong` |
| **Run** | You are not moving | "I'm stuck" | `get-unstuck` |
| **Run** | Part of it could go to an AI or a person | "What should I hand off?" | `delegate` |
| **Run** | You need an answer from people | "Meeting or message?" | `meeting-or-message` |
| **Run** | The chat is long or costly | "Carry this into a new chat" / "This is getting expensive" | `continue-in-new-chat`, `cut-token-cost` |
| **Review** | You have a draft | "Is this good enough to send?" | `review-my-work` |
| **Learn** | It is finished or dropped | "What did we learn?" | `lessons-learned` |
| **Tools** | Before, during and after buying one | "Should I sign up for X?" / "What am I paying for?" / "Can I leave X?" | `before-you-install`, `audit-my-tools`, `before-you-switch` |

If the work is a meeting, point to the separate `meeting-design` set: `meeting-design` before, `meeting-close` after, `meeting-audit` for recurring ones. It lives at github.com/theAnirudhKumar/meeting-design.

---

## Step 2: Name the one or two that fit

Reply with at most two skills from the table, each as: the skill name, one sentence on what it will hand back, and the exact phrase to say. If the user is at the very start of something unclear, the answer is `plan-the-work`.

If a skill in the table is not installed, say so plainly and name the install command from the README, rather than imitating the skill.

---

## Output

A short answer in chat: the stage, the one or two skills, the phrase to say for each. No plan, no review, no estimate. If the user asks this skill to do the work itself, name the skill that does it and stop.

---

## Failure modes

- **Doing the sibling's job.** The moment this skill starts drafting a plan or critiquing a draft, it has stolen routing and produced a thinner answer than the real skill. Hand off instead
- **Interrogating.** One question at most. A guess at the stage, stated, beats a questionnaire
- **Listing everything.** The table is for the skill's reference. The user gets one or two names
- **Firing on specific requests.** If a sibling's trigger phrase is already in the message, this skill steps aside

---

## What I had to assume

State the stage that was assumed when the user did not say.
