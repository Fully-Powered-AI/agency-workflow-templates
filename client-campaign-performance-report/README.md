# Client campaign performance report

At the reporting cutoff, get a client report from your exports: figures by source, a draft narrative and anomalies. A person approves it.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Client campaign performance report on our website](https://fullypowered.ai/workflows/client-campaign-performance-report/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the invented ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Marketing and advertising · Analytics and reporting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/client-campaign-performance-report/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report)*

## The outcome

The report arrives as a draft on the analyst's desk once the exports are in, not as an evening of copying figures between tabs. Every figure sits under the source that produced it, with the attribution window that source uses. Nothing is blended: the ad platform's conversions and the analytics tool's transactions are printed side by side, and the gap between them is reported as a gap.

Where a day is missing from an export, the report says so and shows the days it has; a goal that the missing day could change is shown as not calculable for the full window, with the figure on the days available and the bound the arithmetic gives. It never turns a missing day into a zero, and never turns a tracking outage into a bad week. Anything that moved by a lot, or looks odd in a single day, is listed with the facts first and any explanation second, marked as a hypothesis with the check that would settle it.

The analyst verifies the calculations. The account lead reads the narrative, changes it and approves it. The client sees nothing until a person sends it.

## Who starts the work, and when

The analyst starts it at the weekly or monthly client-reporting cutoff, once the platform and analytics exports for the period have been pulled. The account lead reviews the narrative and the discussion points before the client call or the send.

## What they supply

- The ad-platform exports for the period, one per platform, by day.
- The analytics export for the same days.
- The previous report, or the previous period's figures, for the comparison.
- The client's goals and budget, and the agency's reporting definitions: which conversions count, the attribution window each source uses, the currency.
- Notes on anything that changed in the period: budget moves, launches, pauses, tracking problems.
- The agency's report format. If none is supplied, the workflow template uses its own built-in format.

## What comes out

One report, in a fixed order: the reporting window and its gaps, the figures by source, progress against the client's goals, where sources differ, anomalies, a draft narrative, discussion points for the call, open questions and a list of calculations for the analyst to check. Differing periods are compared per day with the day counts printed. A section with nothing to report says so in a line rather than disappearing.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), where the account team reports to each client on a fixed rhythm and the analyst is the one who has to trust the figures.
- [Professional services](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), for consultancies and studios that report campaign results to clients as part of a retainer.
- [Ecommerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), where the in-house team reports paid media to the owner or the board from the same kinds of exports.
- [Analytics and reporting](https://fullypowered.ai/functions/analytics-and-reporting/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), which owns the definitions, the calculations and the habit of showing the source.
- [Marketing and content](https://fullypowered.ai/functions/marketing-and-content/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), whose campaigns the report describes.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), when the number of client accounts has outgrown the hours the analyst has each cutoff.

It is a different piece of work from the [creator campaign performance report](https://fullypowered.ai/workflows/creator-campaign-performance-report/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), which ranks influencer partners from a store's own orders. It is not the [weekly owner business brief](https://fullypowered.ai/workflows/weekly-owner-business-brief/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), which covers a whole business, and not [quarterly business review preparation](https://fullypowered.ai/workflows/quarterly-business-review-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report), which looks across a quarter and a relationship.

## What has to change for your company

Put your own report format in place of the default order of sections. Set the attribution window each platform uses and the conversions your agency counts. Choose the anomaly thresholds: how large a movement is worth a line, and how large a one-day spend swing is worth a question. Decide the comparison period for weekly and monthly reports, and the number of decimals your clients are used to. Decide who is allowed to approve a narrative when the account lead is away, and where the approved report is kept.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was run twice on its invented example in Claude on 10 November 2026. The instructions, the output format and the example were revised after the first run, and the second run is the one recorded and published with it. After that run, small wording edits were made following a review, without a new run. It has not yet been tested in a client environment.

Testing in your environment means running it on a past reporting period whose figures your analyst already knows, including a week with a missing day, a week with a tracking outage and a week where the platform and analytics disagree. The analyst recomputes every figure before any report goes further.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Creator campaign performance report](https://fullypowered.ai/workflows/creator-campaign-performance-report/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report)
- [Weekly owner business brief](https://fullypowered.ai/workflows/weekly-owner-business-brief/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report)
- [Quarterly business review preparation](https://fullypowered.ai/workflows/quarterly-business-review-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-client-campaign-performance-report&from=gh-client-campaign-performance-report).
