# Creative test evidence review

When a batch of ad creative is ready for review, the creative strategist and media lead get an evidence table by creative, angle, format and hook, with tentative learning and next-test options. No winner or loser is named, and thin evidence is held back.

*Capability template · Marketing and advertising · Advertising and lead generation · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/creative-test-evidence-review/)*

## The outcome

The creative review stops being a debate over whichever chart was on screen. The strategist and the media lead sit down with one page that lists every creative in the batch by its ID, angle, format and hook, with its spend, impressions, clicks, conversions and cost per conversion. Beside the table sit the conversion definitions in use and the campaign change log, so everyone can see what each number means and what changed while the batch ran.

Each creative is marked readable or held back, and every held-back creative says why: too few conversions or impressions, an offer that differed from the rest of the batch, an edit to the creative itself, or conversions nobody has confirmed. Only readable creatives feed the roll-ups by angle, format and hook and the tentative learning. The page ends with several next-test options and the questions that could change the reading. The strategist and media lead choose what to test next.

## Who starts the work, and when

A creative strategist or a media analyst starts it when a batch of creative has finished its run and the team has set a time to talk about what to make and test next. The creative strategist and media lead read it before the meeting.

## What they supply

- An export with one row per creative: ID, angle, format, hook, conversion event, run dates, spend, impressions, clicks and conversions.
- The conversion definitions: what each event counts, its window, and whether it has been confirmed against a second record.
- The campaign change log for the period: offers, prices, landing pages, audiences, budgets, tracking and edits to the creative itself.
- Optionally, your own minimums for impressions and conversions, and the size of gap worth discussing.

## What comes out

One page in a fixed order: the conversion definitions and change log used, the evidence table, what is held back and why, roll-ups by angle, format and hook for the readable creatives, tentative learning, two to four next-test options, and questions for the strategist and media lead. Where a section is empty it says so. The page names no winner and no loser, and it changes nothing in any ad account.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Advertising and lead generation](https://fullypowered.ai/functions/advertising-and-lead-generation/), where creative is tested against live spend and the next round has to be chosen.
- [Marketing and content](https://fullypowered.ai/functions/marketing-and-content/), where the team that makes the creative needs to know what the numbers can and cannot say.
- [Analytics and reporting](https://fullypowered.ai/functions/analytics-and-reporting/), for keeping conversion definitions and the change log beside the results.
- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/), where an agency reviews creative on behalf of several clients.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where product, offer and price change often during a test.
- [Software and technology](https://fullypowered.ai/industries/software-technology/), where sign-up and trial conversions are hard to confirm.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when many creatives are launched quickly and each batch needs an honest reading.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), when an in-house team inherits a long history of creative with no shared way to review it.

It does not test whether one result beats another by more than chance (see [comparison claim check](https://fullypowered.ai/capabilities/comparison-claim-check/)), and it does not report on creators ([creator campaign performance report](https://fullypowered.ai/capabilities/creator-campaign-performance-report/)).

## What has to change for your company

Set your own minimum conversions and impressions before a creative can be read, and the size of gap that is worth discussing. Decide which conversion events your team treats as confirmed and what they are checked against. Agree the list of angles, formats and hooks, so the same creative is tagged the same way every time. Decide what goes in the change log and who keeps it. Name the people who must read the page before a learning is repeated to a client.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026, and the record is published with it. It has not yet been tested in a client environment, and it has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past batch whose story you already know: one with a thin creative, one that ran under a different offer, and one with conversions that were never confirmed. The media lead should recompute every figure in the table from the export before the page is relied on.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Comparison claim check](https://fullypowered.ai/capabilities/comparison-claim-check/)
- [Creator campaign performance report](https://fullypowered.ai/capabilities/creator-campaign-performance-report/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
