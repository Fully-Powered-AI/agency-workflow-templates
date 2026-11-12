# Campaign claim evidence register

An account lead gets a register that pairs each draft campaign claim with the evidence the client supplied, its source date, proposed qualified wording and the approvals still missing. Unsupported or stale claims are blocked; only approved wording is released.

*Workflow template · Marketing and advertising · Marketing and content · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/campaign-claim-evidence-register/)*

## The outcome

A campaign is ready to brief and someone has written the lines everyone likes: a comparison with a rival, a result, an offer. The account lead needs to know which of them can go out, and on what words. The register answers that claim by claim, in one fixed layout. Each draft claim sits beside the evidence the client supplied for it, when that evidence is dated, what it actually covers, wording that stays inside it, and which approvals have not yet been recorded.

Every claim ends in one of three states. Ready for release means the evidence is current, permission is stated and the right people have approved the exact wording. Pending approval means the evidence holds but approvals are missing. Blocked means there is no evidence, no date, evidence that is too old, no stated permission, or nothing in the evidence that supports the line. Only wording on the release list goes out, and the account lead is the one who releases it.

The workflow template treats everything the client hands over as an assertion the client has made. It does not confirm it, and it makes no legal or advertising-regulation judgment: that stays with the client's claims owner and the specialist who signs off the kind of claim.

## Who starts the work, and when

The account lead starts it when a proposed campaign contains a comparison, a result or an offer, before copy goes to production or media. The client's claims owner and the relevant specialist read the register and approve wording. The account lead releases the approved lines to the team and records the register again whenever the evidence or wording changes.

## What they supply

- The draft claims, each with an identifier, the line as written, its type (comparison, result or offer) and where it will appear.
- The client's evidence for each claim: a log of what was supplied, who supplied it, its source date, what it covers and whether it may be used, plus the evidence itself.
- The offer terms and any standing disclosure text that appears with a claim.
- The approvals recorded so far: who approved which wording, and when.
- The campaign launch date, the date copy is due, and the client's approval procedure: who approves each type of claim.

## What comes out

One register in a fixed order: a count of claims by status, then one entry per claim showing the draft line, the evidence, its age against the limit, permission, proposed wording, approvals still missing and the reason for the status. After the entries come the release list, what would unblock each blocked claim, any evidence that matched no claim, and questions for the account lead. Where a section is empty it says "None."

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Marketing and content](https://fullypowered.ai/functions/marketing-and-content/), where campaign copy is written and passed on.
- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), whose reviewers decide what the claim may say; the register only prepares their paperwork.
- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/), where the account lead carries the client's claims into production.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), where offers, rankings and comparisons are the usual copy.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where promotions and price comparisons change often.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when campaigns multiply faster than anyone can keep track of what each line rests on.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), when old claims keep being reused after their evidence has aged.

It is separate from [creator content approval](https://fullypowered.ai/workflows/creator-content-approval/), which reviews a creator's finished post. It does not test whether a difference in numbers is real, which is [comparison claim check](https://fullypowered.ai/workflows/comparison-claim-check/), and it does not edit copy, which is [copy edit with a change list](https://fullypowered.ai/workflows/copy-edit-with-a-change-list/).

## What has to change for your company

Write down who approves each type of claim and keep that list with the client. Set how old evidence may be for comparisons and for results; the template starts at six and twelve months. Decide what the client must say when granting permission to use evidence. Agree the exact status words your account teams use. Fix who may release approved copy and to whom, and where the register is stored so that one version is current.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026, and the record of that run is published with it. It has not yet been tested in a client environment.

Testing in your environment means running it on a past campaign whose claims are already known: one with stale evidence, one with a missing date, one where the approver signed different wording than the one proposed. The account lead and the client's claims owner should recompute every date and age before the register is relied on.

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

- [Comparison claim check](https://fullypowered.ai/workflow templates/comparison-claim-check/)
- [Creator content approval](https://fullypowered.ai/workflow templates/creator-content-approval/)
- [Copy edit with a change list](https://fullypowered.ai/workflow templates/copy-edit-with-a-change-list/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
