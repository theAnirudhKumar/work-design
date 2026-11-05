# work-design

**Do better work, on purpose. Skills for the moments when the quality of a piece of work is decided: the start, the middle and the check before it goes out.**

Most bad work was bad at the start: nobody said what it was for, what done looks like, or what to leave alone. Most late work was never cut to fit its deadline. Most polished-looking work was never really read before it was sent. These sixteen Claude skills sit at those moments, in any field, and each hands back something you can use: a one-page plan, a ranked cut list, a verdict on a draft.

The names are the sentences you would say anyway. If you cannot remember a name, say what you are about to do, or say **work-design** and it will point you to the right one.

None of them needs a terminal, a workspace, connectors or an API key. They work from what you type.

## See it work

You type:

```
I have to run the customer survey for Brightwell Cycles. I don't know where to start.
```

You get, from [`plan-the-work`](skills/plan-the-work) (shortened, illustrative, invented company):

```
Work Card: Brightwell Cycles customer survey

Outcome      By Friday the owner has a one-page summary of what 100+ customers
             say about delivery, and a yes/no on changing courier.
Appetite     Up to 10 hours. A courier change is worth a survey, not a study.
Done looks   Survey sent and test-checked on a phone / 100+ replies or a stated
like         reason / page answers "change courier?" in its first line
Out of scope Pricing questions. Website feedback. A repeat survey next quarter.
Biggest      Too few replies. If under 40 by Wednesday noon, send one reminder
risk         and report the count with the result.
First move   Write the three questions on paper before opening any survey tool.
Assumed      The courier contract renews at month end. Correct me if not.
```

That is the whole idea. Before the work starts, one page; while it runs, a skill for the moment it stalls; before it goes out, a skeptical reader; when it ends, a log. Everything else here serves one of those.

## Which one do I need?

Say the sentence on the left. The skill on the right picks it up.

### Before you start

| You are thinking | Say or use | You get |
| :--- | :--- | :--- |
| "Where do I even start?" | [`plan-the-work`](skills/plan-the-work) | A one-page Work Card: outcome, appetite, done criteria, biggest risk, first move |
| "I only have until Friday" | [`fit-to-deadline`](skills/fit-to-deadline) | Minimum, target and stretch versions, a ranked cut list, a midpoint rule |
| "How long will this really take?" | [`how-long-will-it-take`](skills/how-long-will-it-take) | Your guess next to what similar work took, and a corrected range |
| "What exactly am I committing to?" | [`scope-the-work`](skills/scope-the-work) | A boundary note: in, out, done, who can move the line |
| "What could go wrong with this plan?" | [`what-could-go-wrong`](skills/what-could-go-wrong) | Failure causes specific to your plan, each with an early warning and an if-then response |

### While you work

| You are thinking | Say or use | You get |
| :--- | :--- | :--- |
| "I'm stuck" | [`get-unstuck`](skills/get-unstuck) | A diagnosis of why, and one next action of 15 minutes or less |
| "What should I hand to an AI?" | [`delegate`](skills/delegate) | An allocation table: each part, who does it, the check, when to take it back |
| "Meeting or message?" | [`meeting-or-message`](skills/meeting-or-message) | One medium, the runner-up, and what the runner-up would cost |
| "This chat got long and slow" | [`continue-in-new-chat`](skills/continue-in-new-chat) | A handoff to paste into a fresh chat, and a resume that reads it back |
| "This is eating my usage" | [`cut-token-cost`](skills/cut-token-cost) | The same request, rewritten leaner, with the quality impact stated |

### Before it goes out

| You are thinking | Say or use | You get |
| :--- | :--- | :--- |
| "Is this good enough to send?" | [`review-my-work`](skills/review-my-work) | Ship, fix then ship, or rework, the three worst problems with quoted passages, and what to verify |

### When it is done

| You are thinking | Say or use | You get |
| :--- | :--- | :--- |
| "What did we learn?" | [`lessons-learned`](skills/lessons-learned) | Planned vs actual, one change for next time, and a log entry that feeds `how-long-will-it-take` |

### Tools you buy

| You are thinking | Say or use | You get |
| :--- | :--- | :--- |
| "Should I sign up for X?" | [`before-you-install`](skills/before-you-install) | Install, install with conditions, or do not, with the clauses behind it |
| "What are we paying for?" | [`audit-my-tools`](skills/audit-my-tools) | Every subscription with a verdict, and the total you would free up |
| "Can I leave X?" | [`before-you-switch`](skills/before-you-switch) | What exports, what is lost, the hours, and a low, conditional or high verdict |

### Lost?

| You are thinking | Say | You get |
| :--- | :--- | :--- |
| "I have work and don't know which skill" | [`work-design`](skills/work-design) | The one or two skills that fit, and the phrase to say |

## Start here

Three skills cover most weeks. Install these first.

| Skill | Why |
| :--- | :--- |
| [`plan-the-work`](skills/plan-the-work) | Fixes the start, which is where most of the damage is done |
| [`get-unstuck`](skills/get-unstuck) | Fixes the middle, when nothing is moving |
| [`review-my-work`](skills/review-my-work) | Fixes the end, the check before it goes out |

## They work without any setup

Every skill states its floor in a **What this needs** section and runs from there. Most need only a sentence describing the work or the draft pasted in. Missing context never blocks a skill. It changes what the skill can honestly claim, and each one says which checks it could not run instead of guessing around the gap.

## Install

### Claude Code and Cowork

```
/plugin marketplace add theAnirudhKumar/work-design
/plugin install work-design@work-design-marketplace
```

That installs all sixteen. For just the three in [Start here](#start-here), install `work-design-starter@work-design-marketplace` instead.

### One skill

If your AI tool can read and write files on your computer (Claude Cowork, Claude Code, or similar), paste this, naming the skill you want:

```
Install the <skill-name> skill from
https://github.com/theAnirudhKumar/work-design: copy its
skills/<skill-name> folder into ~/.claude/skills/ (or .claude/skills/
for one project only), keeping the folder name, and tell me the path
it landed in.
```

Or copy the folder by hand to `~/.claude/skills/<skill-name>/`, or `.claude/skills/<skill-name>/` inside one repo. It loads on the next session.

### Claude.ai

Zip a skill's folder, then go to **Customize > Skills**, click **+**, choose **Create skill** and then **Upload a skill**. The folder name inside the ZIP must match the skill's `name` in its frontmatter, or the upload is rejected. See [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

### Claude API

Follow the [Skills quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill).

## Elsewhere

- **Meetings.** [`meeting-or-message`](skills/meeting-or-message) decides whether something should be a meeting. [`meeting-design`](https://github.com/theAnirudhKumar/meeting-design) takes over from there: `meeting-design` before a meeting, `meeting-close` after it, `meeting-audit` for recurring ones. The last two arrive with its v2.0.0 release. Install:

  ```
  /plugin marketplace add theAnirudhKumar/meeting-design
  /plugin install meeting-design@meeting-design-marketplace
  ```

- **Customer success.** `call-recap-follow-up` and `email-critic` used to live here. They are maintained at [CSPulse/customer-success-skills](https://github.com/CSPulse/customer-success-skills), alongside thirty others for reading an account, running the set-piece moments and handling the conversations.

## Writing your own

[`template/SKILL.md`](template/SKILL.md) is a starting structure, and [CONTRIBUTING.md](CONTRIBUTING.md) has the standard this repository holds itself to. Two things matter more than the rest:

The description is the trigger. Claude decides whether to run a skill by reading its description, so list the actual phrases someone says when they want it. A description explaining what a skill *is* rather than when it *fires* produces a skill that never runs.

Write instructions, not documentation. "Read the transcript in full" works. "This skill reads transcripts" does not.

Anthropic's [Agent Skills spec](https://github.com/anthropics/skills/tree/main/spec) is the reference for the format itself. Before opening a pull request, run `python3 validate-skills.py`; the same script runs on every pull request.

Every skill also carries a file in [`evals/`](evals): the prompts that should make it fire, the near misses that should not, and, where it has been run, what three models did with each. The older skills have recorded results; the newer ones are marked "not yet run" until someone runs them. Routing happens on the description alone, so this is the check that tests the thing most likely to be wrong.

## Research

Work design is a real field with a century of research behind it, defined by [Parker, Morgeson and Johns (2017)](https://espace.curtin.edu.au/bitstream/handle/20.500.11937/69907/70119.pdf?sequence=2) as "the content and organization of one's work tasks, activities, relationships, and responsibilities." Its academic centre is the [Centre for Transformative Work Design](https://www.transformativeworkdesign.com/about-work-design) at Curtin University. Both study jobs and teams; `work-design` asks the same question at the scale of a single piece of work, which is where the name comes from.

The methods behind individual skills are established and named where they are used:

- **Appetite**, a time budget that fixes the time and lets the scope flex, is from Ryan Singer's *Shape Up* (Basecamp). It underlies `fit-to-deadline` and the appetite line on the Work Card
- **The pre-mortem**, imagining the plan has already failed, is Gary Klein's, published in Harvard Business Review in 2007. It underlies `what-could-go-wrong`
- **If-then plans** ("if X by Y, then Z") are Peter Gollwitzer's implementation intentions, 1999. They appear in tripwires, in `get-unstuck` and in `lessons-learned`
- **Polished work that hides thin thinking** is the pattern the January 2026 Harvard Business Review article "Why People Create AI Workslop and How to Stop It" calls workslop. It is the failure `review-my-work` exists to catch

An honest limit: this support comes mostly from practice and from related research on planning and behaviour change. There is little direct evidence that any one of these raises the quality of knowledge work, and this repository does not claim a measured improvement.

## License

[MIT](LICENSE).

---

More at [hustlyst.com](https://hustlyst.com?ref=github) · [anirudhk.com/connect](https://anirudhk.com/connect?ref=github)
