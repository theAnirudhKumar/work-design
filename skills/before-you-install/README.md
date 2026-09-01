# before you install

**Vet a tool before it has your data, not after.**

Every tool's landing page is written by the people selling it. What actually changes your mind - a buried clause in the terms, an old complaint thread, a permission the installer never explains - lives somewhere else, and most people find it six months late.

This skill gets those things before you sign up: what the policy and terms actually permit, how the tool makes money, what the installer asks for that it doesn't explain, and documented complaints from places the vendor can't edit. It names which mode it ran - researched (searches and cites directly) or guided (hands you the searches to run) - and closes on exactly one of three calls.

The failure this exists to prevent: **finding out what you agreed to only after your data is already inside the tool.**

Part of the **Tool lifecycle** group in [work-design](../../#readme).

---

## What it actually does

| Step | What you get |
| :--- | :--- |
| Name the decision, not the tool | Three one-line questions answered first - what goes in, who else is affected, what happens if it disappears in a year - because the same tool passes for one use and fails for another |
| Privacy and data | What the policy actually permits: training on your content, retention after deletion, sub-processors, what "privacy mode" does and doesn't cover |
| Business model | How a free tool makes money, and whether it was acquired or changed terms after being acquired |
| Permissions and footprint | What the installer asks for that has no visible feature behind it |
| The public record | Documented complaint patterns from places the company can't edit - dated, and counted, not just cited once |
| Buried value | The genuinely good thing the marketing page doesn't lead with |
| The call | Install, install with conditions, or do not install - with conditions written as actions, never attitudes |

---

## Who this is for

Anyone deciding whether to bring a tool in, keep paying for one, or leave it, without redoing the research from scratch every time a similar question comes up. It's built for one person with a credit card, not a buying committee - for a company purchase with a procurement process behind it, a vendor-review skill is the right tool instead.

You don't need to be technical. It works from a tool's name typed into a chat window.

---

## What this needs

**Minimum:** the tool's name. Nothing else - it tells you what to go look at and marks every gap it couldn't fill.

**Better with:** the pricing page, privacy policy or terms pasted in, and one line on what you plan to use it for.

**Best with:** all of that plus what you'd be moving off, since the honest question is rarely "is this good" but "is this better than what I have."

Missing context never blocks this skill. Without web access it runs in guided mode - handing you the exact searches and clauses to check rather than guessing at what it would probably find - and it names every check it couldn't run instead of quietly skipping it.

---

## Install

**The easy way: one paste**

```
I want to install the before-you-install skill from
https://github.com/theAnirudhKumar/work-design. Download or clone the
repository, then copy the skills/before-you-install folder into
~/.claude/skills/ (or .claude/skills/ if this is for one project only),
keeping its own folder name. Tell me the exact folder path it landed in
when you are done.
```

**In the Claude app (no terminal needed)**

1. Download this repository as a ZIP, or clone it
2. Zip the `skills/before-you-install` folder on its own
3. In Claude, go to Customize, then Skills, then Create skill, then Upload skill
4. Upload the ZIP

**As a plugin, in Claude Code or Cowork**

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

**Want the whole set?** The [main README's install section](../../#readme) installs all 9 skills at once.

**Or just read it.** `SKILL.md` is the method. `references/` holds the search prompts (`what-to-look-for.md`), a worked example of a tool that fails on design rather than reputation (`worked-example.md`), and notes on writing the verdict up for someone else (`writing-it-up.md`). `assets/` has the checklist you can run yourself (`intel-checklist.md`) and the verdict template (`verdict-template.md`) - both plain markdown you can use without Claude involved at all.

---

## What this does not do

- **Not a procurement process.** No total cost of ownership, no request for proposals, no negotiation - use a vendor-review skill for a company purchase with a committee.
- **Not legal advice.** It reports what a document says. Anything contractual, regulated, or involving another company's data goes to someone qualified, and the output says so.
- **Not a security audit.** It can find that a claim is unaudited. It cannot tell you whether the claim is true.
- **Not a substitute for the reader's own judgement about their own work.** It supplies the facts and the call. The reader knows what's actually in their files.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
