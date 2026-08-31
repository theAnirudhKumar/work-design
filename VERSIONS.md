# Versions

What changed, and when.

## 3.0.0

**Added three skills to Tool lifecycle and Working with agents.** `delegate` (#3), splitting a single piece of work into an allocation table across you, another person or a model, each part carrying a check and a stop condition. `stack-audit` (#13), auditing tools already paid for into a keep, cancel, downgrade or consolidate verdict. `switch-cost` (#19), checking what breaks on the way out of a tool already in use, closing the Tool lifecycle category as scoped.

**Opened a third category, Deciding how work runs.** `pick-the-medium` (#21) picks the channel for one piece of communication before it happens and hands off to a meeting-design skill the moment a meeting is the answer; its boundary against `meeting-design` was resolved by reading that skill's actual shipped description in the sibling `theAnirudhKumar/meeting-design` repository rather than assuming one. `scope-the-work` (#23) draws the in/out/done boundary of a piece of work before it starts. `estimate-from-precedent` (#25) corrects a time estimate against a reference class of ordinary past cases, built on the planning fallacy (Buehler, Griffin & Ross, 1994) and reference class forecasting (Flyvbjerg, 2006), and closes the duration-estimate gap `scope-the-work`'s own eval named.

**Added the evaluations harness and backfilled it across every skill.** `evals/README.md` plus one file per skill, each run against Haiku, Sonnet and Opus with results recorded honestly, including disagreements (#5). Every skill added since carries its own eval from the day it shipped.

**Fixed two routing bugs.** `optimize-tokens`'s proactive trigger fired inconsistently across models; rewritten to name request shapes instead of asking the model for a judgement call. A cost-shaped complaint was falling through every skill instead of reaching `chat-context` (#11).

**Rewrote the README.** Replaced the three-paragraph, citation-heavy opening with plain what/why/how text, moved the academic citation into its own Research section at the bottom (#15). Regrouped the flat skills table into the three category tables that now structure the whole document (#17), and kept them in sync as each new skill shipped.

## 2.0.0

**Renamed from `skills` to `work-design`.** The old name said nothing about what was inside, and what was inside was two unrelated groups of skills. GitHub keeps a permanent redirect, so the old repository URL still resolves.

The marketplace is now `work-design-marketplace` and the plugin is `work-design`, replacing `cowork-skills` and `workflow-skills`. Reinstall with the strings in the README.

**Added `before-you-install`,** moved from the `tool-decisions` repository, which has been retired into this one. Vets a tool before signup across five checks and ends on install, install with conditions, or do not install.

**Removed `call-recap-follow-up` and `email-critic`.** Both are maintained in `CSPulse/customer-success-skills`, which is where anyone looking for customer-facing skills should land. Two copies of a skill drift; one does not.

**Added the contribution surface.** `validate-skills.py`, a GitHub Actions workflow running it on every pull request, `CONTRIBUTING.md`, issue and pull request templates, and a gitignore. The structural rules were previously enforced only by a local hook, so anyone arriving by fork had nothing to run.

**Fixed.** The H1 in `chat-context` did not match its folder. The description on `call-recap-follow-up` was 1,096 characters against the 1,024 limit, putting its trigger phrases in the range assistants truncate; that skill has moved, and the copy in the customer success library is the one to fix.

## 1.0.0

First release, as `skills`. Four skills: `call-recap-follow-up`, `chat-context`, `email-critic`, `optimize-tokens`.
