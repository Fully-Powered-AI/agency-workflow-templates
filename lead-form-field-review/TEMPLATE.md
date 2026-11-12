# Lead form field review

Workflow template, version 0.1.0.

## Purpose

Prepare, for one inquiry form and one period, a field-by-field review that ties every field the form asks for to the use made of its answer after submission, beside how many people reached the field, filled it, saw a validation message there and left there. Fields that need attention become numbered findings, each with its facts, a proposed label or error message where the current one does not help, a test question and a question for the people who decide. The assistant prepares; it never edits the form, removes or reorders a field, predicts a result, contacts anyone or decides any change.

## When to use it and when not to

Use it when a client questions a long inquiry form or the share of people who start it and do not submit it, and a completion export for a stated period is available. Run it again after a change has been approved, built and had time to collect a new period.

Do not use it:

- to judge how the site is found or understood; that is the website findability audit;
- to decide what events to collect on a site; that is the tracking event plan;
- to explain why people left. The export holds counts, not reasons; a session with real users is a different piece of work;
- to review consent wording. The data owner holds it, and the review does not judge it.

## Roles

- **Runs it:** the conversion lead, or whoever at the agency looks after the form.
- **Supplies the field-use notes and approves any change to a field:** the client's data owner.
- **Decides what goes forward:** the conversion lead and the client data owner together.
- **Implements an approved change:** the developers, after review.
- **Named in the follow-up process:** the client's sales, service or operations roles, who confirm how an answer is used.

## Inputs

1. **Review settings.** The client, the form's name and address, the period, the as-of date, whether the form changed during the period, the form's totals (views, starts, submissions), the stage by which the form must supply what the follow-up needs, the exit flag, the validation flag, the minimum reached to judge a field, the conversion lead, the data owner and who receives the review. Defaults: exit flag 10 percent, validation flag 15 percent, minimum reached 100, data needed by stage 1. Say when a default is used. If the period or any of the three totals is missing, stop and ask.
2. **Form definition** (form_fields.csv), one row per field, with these headers: `field_order`, `field_label`, `field_type`, `required`, `choices_or_rule`, `validation_message`, `shown_when`. If the file is missing, stop. If a header does not match, stop and ask which column is which; never guess.
3. **Completion export** (completion.csv), one row per field, with these headers: `field_label`, `reached`, `filled`, `errors`, `exits_here`. `reached` is how many people were shown the field, `filled` how many left it with an accepted answer, `errors` how many times a validation message was shown there (times, not people), and `exits_here` how many left the form at that field. If the file is missing, continue with the use side only and mark every completion figure unassessed. If a header does not match, stop and ask. Counts only; ask for no lead records or personal details, and if some are pasted, do not copy them into the review.
4. **Field-use notes** (field_use.csv), one row per field, with these headers: `field_label`, `used_for`, `used_by`, `first_used_stage`, `required_by`, `requirement_ref`, `note`. `required_by` is `consent`, `business` or `none stated`. `first_used_stage` is a stage number from the follow-up process, or a word such as `report` for a use outside it. If the file is missing, treat every field as "use not stated". If a header does not match, stop and ask.
5. **The follow-up process,** as numbered stages from the first reply onward. If missing, stop: the stage numbers in the notes mean nothing without it.
6. **The data requirements,** each with a reference, the requirement and an owner. If missing, a field may be held as required only where the notes already say so; say that the requirements text was not supplied.

The assistant works from the files and notes the person supplies. It needs no connection to the form tool, the website or the customer records, and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm one form, one period and one set of totals. Match field labels across the three field files by label, ignoring case and spaces at the ends. A label in the export or the notes that is not in the form definition stops the review: ask the conversion lead whether the form changed in the period. A field in the form definition missing from the export or the notes is carried forward and marked unassessed on that side.
2. **Check the counts.** Starts must not exceed views, submissions must not exceed starts, and the exits across all fields must equal starts minus submissions. If a check fails, stop, report the figures and the difference, and draft nothing else. If the form changed in the period, say in the header that the figures blend two forms and judge no field that changed.
3. **Work out the form's totals.** Start rate is starts divided by views. Completion is submissions divided by starts. Those who left are starts minus submissions. Name the three fields with the most exits and their share of all exits. Round percentages to one decimal place, and compare against the flags using the unrounded figures.
4. **Work out each field.** Filled rate is filled divided by reached. Exit rate is exits at the field divided by reached. Validation rate is errors divided by reached; it counts times a message was shown, not people, so call it "shown per hundred who reached the field" and never "share of people", and it can exceed 100 percent. If reached is under the minimum, write "too few to read" and judge nothing from the counts for that field; its use side is still reviewed.
5. **Give each field a status,** the first that applies:
   - **Required by consent requirement [ref]** when `required_by` is consent.
   - **Required by business requirement [ref]** when it is business.
   - **Use not stated** when `used_for` is empty or the field has no note.
   - **Used later than the form needs it (stage n)** when `first_used_stage` is a number greater than the stage by which the form must supply what is needed.
   - **Used at stage n** when it is a number at or below that stage.
   - **Used outside the follow-up ([use])** when it is not a number.
6. **Raise findings.** A field gets a finding when any of these holds, and carries every kind that applies in one finding:
   - **Use:** the status is use not stated, or used later than the form needs it, and the field is required on the form.
   - **Exits:** the exit rate is at or over the exit flag.
   - **Validation:** the validation rate is at or over the flag, or the message is empty or generic ("Error in field", "Not valid", "Required", "Error") and the field shows at least one.
   - **Label:** the label is a bare generic word that names nothing to enter ("Details", "Other", "Info", "Notes"), or the label and the use note name different things. Nothing else makes a Label finding; whether a label is clear enough is not judged.
   - **Choices:** the choice for exactly one figure is not clear from the words, or the choices do not fit the use. That is any of these three cases:
     - the choices or rule on the form do not match what the notes or the data requirements say the answer is used for;
     - a figure is the edge of two choices (for example "Under 20,000" and "20,000 to 50,000");
     - a figure lies in none of the choices.
   Number the findings in the form's order. A field with no kind has no finding.
7. **Write the proposals.** For each finding:
   - **Proposed label,** only for a Label finding, or for a Use finding where the field stays; built from the use note's own words. It may add "(optional)" only where the form definition shows the field as optional, and "your" where the note's words say the answer is for the person's own booking or request; it adds nothing else. Never for a consent field. Otherwise write "no change proposed".
   - **Proposed error message,** only for a Validation finding; it says what is wrong and what to do, using only the facts of the rule on the form (its own words or a plain restatement of them): no example values, no added detail. If no rule was supplied, write "rule not supplied; no message proposed". Never write one that blames the person. For a consent field the message may restate only the rule (for example "must be ticked"), never reword or judge the consent text, and it is marked as needing the data owner's approval.
   - **Test question,** exactly one (none for a consent field, where it would be about its wording), phrased neutrally, naming the current figure as the baseline and what would be compared, as one comparison of the form as it is with one stated version (for a Use finding on a required field, the version in which the field is optional). Say if the export cannot answer it and what would; where the question is about a proposed change, ask whether the proposed label or message changes the figure and never assume it is clearer. Never state or imply what the result will be.
8. **Write the question.** One per finding, to the conversion lead and the data owner, with the facts that bear on it. A Validation finding alone asks who set the rule on the form and what depends on it; for a consent field it asks whether the data owner approves the message. Where a field is required on the form and carries a Use finding (use not stated, or used later than the form needs it), set out all four options (keep as it is, make optional, ask later, remove) without choosing between them and leaving none out. An Exits finding without a Use finding, on a field whose stated use is needed in time, or on an optional field, gets no option list and no option to remove or loosen it; the question asks the owner of the use whether anything about how the field is asked can be looked at. Where the field also has a Choices finding, the question is about the Choices issue instead, and takes precedence. For a consent or business-required field, offer no option that removes it or makes it optional, and say why it is held. Recommend nothing unless asked.
9. **Close.** List the fields with no finding, the fields held as required, and everything not assessed with what is missing, or "nothing" with the reason. End with the trace line and return the draft to the person who ran it only.

## Exceptions and stop conditions

- **Counts fail** (exits do not equal starts minus submissions, submissions over starts, starts over views): stop and report the figures and the difference.
- **A header does not match the default:** stop and ask which column is which.
- **A label in the export or notes is not on the form:** stop and ask whether the form changed in the period.
- **Completion export missing:** continue on the use side; mark completion unassessed; raise no Exits or Validation finding.
- **Reached under the minimum:** "too few to read"; raise no Exits or Validation finding for the field.
- **A field's use is not stated:** raise the finding and ask. Never treat it as unneeded, and never fill in a use from the label.
- **A consent or business-required field:** keep it. Do not suggest dropping it, making it optional or moving it. A proposed error message is allowed only as the rule restated and needs the data owner's approval; the consent wording is never judged or reworded.
- **Asked to predict a gain, edit the form, remove a field, rank fields by what should go, judge consent wording, or send the review:** decline; the conversion lead and the data owner decide.
- **Personal details pasted in:** do not copy them; ask for counts only.

## Output format

```
LEAD FORM FIELD REVIEW: [form name], [client]

For: [conversion lead] and [client data owner]. Period [from] to [to]; as of [date]. Form changed in the period: [yes or no].

Form: [n] views, [n] starts ([%] of views), [n] submissions ([%] of starts), [n] left before submitting. Check: exits by field add to [n] = [starts] - [submissions]. Most exits: [field] [n], [field] [n], [field] [n], together [n] of [n] ([%]).
Follow-up stages as supplied: [list]. The form must supply what is needed by stage [n].

FIELD BY FIELD

[order]. [Label] ([type], [required or optional])
Use: [used for], by [role], first used at stage [n] (or, for a use outside the stages, first used outside the follow-up stages). Required by: [ref and requirement, or nothing stated]. Status: [status].
Completion: reached [n], filled [n] ([%]), left here [n] ([%]), validation message shown [n] times ([%] of those who reached it).
Finding: [number, or none].

FINDINGS

[n]. [Field], [kinds]
Facts: [the figures, the flags they meet, the message or rule on the form, the use note].
Proposed label: [label, or no change proposed].
Proposed error message: [message, or no change proposed].
Test question: [question, or none].
Question for the conversion lead and the client data owner: [question and options].

Fields with no finding: [list, or none].
Held as required: [field (ref)], or none.
Not assessed: [field and what is missing], or nothing with the reason.

Every figure traces to the form definition, the completion export for [period], the field-use notes, the follow-up stages and the data requirements supplied. The review changes no form and sends nothing; the conversion lead and the client data owner approve any change, and developers implement it after review.
```

## Reviewer checklist

1. The exit check holds: exits by field equal starts minus submissions. (Analytics lead)
2. Every percentage matches its two counts, and each flag was applied to the unrounded figure. (Analytics lead)
3. Every field in the form definition has a block, in the form's order, with a status. (Conversion lead)
4. Every use shown is the data owner's note, not a guess from the label. (Client data owner)
5. No consent or business-required field is proposed for removal, made optional or moved, and any message for a consent field only restates its rule. (Client data owner)
6. Each proposed error message uses only the facts of a rule that was supplied, and each proposed label comes from the use note's words. (Developers)
7. No sentence predicts a result, gives a reason people left, or calls a field wasted. (Conversion lead)
8. Every finding has one test question (none for a consent field) and one question for the people who decide; where a required field carries a Use finding, all four options (keep, make optional, ask later, remove) are set out without a recommendation. (Conversion lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal run.** The invented example in the public folder. Expected: ten blocks, seven findings, three fields with none, three held as required, and four options on each of the two Use findings.
2. **Exits do not add up.** Exits sum to 900 where starts are 1,260 and submissions 340. Expected: stops; reports a difference of 20; drafts nothing else.
3. **Header mismatch.** The export names a column `left_at` in place of `exits_here`. Expected: stops and asks which column is which.
4. **Business-required field with high exits.** A field required by a stated business requirement has 33.3 percent exits. Expected: an Exits finding, and a Label or Choices finding if one of those rules applies; no option to remove it or make it optional; the reason it is held is stated.
5. **Too few to read.** A conditional field with 80 reached and 30 exits. Expected: "too few to read"; no Exits finding; the use side still reviewed.
6. **Use not stated.** A required field with no note. Expected: a Use finding that asks who uses it; not called unneeded.
7. **No completion export.** Expected: use-side review only; every completion figure unassessed; no Exits or Validation finding.
8. **Asked to predict.** "How many more leads will we get if we drop the phone number?" Expected: declines; offers the test question instead.

## Instructions for the AI assistant

```
You prepare a lead form field review for the conversion lead and the
client's data owner. You never edit the form, remove or reorder a field,
contact anyone or send the review, and you never decide any change: the
conversion lead and the data owner approve, and developers implement after
review.

The user will supply: review settings; the form definition; the completion
export; the field-use notes; the follow-up process; the data requirements.
Settings: if the user gives none, use exit flag 10 percent, validation
flag 15 percent, minimum reached 100, and data needed by stage 1, and say
that defaults were used; the stage setting says by which follow-up stage the
form must supply what is needed. Use the default column headers:
form_fields.csv has field_order, field_label, field_type, required,
choices_or_rule, validation_message, shown_when; completion.csv has
field_label, reached, filled, errors, exits_here; field_use.csv has
field_label, used_for, used_by, first_used_stage, required_by,
requirement_ref, note. If a header does not match, stop and ask. Match labels across the files ignoring case and
spaces at the ends. If the settings' period or totals, the form
definition or the follow-up process is missing, stop and say so. If the
field-use notes are missing, treat every field as use not stated. If the
data requirements are missing, hold a field as required only where the
notes already say so, and say the requirements were not supplied. If the
form changed in the period, say in the header that the figures blend two
forms and judge no field that changed. If the completion export is
missing, review the use side only, mark every completion figure unassessed
and raise no Exits or Validation finding. Ask for counts only; do not copy
personal details into the review.

1. Check counts: starts not over views, submissions not over starts, exits
   across fields equal to starts minus submissions. If any fails, stop,
   report the figures and the difference, and draft nothing else. Stop and
   ask if a label in the export or notes is not on the form.
2. Work out the form's totals, naming the three fields with the most
   exits and their share of all exits, and, for each field, filled, exit
   and validation rates (counts over reached; the validation rate counts
   times shown, not people, so say "shown per hundred who reached it").
   Round to one decimal place; compare to the flags unrounded. Under the
   minimum reached, write "too few to read" and judge nothing from the
   counts.
3. Give each field a status, the first that applies: required by consent,
   required by business, use not stated, used later than the form needs it,
   used at a stage, used outside the follow-up.
4. Raise a finding for Use (required on the form and use not stated or
   later), Exits (at or over the exit flag), Validation (at or over the
   flag, or an empty message or a generic one such as "Not valid",
   "Required", "Error" or "Error in field", with at least one shown),
   Label (a bare generic word such as "Details", or a label and use note
   that name different things) or Choices (not matching the use, a figure at the edge of two choices, or a
   figure in none). Skip Exits and Validation where reached is under the
   minimum. Number in the form's order.
5. For each finding write: facts; proposed label (only for a Label
   finding, or a Use finding where the field stays; never for consent; from
   the use note's words, adding "(optional)" only where the form shows the
   field as optional and "your" only where the note says the answer is for
   the person's own booking or request; otherwise "no change proposed");
   proposed error message (only for a Validation finding; only the facts of
   a rule that was supplied; never one that blames the person; for a
   consent field only the rule restated, marked as needing the data owner's
   approval); exactly one neutral test question, one comparison of the form
   as it is with one stated version (for a Use finding on a required field,
   the version where the field is optional), naming the current figure and
   what the export can or cannot answer (none for a consent field; ask
   whether a proposed change alters a figure, never assume it is clearer);
   one question for the lead and data owner (for a Validation finding
   alone, who set the rule and what depends on it; for a consent field,
   whether the data owner approves the message). Where a required field
   carries a Use finding, set out all four options (keep as it is, make
   optional, ask later, remove) and recommend none. An Exits finding alone
   gets no option list; one beside a Choices finding asks about the Choices
   issue instead.
6. Keep every consent or business-required field. Never suggest dropping,
   loosening or moving it, and never judge consent wording.
7. Never predict a gain, give a reason people left, or call a field
   wasted. Report counts as counts.
8. Use the output format exactly. Empty parts say what is empty and why.
   Return the draft to the person who ran it only.

If asked to predict, edit the form, remove a field or send, decline.
```

Paste this block as custom instructions, followed by the output format above.

## What to customize

- Your column names, or rename them once to the defaults.
- The exit flag, the validation flag and the minimum reached.
- Your follow-up stages and the stage by which the form must supply its data.
- Who holds the data requirements and who approves a field change.
- Which words count as a generic validation message for your form tool.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried once on its invented example in Claude on 10 November 2026, after two independent reviews that day; the record is in the public folder. That run was not blind to the published example output, and a blind run is still to do. Not yet tested in a client environment.
