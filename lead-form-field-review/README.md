# Lead form field review

When a client questions a long inquiry form or abandoned submissions, the conversion lead gets a field-by-field review: what each field is used for downstream, where people leave, and proposed labels, error messages and test questions. The lead and the client's data owner decide every change.

*Workflow template · Marketing and advertising · Design and user experience · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/lead-form-field-review/)*

## The outcome

The argument about the form stops being about opinion. Every field the form asks for is set beside the use someone made of the answer after submission, and beside the number of people who reached it and the number who left there. Where nobody can say what a field is for, the review says so plainly and hands the question to the person who can answer it.

Each field that needs attention becomes a numbered finding with its facts, a proposed label or error message where the current one does not help, and a test question the team could answer by comparing versions. The review never says a change will raise completions, and it never decides that a field goes.

Fields the client has said are required for consent or for the business are kept. The review may suggest clearer words for them; it does not suggest dropping them.

## Who starts the work, and when

The conversion lead starts it when a client questions a long inquiry form or the share of people who start it and do not finish. The client's data owner supplies what each field is used for and approves any change to a field; the conversion lead decides what goes forward.

Developers change the form only after both have approved. The template edits no form and contacts no one.

## What they supply

- **The form definition:** each field in order, with its label, type, whether it is required, its choices or format rule and the message shown when it is rejected.
- **The completion export** for a stated period, as a file: for each field, how many people reached it, how many filled it, how many times a validation message was shown and how many left at that field. No lead records and no personal details are needed, only counts.
- **Field-use notes** from the client's data owner: what each answer is used for, by which role, at which step of the follow-up, and whether a consent or business requirement makes it required.
- **The follow-up process,** as numbered steps from the first reply onward.
- **The data requirements** the client has supplied, each with a reference and an owner.
- **A few settings:** the period, the as-of date, the totals for the form, and the flag levels for exits and for validation messages.

No connection to the form tool, the website or the customer records is needed, and no sign-in details are asked for.

## What comes out

One document in a fixed order: the form's totals, a block for every field in the form's order, numbered findings, the fields with no finding, the fields held as required, what could not be assessed, and a closing line on where every figure comes from.

Good looks like this: the client's data owner can read any finding, see which note and which export row it rests on, and know what is being asked of them.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Design and user experience](https://fullypowered.ai/functions/design-and-user-experience/), where a form is judged by whether a stranger can complete it.
- [Advertising and lead generation](https://fullypowered.ai/functions/advertising-and-lead-generation/), where paid traffic ends at a form and every field is paid for in people who leave.
- [Analytics and reporting](https://fullypowered.ai/functions/analytics-and-reporting/), which needs to know what each field feeds after submission.
- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/), the agencies whose clients question the forms they have been given.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where an inquiry form is often the first thing a prospective client meets.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where demo and contact forms ask for more as sales processes grow.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when a form has gained a field for every team that wanted one.

It is not a review of how a website is found ([website findability audit](https://fullypowered.ai/workflows/website-findability-audit/)), and it is not a plan for what to track ([tracking event plan](https://fullypowered.ai/workflows/tracking-event-plan/)).

## What has to change for your company

- **Your export.** Use the column names your form tool gives you, or rename them once to the defaults. When a header does not match, the assistant stops and asks.
- **Your flag levels.** The defaults flag a field when a tenth of those who reach it leave there, or when a validation message is shown there 15 times for every hundred who reach it. Set the levels your team can act on.
- **Your follow-up steps.** Write the steps as your sales or service team really runs them, and say by which step the form must have supplied its data.
- **Your owners.** Decide who holds the data requirements, who approves a field change and who may ask developers to make it.
- **Your platform.** It is written for ChatGPT, Claude, Copilot or Gemini and works from files you supply. Decide which exports the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; that run was not blind to the published output, and a blind run is still to do. The record is published with it. It has not yet been tested in a client environment, or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a form your team already knows well, with cases written in advance: a required field nobody can explain, a field whose choices do not match the quote bands, a field with too few visitors to read, a consent field. Your analytics lead checks every figure against the export before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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
- [Usability test session plan](https://fullypowered.ai/workflow templates/usability-test-session-plan/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
