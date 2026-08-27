# What to look for

The five checks in detail. Read this when running the vetting, and use the search strings verbatim in guided mode.

## 1. Privacy and data

The question is not "do they respect privacy". It is **what does this document permit them to do, whether or not they currently do it.** Policies are written to allow more than the company practises today, and today is not the only day the tool will exist.

Find and quote:

- **Content licence.** Look for "licence to use, host, reproduce, modify, publish" applied to what you upload. Broad is normal for a service that has to display your files back to you. Broad plus "improve our services" or "train our models" is a different clause and worth quoting exactly.
- **Training.** Is content used to train models, is it opt-out or opt-in, and does the setting cover past data as well as future.
- **Retention after deletion.** "Deleted immediately" and "removed from active systems within 30 days, backups within 12 months" are both common and very different.
- **Sub-processors.** Which other companies receive the content. Often a separate page.
- **What "local" or "private" mode covers.** Frequently the content stays local and the metadata does not, or the main path is local and one specific feature is not. Find the exception, because the exception is the story.
- **Jurisdiction.** Where the data sits and whose law applies.

Ask in guided mode: *paste the Privacy Policy and the Terms of Service, or the URLs. If they are long, the sections on content ownership, data retention, and third parties are the ones that matter.*

## 2. Business model

Free is paid for by someone. Usually a paid tier, sometimes investors buying growth, occasionally the data.

- **How it makes money today**, in one sentence.
- **Acquisition.** Search `<tool> acquired` and `<tool> acquisition`. An acquisition is not bad news in itself. Terms rewritten quietly after one is.
- **Price drift.** Compare the vendor's current pricing page against what reviews from six or twelve months ago say. Where they disagree, the vendor's page wins and the disagreement is itself worth reporting.
- **Free tier caps.** Often absent from the pricing page and present in the docs or a support article.
- **Funding stage.** A tool burning investor money at a low price will reprice eventually. Say so without pretending to know when.

## 3. Permissions and footprint

- **Every permission requested, matched to a feature.** Screen recording, accessibility access, microphone, camera, clipboard, full disk, contacts, calendar. Accessibility access on macOS and Windows is broad: it can generally read and control other applications.
- **A permission with no visible feature behind it** is the single most useful thing this check produces. Report it as an open question rather than an accusation.
- **Background and startup behaviour.**
- **Browser extensions.** An extension that can "read and change all your data on all websites" deserves its own line, whatever the app does.
- **Platform reality.** Check the vendor's site today rather than a review. Listings go stale in both directions.

## 4. The public record

Run all of these. They surface different things.

```
<tool> reddit
<tool> hacker news
<tool> controversy
<tool> complaints
<tool> privacy concern
<tool> data collection
<tool> cancel subscription
<tool> refund
<tool> alternative
<tool> vs <the obvious competitor>
```

Reading rules:

- **Volume and repetition over intensity.** Twenty calm people describing the same billing problem beats one furious review.
- **Age matters.** A complaint from two years ago may describe something fixed. Check whether anyone says it was.
- **The company's response is evidence.** How a team answers public criticism tells you what dealing with them will be like.
- **`<tool> alternative` is underrated.** It shows you who leavers left for, and why.
- **Trial-versus-paid patterns.** A repeated claim that quality drops after payment is worth taking seriously if several people say it independently.
- **The vendor's own comparison posts are marketing.** Where a tool's blog ranks the best tools in its category and itself first, treat the ranking as a claim and the competitor descriptions as possibly still useful.

## 5. Buried value

Look for what is real, useful, and not on the landing page: features in the docs but not the marketing, integrations not led with, settings that materially change how good the tool is, workflows the community found that the vendor never wrote up.

This check exists for two reasons. It is often the most useful part of the output. And a process that only produces problems trains the reader to discount it, which means the day it says stop, nobody stops.
