# Evaluation: chat-context

**Run 2, 29 Aug 2026.** Haiku, Sonnet and Opus, judged on the four descriptions in this repository, shown in full.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 5 | "Wrap this chat, I am moving to a new one." | fire, handoff | fire | fire | fire |
| 6 | "Pick up where we left off on the pricing page work." | fire, resume | fire | fire | fire |
| 7 | "Can you summarise what we talked about today so I can read it back?" | none | none | none | none |
| 16 | "This chat has got huge and it is costing me a fortune. What do I do?" | conflict with `optimize-tokens` | optimize-tokens | optimize-tokens | optimize-tokens |

Both modes fire. The exclusion holds. One finding on case 16.

---

## Case 7, the exclusion that matters most

"Summarise what we talked about" is the single most likely false positive for this skill, because it is superficially the same request and the skill's own rules say it is a different ask. All three models declined it. The sentence "do not use it when the user wants a summary to read rather than a handoff to reuse" is what produced that, and it should survive any future trim.

## Case 16, the gap

"This chat has got huge and it is costing me a fortune" went to `optimize-tokens` on all three models, unanimously and with no hesitation.

That is defensible, and it is also arguably the wrong skill. The actual remedy for a chat that has grown expensive is to close it and open a fresh one carrying a handoff, which is exactly what this skill does. `optimize-tokens` will produce a leaner prompt inside a context that is already the problem.

**Recorded as a gap, not fixed here.** The fix would be a clause in this skill's description about a chat that has become long or expensive, and that is a description change to a shipped skill, which needs its own issue. Two reasons to think before making it:

1. It would put this skill into direct competition with `optimize-tokens` on every cost-shaped message, and `optimize-tokens` is right for most of them.
2. The two are complementary in this case rather than exclusive. The best session opens with a handoff and then prompts the new chat leanly.

The honest version of the finding: a user who describes their problem in terms of cost will not reach this skill, and the skill that they do reach cannot solve the cost problem at its root.

---

## Not tested

- Whether handoff correctly detects that no file access exists and prints the block in chat instead. That is an output check.
- Whether resume states what was loaded before doing any work, which is the rule most likely to be skipped under load.
- The two-Active-rows case, where the skill is supposed to ask rather than guess.
