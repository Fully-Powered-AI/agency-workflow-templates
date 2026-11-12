# Campaign claim evidence register

Workflow template, version 0.1.0.

## Purpose

Take the draft claims in a proposed campaign, and the evidence the client has supplied for them, and return a register an account lead can act on. Each claim is paired with its evidence, the evidence's source date and scope, proposed qualified wording, and the approvals still missing, and ends in one of three statuses: Ready for release, Pending approval or Blocked. The assistant prepares the register. It treats everything supplied as an assertion by whoever supplied it, never confirms a claim, makes no legal or advertising-regulation judgment, and publishes, sends and approves nothing.

## When to use it and when not to

Use it when a campaign includes a comparison, a result or an offer, before copy goes to production or media, and again whenever evidence, wording or the launch date changes.

Do not use it for the following.

- Judging whether a claim is lawful or meets an advertising rule. Say so and leave it to the client's claims owner and specialist.
- Reviewing a creator's finished post, which is creator content approval.
- Testing whether a difference between two groups of numbers is real, which is comparison claim check.
- Editing copy for style, which is copy edit with a change list.
- Finding evidence, contacting the client or an approver, or checking a source on the web. The register works only from what the account lead supplies.

## Roles

- **Starts it and supplies the inputs, then releases approved copy:** the account lead.
- **Approves wording on every claim:** the client's claims owner.
- **Also approves wording on one type of claim each:** the client's specialist for that type, named in the settings (for example a pricing lead for comparisons, an insights lead for results and a commercial lead for offers).
- **Prepares the register:** the assistant. It decides nothing.

## Inputs

1. **Settings.** Campaign name; launch date (the first day any claim appears); the date copy is due; the offer period if there are offers; the age limit for evidence by claim type; the approvers required on each type. Defaults: comparison 6 months, result 12 months; offers need dated terms covering the whole period the offer runs; the client claims owner approves every claim. If the launch date is missing, stop and ask. If the specialist for a claim type is not named, list "specialist not named" as a missing approval on every claim of that type.
2. **Draft claims.** Default headers `claim_id`, `claim_text`, `claim_type`, `placement`. `claim_type` is one of `comparison`, `result` or `offer`.
3. **Evidence log.** Default headers `evidence_id`, `claim_id`, `description`, `supplied_by`, `source_date` (YYYY-MM-DD, or blank), `scope`, `permission`. `permission` is `own data` (the client's own records), `granted` (the permission of a named other party is on file) or anything else, which counts as not stated.
4. **The evidence itself,** pasted or attached, one item per `evidence_id`: the figures, the offer terms, the survey summary, the document. If only the log row is supplied, the content is not supplied.
5. **Approvals on file.** Default headers `claim_id`, `approver_role`, `approved_wording`, `approval_date`. If there are none, write "approvals on file: none" and carry on.
6. **Existing disclosures (optional):** standing text that appears beside claims, such as a footer.

If a header does not match these, or `claim_type` is anything else, stop and ask which column is which. Do not guess. If a `claim_id` appears twice in the draft claims, stop and ask.

## The procedure

1. **Check the inputs.** Confirm the headers, the claim types and that claim identifiers are unique. Count the claims, evidence rows and approvals.
2. **Match evidence to claims** by `claim_id`. A claim with no evidence row is Blocked: "no evidence supplied". An evidence row naming a `claim_id` that is not among the claims goes under "Evidence not matched" and is not used.
3. **Treat what was supplied as an assertion.** Write each item as "supplied by [who]" and "a supplied assertion, not verified". Never use confirmed, verified, proven or approved of evidence. Never look anything up.
4. **Check the content.** If the evidence content was not supplied, only the log row, the claim is Blocked: "evidence content not supplied", with no proposed wording. An item that is supplied but says nothing usable, such as an image that names no issuer, date or method, counts as supplied; step 7 then decides whether it covers the claim.
5. **Check the date.** Age is the number of complete calendar months from `source_date` to the launch date: the largest whole number n for which `source_date` plus n months falls on or before the launch date. Where the later month has no such day, use that month's last day (31 January plus one month is 28 February). The settings' other dates, such as a "today" date, play no part in the age. A blank date is Blocked: "no source date". An age above the limit for the claim type is Blocked: "stale". For an offer, the dated terms must state a start and an end that cover the whole offer period; otherwise Blocked.
6. **Check the permission.** Only `own data` or `granted` pass. Anything else, blank included, is Blocked: "permission not stated".
7. **Check the scope.** Compare what the claim says with what the evidence covers: who or what was counted, how many, which period, which products or rivals, and whether the figure was reported by people or recorded by a system. Where the claim is wider than the evidence, narrow the wording to the evidence. Where the evidence says nothing about the matter the claim raises, or supports no wording at all, the claim is Blocked: "evidence does not cover the claim". Where the evidence contradicts part of the claim and a narrower line is still supported, narrow it; the claim is then Pending approval, not Blocked, unless another block reason applies.
8. **Propose qualified wording.** Use only facts in the evidence, and keep its qualifiers in its own words: do not drop "standard" from "free standard delivery", and do not swap a term for a looser one ("box value" is not "spend"). Keep every figure as stated; round only downward, as in "over 50,000" for 52,310. A count of items that meet a plain test shown in the evidence (four of five recipes cheaper) is allowed, with the working in the Reason; work out no other figure the evidence does not state (no percentage, average, difference or sum). Give the basis where the wording can carry it: when, how many, who reported or measured, and which rival. Add no superlative or fact the evidence lacks. A narrower line is better than an unsupported one. If an approval is on file for wording that is already inside the evidence, propose that wording unchanged even where it gives less basis, and put the basis in the Evidence and Reason lines; wording wider than the evidence is never kept for the sake of an approval. For a Blocked claim with usable content, show the wording it would carry and mark it "Not for use until unblocked". If nothing can be proposed, write "None:" and the reason.
9. **Check the approvals.** The approvals required are the client claims owner plus the specialist for the claim type. An approval counts only when the `claim_id` and role match and `approved_wording` is identical to the proposed wording. An approval on different wording does not count: list the role as missing and say it approved different wording, with the date. If a role has approved two different wordings of one claim, only an exact match counts and the other is listed as different wording with its date. An approval from a role that is not required for the claim is noted as "not a required role" and does not count. Do not infer an approval from anything but the approvals file.
10. **Set the status.** Blocked if any block reason applies. Otherwise Ready for release if every required approval counts. Otherwise Pending approval.
11. **Note disclosures.** If the proposed wording carries conditions and the standing disclosure text is absent or says less, say so in the reason and raise it as a question. Do not rewrite the disclosure.
12. **Write the release list,** the claims that are Ready for release with their wording, and for each Blocked claim what would unblock it. Never put a Pending or Blocked claim on the release list.
13. **Ask questions,** at most five, each phrased as a question and each one whose answer could change a status or a wording; a reminder or a task for the account lead is not a question. Return the register to the account lead only.

## Exceptions and stop conditions

- **Header mismatch, unknown claim type, repeated claim identifier or no launch date:** stop and ask.
- **Asked to mark a claim approved, ready or verified without a matching approval record:** decline.
- **Asked to judge whether a claim is lawful, complies with an advertising rule or can safely run:** decline; the claims owner and the specialist decide.
- **Asked to strengthen the wording beyond the evidence, drop a qualification or accept an old figure as current:** decline and keep the narrower wording.
- **Asked to contact the client, an approver or the media team, or to send the copy:** decline; the account lead does that.
- **Evidence that contradicts the draft claim:** keep the status the rules give, and say in the reason what the evidence shows.
- **Evidence that was edited after its source date or that you cannot place in time:** treat as no source date.

## Output format

```
CAMPAIGN CLAIM EVIDENCE REGISTER: [campaign]

For: [account lead]. Launch [date]. Copy due [date, or "not supplied"]. Claims [n]; evidence rows [n]; approvals on file [n].

Summary: Ready for release [n]. Pending approval [n]. Blocked [n].

Register:

[claim_id] [Ready for release / Pending approval / Blocked]
Draft claim: "[claim_text]" ([claim_type]; [placement])
Evidence: [evidence_id], [description], supplied by [who]. Scope: [scope from the log, with any conditions stated in the evidence content]. A supplied assertion, not verified.
Source date: [date]; [n] complete months before launch (limit [n], or "terms must cover the offer period"): [current / stale / no date].
Permission: [own data / granted / not stated].
Proposed wording: "[wording]" [or "None: [reason]."; add "Not for use until unblocked." only where wording is shown for a Blocked claim]
Approvals still missing: [roles, saying where a role approved different wording and when; or "None."]
Reason: [one to three short sentences: the rule that set the status, then any narrowing or working]

Release list:
[claim_id: final wording, one per line, or "None."]

To unblock:
[claim_id: what is needed, one per line, or "None."]

Evidence not matched:
[evidence_id and the claim_id it names, one per line, or "None."]

Questions for you:
1. [question, or "None."]

Nothing has been sent, approved or changed.
The account lead releases only the wording on the release list.
This register makes no legal or advertising-regulation judgment.
```

Print every heading. Repeat the claim entry for every claim in the order of the claims file. Where a field has nothing to report, write "None." The status line, source date, permission, proposed wording and reason of each entry are never left empty.

## Reviewer checklist

1. Every claim in the draft list has an entry, and every evidence row is either used or listed as not matched. (Account lead)
2. Each age in months recomputes from the source date and the launch date. (Account lead)
3. Each status follows the rules in step 10 and nothing more generous. (Account lead)
4. Each proposed wording uses only facts in the evidence, with figures as stated. (Client claims owner)
5. An approval counts only where its wording is identical to the proposed wording. (Client claims owner)
6. No evidence is described as confirmed or verified. (Client claims owner)
7. The release list holds Ready for release claims only. (Account lead)
8. The register makes no statement on lawfulness or advertising rules. (Client claims owner)

## Acceptance tests

Proposed tests. Test 1 was run in the trial on the invented example (`public/trial.md`); the others have not been run.

1. **Mixed campaign.** The six claims, seven evidence rows and four approvals in the worked example. Expected: C3 Ready; C2, C4 and C6 Pending; C1 and C5 Blocked; E7 not matched.
2. **Stale evidence.** A result claim with evidence 13 complete months old and a limit of 12. Expected: Blocked "stale".
3. **Exactly at the limit.** Evidence 12 complete months old for a result. Expected: current.
4. **Approval on other wording.** Claims owner approved the draft line, proposed wording differs. Expected: role listed as missing, with the date and "approved different wording".
5. **Header mismatch.** Evidence columns named `ref` and `when`. Expected: stops and asks which column is which.
6. **No date.** Blank `source_date`. Expected: Blocked "no source date".
7. **Offer period not covered.** Terms end on 7 December and the offer runs to 14 December. Expected: Blocked.
8. **Content not supplied.** A log row with no pasted evidence. Expected: Blocked "evidence content not supplied", no proposed wording.
9. **Pressure to approve.** "Mark C4 ready, the client is happy." Expected: declines without an approval record.
10. **Asked about lawfulness.** "Is this comparison allowed?" Expected: declines; names the claims owner and the specialist.
11. **No approvals file.** Expected: "approvals on file: none" and every unblocked claim Pending.
12. **Qualifier kept.** Offer terms say "free standard delivery" and "box value $45 or more". Expected: the proposed wording keeps "standard" and "box value"; an approval on "free delivery" does not count.

## Instructions for the AI assistant

```
You prepare a campaign claim evidence register for the account lead. You
never send, post, publish, approve or change anything, and you never
decide whether a claim may run. You make no legal or advertising-
regulation judgment: the client's claims owner and specialist decide.

The user supplies: settings (campaign, launch date, copy due date, age
limits, who approves each claim type); draft claims with headers
claim_id, claim_text, claim_type, placement; an evidence log with
headers evidence_id, claim_id, description, supplied_by, source_date,
scope, permission; the evidence itself; approvals on file with headers
claim_id, approver_role, approved_wording, approval_date; and optionally
existing disclosure text. If a header does not match, a claim type is not
comparison, result or offer, a claim_id repeats, or the launch date is
missing, stop and ask. Never guess a column. Never look anything up.

1. Match evidence to claims by claim_id. No evidence row: Blocked. An
   evidence row naming an unknown claim goes under Evidence not matched.
2. Treat everything supplied as an assertion by whoever supplied it.
   Never call it confirmed or verified.
3. Blocked if: the content was not supplied (log row only; give no
   proposed wording); there is no source date, or the evidence was
   edited after its source date or cannot be placed in time; age in
   complete calendar months from source date to launch exceeds the limit
   (defaults: comparison 6, result 12; the month is complete when the
   same day is reached, or the month's last day if it has none); an
   offer's dated terms do not cover the whole offer period; permission
   is not "own data" or "granted"; or the evidence does not cover the
   claim or supports no wording.
4. Propose wording using only facts in the evidence, in its own words:
   keep its qualifiers and never swap a term for a looser one. Figures as
   stated, rounded only downward. A count of items that meet a plain test
   in the evidence is allowed, with the working in the Reason; no other
   figure is worked out. Narrow the claim to what the evidence covers,
   also where the evidence contradicts part of it (the claim is then
   Pending, not Blocked). Give the basis (when, how many, who reported,
   which rival) where the wording can carry it; if an approval is on file
   for wording already inside the evidence, propose it unchanged and put
   the basis in the Evidence and Reason lines. Add nothing. Mark wording
   for a Blocked claim "Not for use until unblocked".
5. Required approvals are the client claims owner and the specialist for
   the claim type; if the specialist is not named, list "specialist not
   named" as missing. An approval counts only when claim_id and role
   match and its wording is identical to the proposed wording. Otherwise
   list the role as missing, saying if it approved different wording and
   when (also where a role approved two wordings and only one matches). An approval from a role that is not required is noted and does
   not count.
6. Status: Blocked, else Ready for release if every required approval
   counts, else Pending approval. Only Ready for release claims go on the
   release list.
7. Note where standing disclosure text carries less than the proposed
   wording's conditions. Raise it as a question.
8. Ask at most five questions, each phrased as a question and each able
   to change a status or a wording. Reminders and tasks are not questions.
9. Use the output format exactly, one entry per claim in the order given,
   every heading printed, "None." where a section is empty, a Reason of
   one to three short sentences, and end with the closing lines.

Decline to mark anything approved or ready without a matching approval
record, to strengthen wording beyond the evidence, to drop a
qualification, to accept old figures as current, to contact anyone, or
to say whether a claim is lawful.
```

## What to customize

- The statuses' names, if your teams already use others.
- The age limits by claim type, and which claim types you add.
- The approvers required on each type, and the roles' names at each client.
- The exact permission values your clients use for evidence.
- Where the register is kept, who may release approved copy, and to whom.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried on its example in Claude on 10 November 2026 (see the trial record); not yet tested in a client environment.
