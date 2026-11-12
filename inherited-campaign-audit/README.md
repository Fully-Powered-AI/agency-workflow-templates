# Inherited campaign audit

When an agency takes over an account or prepares a campaign health review, the media or analytics lead gets an inventory of what is running against the client's plan: mismatched offers, disagreeing destination pages, missing measurement evidence, and an owner for each follow-up.

*Workflow template · Marketing and advertising · Advertising and lead generation · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/inherited-campaign-audit/)*

## The outcome

On the first day with a new account, nobody knows what is actually live. This gives the media and analytics leads one list of every in-scope campaign, set beside the plan the client approved. For each campaign it says whether the offer in its ads is the offer the client approved, whether the ads and the page they land on tell the same story, and whether anyone has evidence that the conversion it is meant to drive was ever recorded.

Each difference becomes a numbered follow-up with a plain question for a named role to answer, and the spend recorded in the period beside it. Nothing is called an error or a waste. A difference between two records is a reason to look, and the leads decide what it means.

Where a record was not supplied, the inventory says "unassessed" and names what is missing. A missing export is never read as a clean result.

## Who starts the work, and when

The media lead or the analytics lead starts it when the agency inherits an account from a client or another agency, or ahead of a periodic campaign health review. The account lead supplies the client's approved plan and agrees any change with the client.

The leads investigate the follow-ups. The template changes no campaign, pauses nothing and contacts no one.

## What they supply

- **The client's approved plan,** one line per campaign group: platform, the text that identifies its campaigns, the approved offer and when it ends, the approved destination and the conversion that matters.
- **Campaign and ad exports** from each platform in scope, as files.
- **Destination-page records:** what a person saw on each landing address, and on what date.
- **Tracking-check results:** who confirmed that a conversion fired, for which campaign, and when.
- **A few settings:** the period, the as-of date, how recent a tracking check must be, and who owns each kind of follow-up.

No connection to any ad account is needed, and no sign-in details are asked for.

## What comes out

One document in a fixed order: the answer, the scope and plan, an inventory with one entry for every in-scope campaign, the numbered findings with their questions and owners, the plan lines that could not be assessed, and the coverage.

Good looks like this: the media lead can open any campaign's entry, see which ad, page and check each statement rests on, and know within a minute whom to ask next.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Advertising and lead generation](https://fullypowered.ai/functions/advertising-and-lead-generation/), where the plan, the ads and the landing pages must agree.
- [Analytics and reporting](https://fullypowered.ai/functions/analytics-and-reporting/), which needs to know where measurement is evidenced and where it is only assumed.
- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/), the agencies that take over accounts and review them on a rhythm.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where promotions change often and ads outlive offers.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), where several agencies and seasonal offers leave accounts out of step with the plan.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when new client accounts arrive faster than anyone can learn each one by hand.

It is not a website findability review, which looks at how a site can be found ([website findability audit](https://fullypowered.ai/workflows/website-findability-audit/)), and it is not a plan for what to track ([tracking event plan](https://fullypowered.ai/workflows/tracking-event-plan/)).

## What has to change for your company

- **Your plan format.** The assistant reads the plan's columns by name; map yours to the defaults, or reshape the plan once.
- **Your scope rule.** The default counts a campaign if it is enabled or recorded spend in the period. Change it if your reviews cover something else.
- **Your freshness limit.** Decide how old a tracking check may be before it stops counting as evidence. The default is thirty days.
- **Your owners.** Say which role follows up each kind of finding, and who may agree an account change with the client.
- **Your files.** Use the export column names your platforms give you, if they differ from the defaults. When a header does not match, the assistant stops and asks.
- **Your platform.** It is written for ChatGPT, Claude, Copilot or Gemini and works from files you supply. Decide which exports the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example, in Claude on 10 November 2026, on an earlier wording of the instructions; the record is published with it. The run was not blind, because the published inventory had been read first, and the revised wording has not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on an account your leads already know well, with cases written in advance: an offer that ended last month, a page that returns an error, a campaign that is in no plan line, a tracking check that failed. Your analytics lead checks every statement against the exports before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
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

- [Tracking event plan](https://fullypowered.ai/workflow templates/tracking-event-plan/)
- [Website findability audit](https://fullypowered.ai/workflow templates/website-findability-audit/)
- [Client campaign performance report](../client-campaign-performance-report/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
