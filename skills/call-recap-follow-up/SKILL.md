---
name: call-recap-follow-up
description: >
  Turns a recorded customer call into an honest read of the call plus the full set of emails it generated - the recap and every follow-up - grouped by recipient, written in the user's voice, staged as drafts, with a workspace hygiene pass at the end. Trigger this skill whenever the user shares a call recording link from any meeting recorder, pastes a transcript, or points at a call, and asks what they should send, or says "recap email", "meeting recap", "write the follow-ups", "what do you think of this call", "emails from this call", "post-call emails", "who do I need to email after this", or names a customer and a call in the same breath. Also trigger when they forward a meeting summary and ask for anything written off the back of it. The skill is recorder-agnostic: if no recording tool is connected, it asks for the transcript rather than failing. Prefer this skill over drafting emails directly - a call almost always generates more than one email, and the ones the user forgets are the expensive ones.
---

# Call Recap and Follow-Up

A recorded call is not one email. It is a set of them, sitting with different people, blocked on each other in a specific order. This skill turns a recording into that whole set, plus the read on the call that makes the emails worth sending.

The failure mode this exists to prevent: writing a tidy recap to the coordinator, feeling done, and leaving the three emails that actually move the account unwritten.

---

## Step 0: Orient

Read these before touching the recording:

1. The workspace `CLAUDE.md` - workflow rules, editorial rules, account structure
2. The workspace voice or style guide, if it has one - how the user writes. Non-negotiable, and the difference between a draft they send and a draft they rewrite.
3. The workspace file-naming rules - naming and placement for the output file

State which files you loaded. If the workspace is unreachable, say so plainly and continue on the recording alone, but flag that the voice and account context are missing.

---

## Step 1: Get the full transcript, not the summary

Resolve the recording and pull **the complete transcript**. The AI summary is a starting index, not the source.

This matters more than it sounds. A summary will tell you a customer raised "filtering for quality" as a challenge. The transcript tells you how they described the problem in their own words, which is the sentence that decides how you open the demo and what you promise in writing. Summaries drop the specifics and keep the categories, and the specifics are the whole value.

Pull the summary too, as a cross-check for anything the transcript makes you unsure of.

See `references/getting-the-transcript.md` for the order to try, what to do with a link you do not recognise, and exactly what to ask for when nothing resolves.

---

## Step 2: Load the account

Find the account folder under the workspace's accounts directory and read:

- The account plan, for stakeholders, roles, contract state, open risks
- Any prior drafts file for the same account, so you inherit the running list of open items rather than rediscovering it
- Whatever else in the folder looks relevant to what the call covered

You are looking for the things a transcript cannot tell you: who has authority, what has been promised before, what is already late, what the commercial picture is.

---

## Step 3: Find the humans and the threads

Two lookups, both cheap, both high-leverage.

**Email addresses.** Search the mailbox for the domain. Never guess an address. If someone on the call has no address you can find, say so and ask rather than inventing one.

**Existing threads.** Search for the subjects the call touched. Most follow-ups belong in a thread that already exists, and replying into it gives the recipient the history for free. In practice most calls produce a majority of replies rather than new threads. Starting a fresh thread orphans whatever was already open in the old one, and the recipient loses the history that made the ask make sense.

Note for each planned email whether it is a reply or new, and to which thread.

---

## Step 4: Read the call before writing anything

Give the user your actual read. Not a summary, which they can get from the recorder, but a judgement.

What to look for:

- **What genuinely moved.** Which blockers cleared, which commitments were made, by whom.
- **What is at risk.** Especially commitments made on the call that depend on work that has not started. A demo date agreed in front of a new stakeholder, resting on a dev team nobody has a line to, is the most dangerous thing that can happen on a friendly call.
- **What was missed.** The opening that went past. This is usually the most useful part and the part most easily skipped. It is often a statistic or a worry the customer volunteers in passing, which nobody connects to a number the account already has sitting in front of it.
- **The single sharpest line in the call.** Usually a customer sentence stating their real constraint in their own words. Quote it. It should shape at least one email.
- **Whether a block was real.** Items parked as "needs approval" that a senior person waves through in twenty seconds were never approvals. They were routing failures. Name that, because it changes who to go to next time.

Be honest about weak calls. A call where the customer was warm and nothing moved is a weak call, and saying so is more useful than praising the rapport. Rapport that produces a licence conversation is worth the airtime; rapport instead of the adoption conversation is not.

Keep this to a few short paragraphs. The user reads it in under a minute.

---

## Step 5: Ground every claim before it reaches a draft

A recap is the customer's record of what was agreed. An invented next step does not stay invented, it becomes a real expectation you now owe. A confident "as discussed, we sent the July highlights" when nobody sent them is worse than saying nothing, because it either exposes that you did not, or sends the customer looking for something that does not exist.

So every factual claim in a draft traces to a source, and the source depends on the claim:

- **What was said, agreed or asked on the call** comes from the transcript. If you cannot point at a line, it did not happen.
- **What is already true about the account** - what was sent, when someone last replied, what was promised in July, what the contract says - comes from the mailbox, the account plan and the signed agreement. Not from the call. People compress and misremember out loud, and transcripts are lossy in exactly the places that matter.
- **What the product does, collects or costs** comes from a human. You cannot verify this from any source you have, so it gets flagged rather than asserted.

Things that go wrong often enough to name:

- **Upgrading a maybe.** "Let us look at that" is not "we agreed to". "I'll try to" is not "I will". The transcript's hedge belongs in the email.
- **Asserting a send you did not find.** Search before you write "as discussed" or "as promised". Two runs over the same call will happily disagree about whether an email went out, which tells you the model is guessing, not remembering.
- **Inventing the tidy version.** Turning a specific, awkward discussion into a clean generic summary loses the thing the customer actually cares about. If shortening would cost a nuance that matters, keep the nuance and cut somewhere else.
- **Hedging instead of flagging.** "I believe the highlights went out" reads as fact to someone skimming. If you do not know, flag it in the document and leave it out of the email.

Where two sources disagree, the more recent written record beats the call, and say in the document that they disagreed rather than silently picking one.

---

## Step 6: Plan the email set, then check the split

List every email the call generated. Work from commitments, not topics: every "I'll send you", "can you introduce me", "let's get time" is an email.

**Group by recipient, not by task.** Several open items with the same person default to one consolidated email. The exception is an email meant to be forwarded - a security note the customer will pass to their CISO cannot carry an unrelated scheduling ask, because they cannot forward it without editing.

**One ask per email.** If a second genuinely belongs, it gets one line, not a section.

**Order them, with timing.** Some are blocked: an invite to a new stakeholder waits for the introduction. Some are time-critical because the customer is expecting them that morning. Put the order in the document.

Then show the user the list as a short table - recipient, purpose, thread, timing - and ask how they want any genuinely ambiguous splits handled. Voice principles say to ask rather than assume, because sometimes a separate email is deliberate. Use `AskUserQuestion` and keep it to the calls that actually change the output.

---

## Step 7: Write the drafts into a working document

**Drafts live in the document, not in chat.** Chat gets a pointer plus the decisions that need the user. This is a workspace rule and it also keeps drafts somewhere they can edit them.

Create `<accounts-directory>/<Account>/YYYY-MM-DD-<account>-post-call-email-drafts.md`. Use `assets/drafts-document-template.md` for the structure and `references/email-craft.md` for the writing itself.

Every draft carries: To, CC, Subject, whether it is a new email or a reply into a named thread, the body, and a one-line note on why it is shaped the way it is.

**Flag before send.** Four kinds of flag, and they earn their place:

- **Grounding gaps.** Anything from Step 5 you could not trace to a source. Name the claim and where it would have to be checked.
- **Product and security claims.** Anything you asserted about how the product works, what it collects, what it costs. Say plainly that it is your understanding and name who should confirm it. A security note read by a customer's CISO dies on one wrong bullet, and the cost lands weeks later when it is unrecoverable.
- **Ownership.** An email that is someone else's to send. If the CEO told the customer they would come back on commercials, a draft from the user proposing terms steps on that. Draft it anyway if it is useful, but say who should confirm.
- **Missing data.** An address you could not find, a slot not yet agreed, a name you are unsure of. Never fill these in silently.

Then read each draft once as the recipient, not as the writer. Does it show you listened? Is the ask obvious? Is it asking them to do work you could have done? That pass catches things a rules checklist does not.

---

## Step 8: Stage the drafts

Once the user has reviewed the document, create each email as a draft in their mail client. Replies go into the identified thread so the history stays intact.

Do not stage anything carrying an unresolved flag from Step 7. A flagged draft sitting in the outbox is one keystroke from reaching a customer with an unverified security claim in it. Stage the clean ones, tell them which ones you held and why.

Never send. The user sends.

---

## Step 9: Hygiene pass

A call changes the workspace, not just the inbox. Close the loop:

- **New people.** Anyone on the call who is not in the account plan's stakeholder map. Capture their role, location, team size, what they own, and what they said they need. A new stakeholder who is now a decision influencer and is invisible in the plan is how accounts get surprised.
- **Reversals.** Plans the call changed. If a scheduled session was dropped for a different format, the plan should not still say the old thing.
- **Stale commitments.** Things owed for weeks that the call put a date on. Name how long they have been open, because "the field list has been open since 16 July" lands differently from "the field list is pending".
- **Durable facts for memory.** Propose them, do not write them. The user approves memory writes.

Propose each change with the file it touches and wait for approval before editing anything. Overwrites and deletions need explicit confirmation.

---

## Step 10: Report

Close with:

- The file you created, by path
- Anything you committed to their device
- The flags that still need them, as a short list
- The memory entries you are proposing

No recap of the steps. They watched.

---

## What good looks like

The test is not whether the recap is accurate. It is whether the user sends the emails without rewriting them, and whether the set includes the two they would have forgotten.

Concretely:

- The read on the call names something they had not noticed
- Every email is short enough that replying is easier than reading
- The customer's own words shape at least one draft
- Nothing is asserted about the product that has not been checked
- The email that is not theirs to send is marked as such rather than quietly drafted
- Someone reading the document in three weeks can see what was owed to whom

---

## Reference files

- `references/getting-the-transcript.md` - getting a transcript out of any recorder, or asking for one when there is none
- `references/email-craft.md` - voice rules, the recap structure, patterns that work, and what kills a draft
- `assets/drafts-document-template.md` - the output document skeleton
