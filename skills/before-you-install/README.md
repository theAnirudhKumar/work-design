# before you install

**Part of [work-design](../../#readme): a set of skills, in three categories, for deciding how a piece of work will run before it starts.**

Every tool's landing page is written by the people selling it - the things that would actually change your mind live somewhere else: a buried clause in the terms, an eight-month-old complaint thread, a permission the installer asks for and never explains. This skill goes and finds those. It reads the privacy policy and terms for what they actually permit (training on your content, retention after deletion, sub-processors), checks the business model and the permissions the app actually requests, and surfaces documented complaints from places the company can't edit. It runs in one of two named modes - researched, when it can search and cite directly, or guided, when it hands you the exact searches and clauses to check and works from what you bring back - and always states which one it ran. It closes on exactly one of three calls: install, install with conditions, or do not install, where a condition has to be a named action ("export monthly, keep client work out of it") and never an attitude ("be careful with sensitive data").

The failure this exists to prevent: **finding out what you agreed to only after your data is already inside the tool.**

Part of the **Tool lifecycle** group in this repository.

## Who this is for

For anyone deciding whether to bring a tool in, keep paying for one, or leave it, without redoing the research from scratch every time.

## What this needs

Works with nothing but the tool's name. Gets better with the pricing page, policy or terms pasted in, and web access, which lets it do the research instead of handing you the searches.

Missing context never blocks this skill. It changes what the skill can honestly claim, and it says which checks it could not run rather than guessing around the gap.

## Install just this skill

**In the Claude app, no terminal needed.** Paste this into Claude:

```
Download the before-you-install skill from
https://github.com/theAnirudhKumar/work-design/tree/main/skills/before-you-install,
zip the before-you-install folder on its own, then upload it as a skill in Claude.
```

Or do it by hand: download this repository as a ZIP (or clone it), zip this folder (`skills/before-you-install`) on its own, then in Claude go to **Customize > Skills > Create skill > Upload a skill**. The folder name inside the ZIP has to match the `name` in `SKILL.md`.

## Want the whole set?

The [main README's Install section](../../#install) has the one-line plugin command that installs the whole set at once, plus the API and by-hand routes.

---

MIT licensed. Part of [work-design](https://github.com/theAnirudhKumar/work-design).
