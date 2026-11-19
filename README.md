# AI workflow templates for marketing and advertising agencies

FullyPowered Workflow Templates for marketing and advertising agencies turn the AI your agency already pays for into a team that knows how the work is done: an account lead with each campaign claim matched to its client evidence, an analyst with the client campaign performance report drafted from the exports, a media lead with an inherited campaign audited against the client's plan. 6 workflow templates, made to be customized and deployed. All plain Markdown, all free, MIT license.

We are FullyPowered AI. We build AI workflows for companies, and these are the templates we start from. We publish them because a good starting point should be open to everyone. Copy one. Change it. Make it yours.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** These are templates, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See more examples for marketing and advertising agencies](https://fullypowered.ai/industries/marketing-and-advertising/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme) · [Have one built for your team](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Who this is for**

- Agency owners and managing partners who have paid for AI and want it doing real client work.
- Account, strategy and delivery leads who want a workflow their team can run this week.
- The analyst or account director who does the work, gets a precise draft and still makes the call.

**What these are for**

- **Your best way of doing it, for the whole team.** One piece of work, written down precisely enough that an assistant prepares it the same way every time.
- **Work you can check.** Every template says what it needs, what it produces, what it checked and what it could not.
- **A person decides.** Anything that sends, posts, pays or changes a record waits for someone to approve it.
- **Tied into your business systems.** A workflow can be designed to pull from the systems your company already runs, and even push data back into them, with guardrails and a person approving. [Browse the Connectors Directory](https://fullypowered.ai/connectors/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme).
- **Free, open and portable.** MIT-licensed plain instructions that run in the assistant or agent your team already uses: ChatGPT, Claude, Claude Code, Claude Cowork, Codex, Copilot, Gemini, Grok, Perplexity.

**Quick start**

1. **Draft this week's client report from your own exports.** Open ChatGPT, Claude, Copilot or Gemini. Copy the text below into a new chat and fill in the square brackets. Then attach or paste your exports for the week. You will get a draft report back in a few minutes.

   ```text
   You prepare a client performance report for an analyst and an account
   lead. You prepare; people decide. You never send anything or change any
   account. Client: [client name]. Reporting window: [dates]. Previous
   period: [dates or last report]. I will paste or attach: the ad platform
   exports by day, the analytics export by day, last period's figures, the
   client's goals and budget, and notes on what changed. Report in this
   order: the days covered and the gaps; the figures for each source, never
   added together across sources; progress against each goal; where the
   sources disagree; unusual days; a short draft narrative; points to
   discuss; open questions; and every calculation for me to check. A
   missing day is a gap, never a zero. Label every explanation as a
   hypothesis and say how to check it. If anything is missing or unclear,
   ask me. Stop at a draft. A person checks the figures and approves what
   the client sees.
   ```

2. Read what comes back. It marks what it checked and what is left for you. What comes out for an invented week:

   ```text
   CLIENT PERFORMANCE REPORT: Client A, week of 2 November 2026
   DRAFT. Figures await the analyst's check. The narrative awaits the account lead's approval. Nothing has been sent.

   For: the analyst and the account lead. Prepared 9 November 2026, from the Platform A export (6 rows), the Platform B export (7 rows), the analytics export (14 rows), last week's report, the definitions, the goals and the media buyer's notes.
   Window: Monday 2 November to Sunday 8 November 2026 (7 days). Compared with: Monday 26 October to Sunday 1 November 2026 (7 days), from last week's report.
   Definitions: Platform A 30-day click. Platform B 7-day click, 1-day view. Analytics last non-direct click. USD. Ratios are built from summed figures. Changes are per-day averages over the days with data.

   REPORTING WINDOW AND GAPS
   Platform A: 6 of 7 days. Not available: Sunday 8 November (the saved date range ended 7 November, per the media buyer). Shown as a gap, not zero.
   Platform B: spend and clicks 7 of 7 days; conversions and conversion value 5 of 7 days. Not recorded: Wednesday 4 and Thursday 5 November (tracking down, per the media buyer). Shown as not recorded, not zero.
   Analytics: 7 of 7 days for both sources.
   Previous period: totals only, from last week's report; daily gaps in that week cannot be checked.
   ```

3. Stop there. You will know if this is for you. When you want it fitted to your company, or built into your agents, [that is what we do](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme).

In every workflow a person starts the work, supplies the inputs and decides; the template prepares and checks, and nothing is sent to a client until a person approves it.

These are samples and a starting point, made to be changed to fit your agency's formats, rules and clients. They do not cover everything an agency does, and your work may not appear here. Any workflow can be built for your company, as one step or as many.

## The workflow templates here today

- **[Campaign claim evidence register](campaign-claim-evidence-register/)**: An account lead gets a register that pairs each draft campaign claim with the evidence the client supplied, its source date, proposed qualified wording and the approvals still missing. Unsupported or stale claims are blocked; only approved wording is released.
- **[Client campaign performance report](client-campaign-performance-report/)**: At the weekly or monthly reporting cutoff, the analyst gets a client report in the agency's format from the exports supplied: source figures, a drafted narrative, anomalies and discussion points. Gaps stay gaps, and every explanation is labelled a hypothesis.
- **[Creative test evidence review](creative-test-evidence-review/)**: When a batch of ad creative is ready for review, the creative strategist and media lead get an evidence table by creative, angle, format and hook, with tentative learning and next-test options. No winner or loser is named, and thin evidence is held back.
- **[Inherited campaign audit](inherited-campaign-audit/)**: When an agency takes over an account or prepares a campaign health review, the media or analytics lead gets an inventory of what is running against the client's plan: mismatched offers, disagreeing destination pages, missing measurement evidence, and an owner for each follow-up.
- **[Lead form field review](lead-form-field-review/)**: When a client questions a long inquiry form or abandoned submissions, the conversion lead gets a field-by-field review: what each field is used for downstream, where people leave, and proposed labels, error messages and test questions. The lead and the client's data owner decide every change.
- **[Missed milestone client reply](missed-milestone-client-reply/)**: When a client challenges a delay, a deliverable or an earlier commitment, the account director gets a draft reply and an internal action note that keep confirmed facts apart from proposed recovery steps and the decisions still needed. Nothing is sent.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

To take the whole collection, press **Use this template** at the top of this page: it copies every folder into a repository in your own account, yours to change.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The workflow template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More workflow templates

The [FullyPowered Workflows Directory](https://fullypowered.ai/workflows/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme) lists every workflow template across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

For the work these templates come from, by area of the business and by task, see [AI workflow examples for marketing and advertising agencies](https://fullypowered.ai/industries/marketing-and-advertising/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the workflow template drew on. Published by [FullyPowered AI](https://fullypowered.ai/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=agency-readme&from=gh-agency-readme).
