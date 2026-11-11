# Trial of "Campaign claim evidence register" on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

This was a second run of the template on its own invented example, made after a first run and an independent review led to changes in the template and the example. The agency, client, campaign, claims, evidence and figures are made up; no client data was used. Unlike the first run, this one was not independent: the assistant that revised the template worked through the revised instruction block and output format, step by step, on the revised inputs in `public/example.md`, wrote the register, and only then compared it with the example's published output. It is a check of the revision, not a fresh test by a stranger. The first run's record is replaced by this one; its findings are summarised under "What the first run found".

## What came out

Six claims, seven evidence rows and four approvals on file. Ready for release 1 (C3), Pending approval 3 (C2, C4, C6), Blocked 2 (C1, C5). E7 named C7, which is not among the claims, and was listed as not matched. The statuses matched the published example, and so did the wording of every claim.

- **C1, Blocked.** The survey is dated 2025-01-20, 22 complete months before the 30 November 2026 launch against a limit of 12: stale. Wording marked "Not for use until unblocked": "In a January 2025 survey, 212 customers of three months or more reported an average 30% reduction in their weekly food spend." Both approvals missing, none on file.
- **C2, Pending approval.** Dated 2026-09-14, 2 months, current. Wording narrowed to Supermarket Kit B and to the four of five recipes where our box was cheaper, with the count worked out in the Reason (R4 dearer, $12.50 against $12.00) and the stated totals given there. The claims owner's 2026-11-11 approval is on the draft line, so it is listed as different wording; the pricing lead's approval is missing.
- **C3, Ready for release.** Dated 2026-11-02, 0 months. Wording "Over 50,000 households have had a box delivered." Both approvals are on exactly that wording. Its date is in the evidence line, not the wording, under the rule that wording already inside the evidence and already approved is kept unchanged.
- **C4, Pending approval.** Terms dated 2026-11-02 cover the whole offer period. Wording: "Free standard delivery on your first box with a box value of $45 or more. New customers only, delivery zones 1 to 3, 30 November to 14 December 2026, not combined with other offers." The claims owner's approval of 2026-11-13 is on this exact wording and counts; the commercial lead's is missing. The footer "Terms apply." carries none of the conditions; raised as question 1.
- **C5, Blocked.** The image was treated as supplied but supporting no wording; no source date, permission not stated. Wording: "None:" with the reason. Both approvals missing.
- **C6, Pending approval.** Dated 2026-10-05, 1 month. Two of the 14 recipes took 25 minutes, so the claim was narrowed to 12 of 14, which keeps it Pending. Both approvals missing.

Release list: C3 only. To unblock: C1 needs a measurement within the 12-month limit or the client's decision to drop the claim; C5 needs the badge's issuer, date and method and the client's statement that it may be used. Three questions: whether the placements can carry the full C4 conditions; whether the claims owner will approve the narrower C2 wording; and whether E7 belongs to a claim missing from the list. The closing lines were printed.

## What was observed

- **Every required part was produced,** in the order of the claims file, with all headings printed and "None." where a section was empty. Nothing required stopping: the headers matched, the claim types were valid, claim identifiers were unique and the launch date was present.
- **The C4 wording follows the offer terms.** "Standard" and "box value" are kept as the terms state them, and "spend" does not appear. Following the qualifier rule produced the wording that the claims owner had approved, so C4 is Pending for one missing approval only.
- **Reasons ran past one sentence** in C2 and C4; the format now allows one to three short sentences.
- **Run on the example only.** The other acceptance tests were not run. Test 12, on keeping a qualifier, was added after this run and is not part of it.
- **Anything in the output that is not in the inputs.** "Box" in "have had a box delivered" is inferred from "delivered order", as the approved wording does. "Four of five" is a count worked out from the table, which the revised rule allows when the working is shown. No other names, figures or dates were found that are absent from the inputs.
- **Limits of this run.** It did not exercise the month-end rule, a second approved wording for one claim, an approval from a role that is not required, or a missing specialist; those rules are written but untried. Because the run was by the reviser, it may share the reviser's blind spots.

## What the first run found

The first run, by an assistant that did not write the template, found these points, each of which led to a change in the template or the example. The example's C4 wording dropped "standard" and changed "box value" to "spend"; the example's questions included one that was a task, not a question; the rules on basis and identical approvals pulled against each other; the template did not say whether a worked-out count was allowed; the one-sentence Reason was too short; "complete calendar months" was undefined at month-ends; there was no rule for two approved wordings or an approval from a role not required; it was unclear whether a claim narrowed after contradicting evidence was Pending or Blocked, and whether an image naming no issuer counted as content supplied; and the example's settings gave a "today" date the template never used.
