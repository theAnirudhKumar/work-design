# work-design

**Design the work before you do it.**

work-design is a small set of Claude skills that make a decision about how a piece of work will run before the work starts, not after it goes wrong: whether to install a tool, whether to keep paying for one, what to hand to an agent and what to keep, how to carry context from one session into the next, and when a request is about to cost more than it needs to.

Eight skills, each built around one moment where a small decision made deliberately saves a large amount of rework later. Every skill ends on something to act on: a verdict, a filled table, a template, never just advice. Nothing here needs a terminal, a workspace, connectors or an API key.

*The name borrows from a real field. Organisational psychology has studied work design for a century; this repository asks the same question one level down, at the scale of a single piece of work rather than a job or a team. The literature behind that framing is under [Research](#research) at the bottom.*

## The skills

Three categories. A skill belongs to a category once it ships; a category with nothing shipped in it yet does not appear here.

**Tool lifecycle:** deciding whether to bring a tool in, and what it costs to keep or leave.

| Skill | What it does |
| :--- | :--- |
| [`before-you-install`](skills/before-you-install) | Vets a tool before you sign up. Reads the privacy policy and terms for what they actually permit, finds documented complaints, checks permissions and business model, and ends on install, install with conditions, or do not install. Ships a checklist and a verdict template |
| [`stack-audit`](skills/stack-audit) | Audits the tools you already pay for. Builds an inventory with cost, last use and overlap, gives every row a verdict of keep, cancel, downgrade or consolidate, and leads with the total it would free up. Ships an inventory table |
| [`switch-cost`](skills/switch-cost) | Checks what breaks before you leave a tool. What exports and in what format, what is lost outright, and what the move costs in hours. Ends on low, conditional, or high switching cost. Ships an exit checklist |

**Deciding how work runs:** the shape of a piece of work itself, before you decide who does it or how.

| Skill | What it does |
| :--- | :--- |
| [`pick-the-medium`](skills/pick-the-medium) | Picks the channel for one piece of communication before it happens: a message, a call, a document, or a meeting. Weighs reversibility and who needs to be live, and hands off to a meeting-design skill the moment the answer is a meeting. Ships a one-page medium call |
| [`scope-the-work`](skills/scope-the-work) | Draws the boundary of one piece of work before it starts. Writes the in list, the out list, a checkable done condition, and who can move the line if something has to change. Ships a boundary note |

**Working with agents:** what to hand over, what to keep, and what a session carries forward.

| Skill | What it does |
| :--- | :--- |
| [`chat-context`](skills/chat-context) | Carries context between chats. Handoff mode writes a structured context file when a session ends; resume mode reads it back and states what was loaded before doing any work |
| [`delegate`](skills/delegate) | Decides what to hand to an agent and what to keep, for one piece of work. Splits the work, allocates each part to you, another person or a model, and attaches a check and a stop condition to everything that leaves your hands. Ships an allocation table |
| [`optimize-tokens`](skills/optimize-tokens) | Spots token-heavy requests before they run and proposes a cheaper approach that gets the same answer. Fires on request, or on its own when a task looks expensive |

## They work without any setup

You do not need a workspace, a `CLAUDE.md`, a `MEMORY.md`, connectors or file access. Every skill states its floor in a **What this needs** section and runs from there.

| | Works with nothing but | Gets better with |
| :--- | :--- | :--- |
| `before-you-install` | the tool's name | the pricing page, policy or terms pasted in, and web access, which lets it do the research instead of handing you the searches |
| `chat-context` | nothing, the handoff prints in chat to paste forward | file access, which turns handoffs into a saved trail with an index |
| `delegate` | a description of the work | what the output is for and who sees it, which is what sets how hard the checks have to be |
| `optimize-tokens` | nothing | nothing |
| `pick-the-medium` | what needs to get decided or conveyed | how reversible the decision is and whether this will come up again in this shape, which is what tells a one-off from a pattern worth fixing |
| `scope-the-work` | what the work is and roughly what finished looks like | who asked for it and what they actually need it for, and a case where this same work grew before, which is what makes the out list specific instead of generic |
| `stack-audit` | a list of tool names from memory | a card statement, bank export or subscription list pasted in, which turns last use from a guess into a fact |
| `switch-cost` | the tool's name | what is actually stored in it, and the destination tool named, which turns the estimate from a category guess into an answer about this account |

Missing context never blocks a skill. It changes what the skill can honestly claim, and each one says which checks it could not run rather than guessing around the gap.

## Install

### Claude Code and Cowork

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

### Claude.ai

Package a skill's folder as a ZIP, then go to **Customize > Skills**, click **+**, choose **Create skill** and then **Upload a skill**. The folder name inside the ZIP must match the skill's `name` in its frontmatter, or the upload is rejected. See [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

### Claude API

Follow the [Skills quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill).

### By hand

Copy any skill folder into `~/.claude/skills/<skill-name>/` for all your projects, or `.claude/skills/<skill-name>/` inside one repo. It loads on the next session.

## Looking for customer success skills?

`call-recap-follow-up` and `email-critic` used to live here. They are maintained in one place now, at [CSPulse/customer-success-skills](https://github.com/CSPulse/customer-success-skills), alongside fourteen others for reading an account, running the set-piece moments and handling the conversations.

## Writing your own

[`template/SKILL.md`](template/SKILL.md) is a starting structure, and [CONTRIBUTING.md](CONTRIBUTING.md) has the standard this repository holds itself to. Two things matter more than the rest:

The description is the trigger. Claude decides whether to run a skill by reading its description, so list the actual phrases someone says when they want it. A description explaining what a skill *is* rather than when it *fires* produces a skill that never runs.

Write instructions, not documentation. "Read the transcript in full" works. "This skill reads transcripts" does not.

Anthropic's [Agent Skills spec](https://github.com/anthropics/skills/tree/main/spec) is the reference for the format itself.

Before opening a pull request, run `python3 validate-skills.py`. The same script runs on every pull request.

Every skill also carries a file in [`evals/`](evals): the prompts that should make it fire, the near misses that should not, and what three models actually did with each. Routing happens on the description alone, so this is the only check that tests the thing most likely to be wrong.

## Research

Work design is a real field with a century of research behind it, defined by [Parker, Morgeson and Johns (2017)](https://espace.curtin.edu.au/bitstream/handle/20.500.11937/69907/70119.pdf?sequence=2) as "the content and organization of one's work tasks, activities, relationships, and responsibilities." Its academic centre is the [Centre for Transformative Work Design](https://www.transformativeworkdesign.com/about-work-design) at Curtin University. Both study jobs and teams; `work-design` asks the same question at the scale of a single piece of work, which is where the name comes from.

## Credits

Two skills used daily here are other people's work and are not republished. Go to the source:

- [garrytan/gstack](https://github.com/garrytan/gstack), `office-hours` and the rest of Garry Tan's planning stack. MIT
- [blader/humanizer](https://github.com/blader/humanizer), strips AI-writing tells from text, built on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). MIT

## License

[MIT](LICENSE).

---

More at [hustlyst.com](https://hustlyst.com?ref=github) · [anirudhk.com/connect](https://anirudhk.com/connect?ref=github)
