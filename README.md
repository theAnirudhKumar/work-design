# work-design

**Design the work before you do it.**

Work design is an old idea with a literature behind it: the study of how work is structured so it is effective and worth doing. Most of that literature is about jobs and teams. This is the same question one level down, at the scale of a single piece of work, and asked before the work starts rather than after it goes wrong.

Three skills for Claude. Each one sits at a moment where a small decision made deliberately saves a large amount of rework: before you adopt a tool, before a session ends, before an expensive request runs.

Nothing here needs a terminal, a workspace, connectors or an API key.

## The skills

| Skill | What it does |
| :--- | :--- |
| [`before-you-install`](skills/before-you-install) | Vets a tool before you sign up. Reads the privacy policy and terms for what they actually permit, finds documented complaints, checks permissions and business model, and ends on install, install with conditions, or do not install. Ships a checklist and a verdict template |
| [`chat-context`](skills/chat-context) | Carries context between chats. Handoff mode writes a structured context file when a session ends; resume mode reads it back and states what was loaded before doing any work |
| [`optimize-tokens`](skills/optimize-tokens) | Spots token-heavy requests before they run and proposes a cheaper approach that gets the same answer. Fires on request, or on its own when a task looks expensive |

Two more are planned: **stack-audit**, for what you already pay for and what overlaps, and **switch-cost**, for what breaks when you leave a tool.

## They work without any setup

You do not need a workspace, a `CLAUDE.md`, a `MEMORY.md`, connectors or file access. Every skill states its floor in a **What this needs** section and runs from there.

| | Works with nothing but | Gets better with |
| :--- | :--- | :--- |
| `before-you-install` | the tool's name | the pricing page, policy or terms pasted in, and web access, which lets it do the research instead of handing you the searches |
| `chat-context` | nothing, the handoff prints in chat to paste forward | file access, which turns handoffs into a saved trail with an index |
| `optimize-tokens` | nothing | nothing |

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

## Credits

Two skills used daily here are other people's work and are not republished. Go to the source:

- [garrytan/gstack](https://github.com/garrytan/gstack), `office-hours` and the rest of Garry Tan's planning stack. MIT
- [blader/humanizer](https://github.com/blader/humanizer), strips AI-writing tells from text, built on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). MIT

## License

[MIT](LICENSE).

---

More at [hustlyst.com](https://hustlyst.com?ref=github) · [anirudhk.com/connect](https://anirudhk.com/connect?ref=github)
