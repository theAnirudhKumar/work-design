# Evaluation: before-you-install

**Run 2, 29 Aug 2026.** Haiku, Sonnet and Opus, judged on the four descriptions in this repository, shown in full.

---

## Results

| # | Message | Expected | Haiku | Sonnet | Opus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | "Is that meeting transcription app safe to use on client calls?" | fire | fire | fire | fire |
| 2 | "A mate recommended a free invoicing tool. What is the catch with it?" | fire | fire | fire | fire |
| 3 | "I installed a clipboard manager last month. What did I actually agree to?" | fire | fire | fire | fire |
| 4 | "We are evaluating a document platform for the whole company, six figures, and procurement needs a recommendation from me." | none | none | none | none |
| 15 | "Should I pay for a tool that would do this whole task for me automatically?" | conflict with `delegate` | before-you-install | before-you-install | before-you-install |

Clean pass. Three fires, one correct decline, one conflict that turned out not to be one.

---

## Case 3, the after-the-fact trigger

"What did I actually agree to" is the only case in the set where the tool is already installed, and the description carries a clause for it. All three models found it. Worth keeping in mind when trimming the description for length: that clause is doing work.

## Case 4, the procurement exclusion

The six-figure company purchase with a buying committee is the exclusion the description names. All three declined it, at high confidence on Haiku and Opus. The deferral clause works.

## Case 15, a conflict that is not one

"Should I pay for a tool that would do this whole task for me automatically" was written as a genuine contest with `delegate`, since it contains both a purchase decision and a delegation decision. All three models picked `before-you-install` without hesitation. The money appears to dominate.

That is the right answer, and it is worth stating why rather than just recording it: the purchase is the irreversible half. A bad allocation can be redone next week. A subscription with the user's client data in it cannot.

---

## Not tested

- The researched versus guided mode split. That is behaviour after the skill fires, and it needs an output check rather than a routing case.
- Whether the five checks actually run in order.
- Any case where the user pastes a policy or a pricing page, since these cases are all short messages.

---

## Note, 29 Aug 2026, stack-audit added

Rechecked with `stack-audit` added to the set, since a new skill's arrival is a listed rerun trigger and the two skills sit either side of the same line: adopted or not. Case 3 (post-install, "what did I actually agree to") and case 4 (six-figure procurement) both held on all three models. Full detail in `evals/stack-audit.md`, which treats these as its own regression check.
