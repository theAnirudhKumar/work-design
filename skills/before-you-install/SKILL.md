---
name: before-you-install
description: >
  Vets a tool before you sign up for it and ends on a call rather than a summary. Trigger whenever the user says "should I use", "is this tool safe", "before I install", "what is the catch", "is it worth paying for", "check this tool", "review this app", "what does their privacy policy actually say", "what are people saying about", "how does this free tool make money", or pastes a product page, pricing page, privacy policy or terms and asks what to make of it. Also trigger when they are choosing between two tools they might pay for, or when they have already installed something and want to know what they agreed to. It reads the policy and terms for what they permit, finds documented complaints and controversies, checks permissions and business model, and finishes on install, install with conditions, or do not install. Runs with or without web access and states which. Use a vendor-review or procurement skill for a company purchase with a buying committee; this one is for one person with a credit card.
---

# Before You Install

Every tool page is written by the people selling it. The things that change your mind are somewhere else: in clause 7 of the terms, in a support thread from eight months ago, in the permission the installer asks for and does not explain.

The failure this exists to prevent: **finding out what you agreed to after your data is already in it.** Not a hack, not a scandal. The ordinary case where someone reads the terms six months late and discovers the answer was public the whole time.

This is not a takedown and not a warning label. It is the briefing a knowledgeable friend gives you before you commit, and it stays useful precisely because it will also tell you a tool is fine.

---

## What this needs

**Minimum: the tool's name.** Nothing else. It will tell you what to go and look at, and mark every gap it could not fill.

**Better with** the pricing page, privacy policy or terms pasted in, and one line on what you plan to use it for.

**Best with** all of that plus what you would be moving off, since the honest question is rarely "is this good" but "is this better than what I have".

### Two modes, and say which one you ran

**Researched mode.** You have web access. Do the searching yourself. Read the actual policy, find the actual threads, and cite what you found.

**Guided mode.** You have no web access. Do not guess, and do not reason from what the tool is probably like. Hand over the exact searches to run and the exact clauses to look for, take back what the reader finds, and read that.

Guided mode is not the degraded version. Most people asking this question are in a chat window with nothing connected, and a skill that quietly invents a privacy policy is worse than no skill. **Name the mode in the first line of the output**, so the reader knows whether they are looking at findings or at homework.

Half and half is normal. Say so: found the pricing page, could not reach the forum, here is what to check yourself.

---

## Step 0: Name the decision, not the tool

Ask what they are actually deciding before checking anything. The same tool passes for one use and fails for another.

Three questions, and they take one line each:

1. **What goes into it?** Public marketing copy is a different risk from customer records, health information, or anything under an employer's contract.
2. **Who else is affected?** A tool that only touches your own notes is your call. One that reads a shared inbox, records other people, or holds client work is not.
3. **What happens if it disappears in a year?** Small tools close. If the answer is "I lose a habit" the bar is low. If it is "I lose the data" the bar is high, and export matters more than features.

Where the answer to 2 is "other people who did not agree to this", say so plainly and early. That is the finding most likely to change the call, and the one the reader least expects.

---

## Step 1: Run the five checks

Full prompts and search strings are in `references/what-to-look-for.md`. The checklist the reader can run themselves is `assets/intel-checklist.md`. In guided mode, hand them that file's contents rather than describing it.

**1. Privacy and data.** Where does the content go, and what may they do with it once it is there? Training on user content, retention after deletion, sub-processors, and what a "privacy mode" covers and does not.

**2. Business model.** How does it make money. A free tool is being paid for somehow, and the answer is usually fine and occasionally the whole story. Check for an acquisition, and whether terms changed after it.

**3. Permissions and footprint.** What the installer asks for and why. Screen recording, accessibility access, clipboard, microphone, background processes, startup items. A permission with no visible feature behind it is the thing to ask about.

**4. The public record.** What people say where the company cannot edit it. Forum threads, complaint patterns, how the company responded when criticised. A pattern repeated by many people over months is evidence; one angry post is not.

**5. Buried value.** The genuinely good thing the marketing page buries. This check is what keeps the skill honest, because a process that only ever finds problems is a process nobody trusts on the day it says yes.

### Evidence rules

- **Documented or confirmed only.** No speculation. "I could not confirm this" is a finding and belongs in the output.
- **Separate the claim from the verification.** "The maker states X" and "X is independently audited" are different sentences. Never merge them.
- **Date what you find.** A policy changes. A two-year-old thread may describe a fixed problem. Say when.
- **Count the complaints.** One person is an anecdote.
- **Name what you could not check**, every time. This is the part most reviews skip and the part that makes the rest believable.

---

## Step 2: Weigh it against the actual use

A finding is not a verdict. Take each one back to Step 0.

Training on user content is close to irrelevant for drafting social posts and disqualifying for client work under a confidentiality agreement. Screen recording is the product in a screen recorder and alarming in a note-taker. Ten users is fine for a to-do list and material for anything holding credentials.

Where a finding only bites under some conditions, say which. "Fine for your own notes, not for anything a client owns" is more use than a risk rating.

---

## Step 3: Make the call

Finish on one of three. Anything else is a summary pretending to be advice.

| The call | What it means |
| :--- | :--- |
| **Install** | Nothing found that changes the decision for this use. Say what you checked, so the reader can see the yes was earned |
| **Install with conditions** | Usable if specific things are true. Name them as actions: turn this setting off, keep this category of work out of it, export monthly, revisit if acquired |
| **Do not install** | For this use, the cost is real and not fixable by a setting. Say which finding decides it, and name the alternative if there is one |

Two rules on the call:

**Conditions must be actions**, not attitudes. "Be careful with sensitive data" is not a condition. "Do not put anything under a client confidentiality agreement into it, because the terms permit training on uploaded content" is.

**Do not install is about a use, not a verdict on the product.** The password-agent example in `references/worked-example.md` is early, thoughtfully built, and still a stop, because the design requires exporting every credential to a plain text file first. Say it that way.

Fill in `assets/verdict-template.md`. Where the write-up is going into an article, review or a message to a team, `references/writing-it-up.md` covers tone and placement.

---

## What this does not do

- **Not a procurement process.** No total cost of ownership, no request for proposals, no negotiation. Use a vendor-review skill for a company purchase with a committee.
- **Not legal advice.** It reports what a document says. Anything contractual, regulated, or involving another company's data goes to someone qualified, and the output should say so.
- **Not a security audit.** It can find that a claim is unaudited. It cannot tell you whether the claim is true.
- **Not a substitute for the reader's own judgement about their own work.** It supplies the facts and the call. The reader knows what is actually in their files.
