---
name: "lead-form-field-review"
description: "Prepare, for one inquiry form and one period, a field-by-field review that ties every field the form asks for to the use made of its answer after submission, beside how many people reached the field, filled it, saw a validation message there and left there. Fields that need attention become numbered findings, each with its facts, a proposed label or error message where the current one does not help, a test question and a question for the people who decide. The assistant prepares; it never edits the form, removes or reorders a field, predicts a result, contacts anyone or decides any change."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  capability: "Lead form field review"
---

# Lead form field review

This is the technical file for a Fully Powered capability template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
