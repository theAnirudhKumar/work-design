# Versions

What changed, and when.

## 2.0.0

**Renamed from `skills` to `work-design`.** The old name said nothing about what was inside, and what was inside was two unrelated groups of skills. GitHub keeps a permanent redirect, so the old repository URL still resolves.

The marketplace is now `work-design-marketplace` and the plugin is `work-design`, replacing `cowork-skills` and `workflow-skills`. Reinstall with the strings in the README.

**Added `before-you-install`,** moved from the `tool-decisions` repository, which has been retired into this one. Vets a tool before signup across five checks and ends on install, install with conditions, or do not install.

**Removed `call-recap-follow-up` and `email-critic`.** Both are maintained in `CSPulse/customer-success-skills`, which is where anyone looking for customer-facing skills should land. Two copies of a skill drift; one does not.

**Added the contribution surface.** `validate-skills.py`, a GitHub Actions workflow running it on every pull request, `CONTRIBUTING.md`, issue and pull request templates, and a gitignore. The structural rules were previously enforced only by a local hook, so anyone arriving by fork had nothing to run.

**Fixed.** The H1 in `chat-context` did not match its folder. The description on `call-recap-follow-up` was 1,096 characters against the 1,024 limit, putting its trigger phrases in the range assistants truncate; that skill has moved, and the copy in the customer success library is the one to fix.

## 1.0.0

First release, as `skills`. Four skills: `call-recap-follow-up`, `chat-context`, `email-critic`, `optimize-tokens`.
