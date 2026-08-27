# Worked example: a stop

A real vetting that ended in do not install. The tool is described rather than named. A dated review names its subject because the reader can check whether it still holds; a permanent reference file cannot make that promise, and a stop that ages badly is unfair to a product that fixed the problem.

**The tool.** A macOS app plus browser extension that rotates the passwords in your password manager for you. AI agents log into each site and change the credential. Genuinely clever, and the underlying idea is good.

**The use.** Personal credentials, including banking and work logins.

---

## What the five checks found

**Scale.** The browser extension listed ten users. Not ten thousand. The public launch finished twentieth for the day. Small is not disqualifying and small products are often the best ones, but this is the category where "almost nobody has stress-tested this" is a material fact, and it appeared nowhere in the marketing.

**Permissions and design.** Step two of setup is exporting the entire password vault to CSV. That is how the credentials get in. A password manager CSV is a plain text file, and for as long as it sits on disk every credential in it is readable by anything that can open a text file. A backup tool or a sync folder will copy it somewhere the user was not thinking about. This is not a flaw in the app. It is baked into how it has to work.

**Claims versus verification.** The maker states that passwords never leave the machine, that the agents never see the username or password, and that a dedicated agent defends against prompt injection, where a malicious page hides instructions that hijack the agent reading it. Those are the right three things to build, and the architecture behind them is more considered than most tools in this space. No independent audit of any of the three could be found. A major password manager published its own advisory on AI-assisted browsing risk in the same year, so this is a live industry problem rather than an invented one.

**Business model.** The site says free. Third-party reviews reported a monthly change cap with one paid tier, and elsewhere a different price entirely. None of it could be confirmed against the vendor's own pricing page.

**Buried value.** Real, and worth saying. The architecture keeps credentials out of the model and gives navigation only to the agent, which is a smart split. The published roadmap goes considerably further than the shipped product.

---

## The call

**Do not install**, for this use.

The deciding finding is the CSV export, not the user count and not the missing audit. Those two are reasons to wait. The export is a step the user must take before any of the safety architecture applies, and no setting removes it.

Note what the verdict does not say. It does not say the product is bad, the team is careless, or the claims are false. It says the design requires putting every credential you own into a plain text file, and that the checks stop there.

---

## Why this example is in the repo

Three things it demonstrates that a passing verdict cannot.

**A vetting process that cannot say no is decoration.** If every run ends in install with conditions, the process is a formality and the reader learns to skip it.

**The deciding finding is usually not the loudest one.** Ten users is the surprising number and the one that would lead a headline. It is not what decides the call.

**The stop is scoped to a use.** Different use, different answer. Someone evaluating the architecture, or rotating throwaway logins, could reasonably reach a different conclusion from the same findings, and the write-up should let them.
