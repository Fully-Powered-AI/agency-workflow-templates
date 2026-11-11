# Lead form field review: trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (Client R, an invented commercial cleaning company, with its form, counts and notes all invented). No client data was used. The inputs were the six blocks under "The inputs" in that file, with one change from the earlier run: the Phone number field's form message is now "Error in field" in place of a different stock string. The run followed the instruction block and the output format in `member/template.md` as revised after a third independent review on the same day.

Limits on this trial, stated first:

- **The run was not blind.** The same session that made the revisions then ran the template over the example, so the published output was known beforehand, and the review was written by applying the revised block line by line to the six inputs and then compared with the published example. The status, finding and wording choices followed the revised rules, but they are not independent of the published output, and the output below is the published example's review word for word. That sameness is a consequence of the run not being blind, not evidence that two independent runs agree.
- **The figures were not worked out again.** This revision changed no count. The rates, the exit check of 920 = 1,260 - 340 and the three largest exits (67.4 percent) were checked with a short script in the earlier run and carried over; this run did not repeat that check.
- **This record replaces earlier ones.** The run recorded here is one of several that day; earlier records were replaced, and earlier outputs are not reproduced here. The earlier runs found problems that later revisions addressed: facts in the published output that were not in the inputs, a missing remove option, rules that were silent or subjective, and a stock form message in the example. This revision further changed the rule for when a label is proposed and what it may add, the one-comparison test question, the question on a validation finding, the list of generic messages in the instruction block, and the stock message above.
- **Nothing has been run since.** No edit made after this run has been run again, and a blind run is still owed.

## What came out

```
LEAD FORM FIELD REVIEW: Request a quote, Client R

For: the conversion lead and the client data owner. Period 2026-10-01 to 2026-10-31; as of 2026-11-09. Form changed in the period: no.

Form: 4,200 views, 1,260 starts (30.0% of views), 340 submissions (27.0% of starts), 920 left before submitting. Check: exits by field add to 920 = 1,260 - 340. Most exits: Phone number 280, Annual budget 190, Your role 150, together 620 of 920 (67.4%).
Follow-up stages as supplied: 1 First reply; 2 Quote; 3 Site survey. The form must supply what is needed by stage 2.

FIELD BY FIELD

1. Full name (text, required)
Use: greeting in the first reply and the contact record, by the sales coordinator, first used at stage 1. Required by: nothing stated. Status: used at stage 1.
Completion: reached 1,260, filled 1,200 (95.2%), left here 60 (4.8%), validation message shown 0 times (0.0% of those who reached it).
Finding: none.

2. Work email (email, required)
Use: where the reply and the quote are sent; key to the contact record, by the sales coordinator, first used at stage 1. Required by: nothing stated. Status: used at stage 1.
Completion: reached 1,200, filled 1,110 (92.5%), left here 90 (7.5%), validation message shown 210 times (17.5% of those who reached it).
Finding: 1.

3. Phone number (tel, required)
Use: booking the site survey after a quote is accepted, by the survey scheduler, first used at stage 3. Required by: nothing stated. Status: used later than the form needs it (stage 3).
Completion: reached 1,110, filled 830 (74.8%), left here 280 (25.2%), validation message shown 330 times (29.7% of those who reached it).
Finding: 2.

4. Company (text, required)
Use: existing-client check and the quote header, by the sales coordinator, first used at stage 1. Required by: DR3, company name is needed to check whether the lead is already a client. Status: required by business requirement DR3.
Completion: reached 830, filled 790 (95.2%), left here 40 (4.8%), validation message shown 0 times (0.0% of those who reached it).
Finding: none.

5. Your role (text, required)
Use: not stated. Required by: nothing stated. Status: use not stated.
Completion: reached 790, filled 640 (81.0%), left here 150 (19.0%), validation message shown 0 times (0.0% of those who reached it).
Finding: 3.

6. Number of sites (dropdown, required)
Use: chooses the quote template, by the sales coordinator, first used at stage 2. Required by: nothing stated. Status: used at stage 2.
Completion: reached 640, filled 570 (89.1%), left here 70 (10.9%), validation message shown 0 times (0.0% of those who reached it).
Finding: 4.

7. Annual budget (dropdown, required)
Use: sorting new leads into priority bands on Monday mornings, by the sales manager, first used at stage 1. Required by: DR2, every lead carries a budget band so the sales manager can sort leads. Status: required by business requirement DR2.
Completion: reached 570, filled 380 (66.7%), left here 190 (33.3%), validation message shown 0 times (0.0% of those who reached it).
Finding: 5.

8. Details (textarea, optional)
Use: special requests for the quote, by the sales coordinator, first used at stage 2. Required by: nothing stated. Status: used at stage 2.
Completion: reached 380, filled 150 (39.5%), left here 20 (5.3%), validation message shown 0 times (0.0% of those who reached it).
Finding: 6.

9. How did you hear about us (dropdown, optional)
Use: monthly source report, by the marketing lead, first used outside the follow-up stages. Required by: nothing stated. Status: used outside the follow-up (monthly source report).
Completion: reached 360, filled 240 (66.7%), left here 10 (2.8%), validation message shown 0 times (0.0% of those who reached it).
Finding: none.

10. I agree to be contacted about my enquiry (checkbox, required)
Use: record of permission to contact, by the sales coordinator, first used at stage 1. Required by: DR1, permission to contact must be recorded before anyone is contacted. Status: required by consent requirement DR1.
Completion: reached 350, filled 340 (97.1%), left here 10 (2.9%), validation message shown 25 times (7.1% of those who reached it).
Finding: 7.

FINDINGS

1. Work email, Validation
Facts: the validation message was shown 210 times to the 1,200 who reached the field (17.5%, over the 15% flag); 90 (7.5%) left here, under the 10% flag. The message reads "Not valid", which is generic. The rule on the form is "Work address only; free webmail domains rejected".
Proposed label: no change proposed.
Proposed error message: "Use a work email address. Addresses from free webmail services are not accepted."
Test question: of the 210 times the message was shown, how many were followed by a corrected entry and how many by leaving the form? This export does not hold it; ask for the form tool's error log.
Question for the conversion lead and the client data owner: who set the work-address rule, and does the sales coordinator depend on it? The review assumes neither answer.

2. Phone number, Use, Exits, Validation
Facts: left here 280 of 1,110 (25.2%, over the 10% flag), the most exits of any field (280 of 920, 30.4%). The validation message was shown 330 times (29.7%, over the 15% flag) and reads "Error in field"; the rule is "10 digits with no spaces or symbols". The field is required on the form. Its stated use is booking the site survey at stage 3, after the quote is accepted; quotes go by email; the form must supply what is needed by stage 2. No data requirement names it.
Proposed label: if the field stays, "Phone number (to book your site survey)", from the use note's words.
Proposed error message: "Enter the phone number as 10 digits, with no spaces or symbols."
Test question: compare the form as it is now with a version where the phone number is optional: what share of those who start finish (now 340 of 1,260, 27.0%)? The export answers that for a later period; whether the survey scheduler still reaches every client who accepts a quote needs the scheduler's records.
Question for the conversion lead and the client data owner: the options are keep it as it is (with the proposed label and message), make it optional, ask for it later (at quote acceptance), or remove it. Which, if any, goes to developers? No option is recommended.

3. Your role, Use, Exits
Facts: left here 150 of 790 (19.0%, over the 10% flag). The field is required on the form. The note says nobody could say what it is for. No data requirement names it.
Proposed label: no change proposed; there is no stated use to build a label from.
Proposed error message: no change proposed; no validation message was shown.
Test question: compare the current form with a version where the field is optional: what share of those who start finish (now 340 of 1,260, 27.0%)? The export answers that for a later period.
Question for the conversion lead and the client data owner: what is this field used for, by whom, and at which stage? The options are keep it as it is, make it optional, ask for it later, or remove it. No option is recommended; until a use is stated the review treats the field as neither needed nor unneeded.

4. Number of sites, Exits, Choices
Facts: left here 70 of 640 (10.9%, over the 10% flag). The choices on the form are "1; 2 to 5; 6 to 10; 11 or more"; the quote templates are "1 site; 2 to 9 sites; 10 or more", so a lead choosing "6 to 10" cannot be matched to one template. The field is used at stage 2, in time.
Proposed label: no change proposed.
Proposed error message: no change proposed; no validation message was shown.
Test question: with choices that follow the templates, how many leads need the sales coordinator to ask the number of sites again, set against the share who leave here now (10.9%)? The export cannot answer the first part; the coordinator's records would.
Question for the conversion lead and the client data owner: should the choices follow the quote templates, or the templates follow the choices?

5. Annual budget, Exits, Choices
Facts: left here 190 of 570 (33.3%), the highest share of any field and over the 10% flag. The field is required by DR2, so the review holds it as required and offers no option to remove it or make it optional. The choices are "Under 20,000; 20,000 to 50,000; Over 50,000": 20,000 and 50,000 each appear as the edge of two choices, so the choice for exactly that figure is not clear from the words. The use note says the answer sorts new leads into priority bands.
Proposed label: no change proposed.
Proposed error message: no change proposed; no validation message was shown.
Test question: if the choices say which band 20,000 and 50,000 each belong to, does the share who leave here change from now (33.3%)? The export answers that for a later period; whether leads fall in the band the sales manager intends needs the sales manager's records.
Question for the conversion lead and the client data owner: which band does the sales manager give a lead at exactly 20,000, and at exactly 50,000?

6. Details, Label
Facts: filled by 150 of the 380 who reached it (39.5%); left here 20 (5.3%, under the flag). The label "Details" is a bare generic word that names nothing to enter. The use note says the field is read at stage 2 for special requests for the quote.
Proposed label: "Special requests for the quote (optional)".
Proposed error message: no change proposed; no validation message was shown.
Test question: does the proposed label change how many fill the field (now 39.5%)? The export answers that for a later period.
Question for the conversion lead and the client data owner: does the sales coordinator want the field to ask for something more specific?

7. I agree to be contacted about my enquiry, Validation
Facts: the validation message was shown 25 times to the 350 who reached the field (7.1%, under the 15% flag), and it reads "Required", which is generic and does not say what to do. The field is required by consent requirement DR1; the review keeps it and does not judge its wording. The rule on the form is "Must be ticked".
Proposed label: no change proposed; the wording is held by the data owner.
Proposed error message: "This box must be ticked." The rule restated; it needs the data owner's approval.
Test question: none.
Question for the conversion lead and the client data owner: does the data owner approve the message? The options for the field itself do not arise: it is held as required because of DR1.

Fields with no finding: Full name, Company, How did you hear about us.
Held as required: Company (DR3), Annual budget (DR2), I agree to be contacted about my enquiry (DR1). None is proposed for removal or made optional.
Not assessed: nothing. Every field in the form definition appears in the export, and every field has at least 100 who reached it.

Every figure traces to the form definition, the completion export for 2026-10-01 to 2026-10-31, the field-use notes, the follow-up stages and the data requirements supplied. The review changes no form and sends nothing; the conversion lead and the client data owner approve any change, and developers implement it after review.
```

## What was observed

- **Every required part was produced:** the header, the totals and the exit check, ten field blocks in the form's order, seven findings, and the three closing lists with the trace line. The counts check held and no label or header was out of place.
- **The acceptance test for this example is met:** ten blocks, seven findings, three fields with none, three held as required, and all four options on each of the two Use findings (Phone number, Your role).
- **Facts that are not in the inputs:** the Work email proposal was written from the rule "Work address only; free webmail domains rejected" and the form's message "Not valid". The output was checked line by line against the inputs for anything not in them. No currency, no timing, no example email address and no phrase about "cleaning" appears in any proposed label or message. The Details label uses the use note's words ("Special requests for the quote") with "(optional)", which the revised rule allows only where the form shows the field as optional (it does here). The Phone number label adds "your" and the note's words, which the revised rule allows.
- **Rules that changed since the first run, and how this run used them:**
  - The Label test now fires only for a bare generic word or a label that names something different from the use note. "Details" qualifies. "Number of sites", "Annual budget" and "Your role" do not, so none of them has a Label finding. The first run's published example had raised one on Number of sites; that no longer applies.
  - The Choices rule now covers a figure at the edge of two choices. It fired on Annual budget (20,000 and 50,000 each appear in two choices) and it did not fire on Number of sites' own bands (no shared figure). Whether a reader would find "Under 20,000" and "20,000 to 50,000" unclear at 20,000 is arguable; the rule treats the shared figure as the trigger and the finding only asks the sales manager which band each figure belongs to.
  - A consent field may have a proposed error message, only the rule restated, marked as needing the data owner's approval; the run proposed "This box must be ticked." from the rule "Must be ticked".
  - The Exits-only rule: Number of sites and Annual budget each have an Exits finding without a Use finding, so neither got an option list. Both are used in time (stage 2 and stage 1) and Annual budget is also held by DR2.
- **Where the instructions were still ambiguous:**
  - A Choices finding beside an Exits finding: the revised block says the question is about the Choices issue and takes precedence, and this run followed that on Number of sites and Annual budget. The first run had found this ambiguous.
  - A proposed label is to come from the use note's words, but use notes describe a process and seldom make a label. For Phone number the run used "(to book your site survey)", the note's own words; for Details it used the note's words directly. For Your role there are none, so none was proposed.
  - Whether a Use finding's proposed label applies "where the field stays" is the very question being asked, so the label is offered conditionally.
  - Whether "optional" or a possessive may be added to a label is now stated in the template; this run applied that rule.
  - Test questions on the two Use findings now compare the form as it is with one version, the field optional; the earlier run offered two variants in each.
- **What this trial does not show:** it was one run, by one model, on an invented example, with the published output known beforehand. It says nothing about a real client's files, a different product, or the other acceptance tests, none of which was run. A blind run on the revised template is still to do.
