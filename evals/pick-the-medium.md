# Evaluation: pick-the-medium

Routing cases for `pick-the-medium`, run against the seven descriptions in this repository as they stand with this skill added. Written alongside the skill, per `CONTRIBUTING.md`.

**Run on:** 31 Aug 2026, against Haiku, Sonnet and Opus.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Should I send Sarah a message about this or hop on a call?" | fire | pick-the-medium | pick-the-medium | pick-the-medium |
| 2 | "Is this worth pulling the whole team into a meeting, or can I just write it up and send it around?" | fire | pick-the-medium | pick-the-medium | pick-the-medium |
| 3 | "Should I sign up for Asana for our team?" | before-you-install | before-you-install | before-you-install | before-you-install |
| 4 | "What should I hand to Claude versus do myself on this report?" | delegate | delegate | delegate | delegate |
| 5 | "We've been going back and forth over email for three days on this decision. Should we just get on a call?" | fire | pick-the-medium | pick-the-medium | pick-the-medium |
| 6 | "Build me an agenda for tomorrow's kickoff meeting." | none | none | none | none |
| 7 | "Can you summarize what we talked about in this chat before I close it?" | none | none | none | none |
| 8 | "How long will this migration realistically take before I decide whether to switch?" | switch-cost | switch-cost | switch-cost | switch-cost |

Eight of eight agree across all three models. No split, no disagreement.

---

## Cases 1, 2 and 5, the skill's own territory

Three shapes of the same question: message versus call, meeting versus write-up, and a failing async thread asking whether to escalate to sync. All three fired `pick-the-medium` cleanly on every model. Case 2 is worth noting specifically: a meeting is one of the two options on the table, and the message still routed to `pick-the-medium` rather than being treated as a meeting request, because the question is which medium to use, not how to run a meeting once chosen. The boundary the description draws (deciding the channel is this skill's job; building what happens inside a chosen meeting is not) held under a case designed to blur it.

## Case 6, the meeting-design boundary held with no competing skill in the room

This is the case this eval exists to check. `meeting-design` is not a skill in this repository, so nothing here was competing with `pick-the-medium` for this message on routing grounds alone. It still declined on all three models, citing the skill's own stated exclusion (agenda-building is explicitly not this skill's job) rather than reaching for the nearest available skill. That is the intended failure mode working from the inside: the description's own carve-out, not an external competitor, is what kept the skill from overreaching into meeting-design's territory. The trigger vocabulary was checked directly against `meeting-design`'s actual shipped description in the sibling repo (`theAnirudhKumar/meeting-design`) before this skill's own description was finalized, and none of its phrases ("plan this meeting", "build an agenda", "agenda for", "run a workshop", "facilitate", "offsite", "kickoff", "planning session") appear in `pick-the-medium`'s trigger list.

## Case 3, 4 and 8, the neighbours hold

Case 3 (adopting a single new tool) went to `before-you-install`, case 4 (splitting AI vs. self work) went to `delegate`, and case 8 (migration hours before a switch decision) went to `switch-cost`. None pulled toward `pick-the-medium` despite each involving a decision of some kind. `pick-the-medium`'s territory is specifically the channel for one piece of communication or coordination, not decisions in general, and the eval confirms the three-way boundary holds against the closest neighbours already in this repository.

## Case 7, an honest boundary check on chat-context

Built to test whether a chat-scoped request would pull toward `chat-context` on proximity alone. It did not: all three models cited `chat-context`'s own explicit exclusion (a request to summarise the chat back in conversation gets a summary, not a handoff) and returned none, since no skill in this repository does in-chat summarisation. Consistent with `evals/stack-audit.md`'s case 5 and `evals/switch-cost.md`'s case 6: an honest gap, not a forced fit.

---

## Not tested here

Whether `optimize-tokens` competes with `pick-the-medium`. Neither skill's trigger vocabulary overlaps with channel or medium language, and optimize-tokens's own recorded cases do not mention meetings, calls or messages, so no case was constructed. Worth a check the day either description changes again.

**The actual meeting-design hand-off.** This eval can only confirm that `pick-the-medium` declines to build an agenda itself; it cannot test what happens when both skills are installed together and a router has to choose between them, since `meeting-design` lives in a separate repository. Worth a real check if the two are ever installed side by side.

**Output behaviour.** Whether the skill actually weighs reversibility over habit in a live session, whether the runner-up and its cost get named rather than skipped, and whether the hand-off line reads as a genuine stop rather than a soft suggestion. All output checks, not routing.

**Real sessions.** Every case here is constructed, same limitation as every other file in this directory.

---

## Field test, 2026-08-31

Two real cases, not constructed, both checked against `meeting-design`'s own Step 0 independently, answering the "actual hand-off" gap this file names above. A single factual policy question that had blocked a customer-facing deliverable for over a week resolved to a written message with a deadline, no hand-off, and `meeting-design`'s Step 0 agreed a document/message was right without being told the other skill's answer. A separate case, eight open decisions on a reporting rebuild owed by two internal stakeholders, resolved to a meeting, handed off cleanly, and `meeting-design`'s agenda step mapped directly onto the eight named decisions. Both directions held. Not a live `Skill` tool run, neither skill is installed in this account. Case detail is internal and not reproduced here.
