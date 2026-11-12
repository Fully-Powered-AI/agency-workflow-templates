# Missed milestone client reply

Workflow template, version 0.1.3.

## Purpose

Prepare two things for the account director when a client challenges a delay, a deliverable or something the agency said earlier: a draft reply to the client, and an internal action note. Both are built only from the records supplied. The note separates confirmed facts from proposed recovery steps and from the decisions still needed. The reply states what the records support and leaves a marked gap wherever a date, a concession or a position has not been approved. The assistant prepares; it never sends, never admits fault, never offers a credit or fee change, and never states a date the delivery team has not confirmed.

## When to use it and when not to

Use it when a client message disputes a date, a deliverable, a scope point or a prior commitment, and the director wants a considered reply on the same day.

Do not use it for an ordinary message that needs an answer (use customer reply drafting), for handing a support case to a senior person (use a support escalation brief), or for the scheduled status update (use client-status update preparation). Do not use it to decide who is responsible, to interpret a contract, or to give legal advice; if the client or the agency raises a legal question, the note says so and the director takes it to whoever handles contracts. If the client has said they will end the relationship or take formal action, stop and tell the director this goes beyond a reply.

## Roles

- **Starts it and supplies the inputs:** the account director, or the account manager for the director.
- **Confirms delivery facts and dates:** the delivery lead named on each milestone.
- **Approves the reply, any concession and any revised commitment, and sends:** the account director.
- **Authorises credits and fee changes:** whoever your agency has named; the workflow template never does.

## Inputs

Where an input is a table or export, the default column headers are given. If a header is missing or named differently, stop and ask the person to confirm which column is which; never guess.

1. **Client message,** verbatim, with the date and time it arrived and the sender's role. If missing, stop.
2. **Milestone record.** Headers: `Milestone | Deliverable | Date agreed | Where agreed | Owner`. If missing, stop.
3. **Scope and terms notes.** Short quotations from the statement of work or schedule about revision rounds, feedback windows and extras, with their location. If missing, write "scope terms not supplied" and make no statement about scope.
4. **Approval history.** Headers: `Date | Item | By | Event | Note`. Events are such things as submitted, changes requested, approved. If missing, stop.
5. **Commitments and statements record.** Headers: `Date | Said by | Channel | What was said`. Covers anything either side said about scope, dates or extras, with where it was said. If missing, write "no statements record supplied".
6. **Delivery status.** Headers: `Item | Status | Delivery-confirmed date | Confirmed by | Date confirmed | Condition`. A date counts as confirmed only when `Confirmed by` and `Date confirmed` are both filled. If missing, stop.
7. **Authorised recovery options.** Headers: `Option | Authorised by | Conditions | Limit`. If missing, treat it as "no recovery options authorised" and say so.
8. **Reply settings:** sender, tone, channel, working days, working-day counting rule, public holiday dates, and who authorises credits and fee changes. Defaults: email; plain, warm and direct; Monday to Friday; working days counted after the day of the event, not including it; no public holidays (every Monday to Friday counts, and the note says so); authoriser "not named in the inputs".
9. **Today's date.**

## The procedure

1. **Check the inputs.** First read the client message: if the client has said they will end the relationship, named a lawyer or cited a contract remedy, stop and tell the director this goes beyond a reply. Then confirm headers and that every item named in the client message appears in the milestone record. If an item the client names is not in the record, say so in the note and continue only for the items that are.
2. **Split the client message** into numbered points: each date or deliverable claimed, each statement about what was promised, each request, and each demand with a deadline. A sentence that holds more than one of these is split, one point for each. Quote the client's words in the note.
3. **Build the timeline.** List dated events from the milestone record, approval history, statements record and delivery status in date order, each with its source. Compute elapsed days by calendar and by working day, and show the arithmetic, between each pair of consecutive events and across every gap that bears on a client claim, a client deadline or a milestone.
4. **Check each client claim against the records** and give it exactly one label (a request or demand is not labelled; mark it "Request" and match it to a confirmed fact or a decision):
   - **Supported:** a record says the same.
   - **Contradicted:** a record says something different. Quote both.
   - **Not in the records:** no record either way.
   - **Records disagree:** two supplied records conflict, for example a scope quotation and an earlier statement. Quote both and do not choose.
   - **Responsibility disputed:** the point turns on who caused the slip. Set out the dated facts and do not assign cause.
5. **Sort every statement the reply or note will make** into three lists. **Confirmed facts:** supported by a record, and for any future date by a delivery-confirmed entry. **Proposed recovery steps:** each taken from the authorised options, with its conditions, and with its date marked "confirmed by [name], [date]" or "date not confirmed". **Decisions needed:** each with the person who decides.
6. **Dates.** Never state a future date as a commitment unless the status has it delivery-confirmed. If the delivery lead confirmed a duration or a condition but not a date, show the arithmetic in the note as "arithmetic from a confirmed duration, not a confirmed date" and put the date in the reply only inside a decision gap. If the arithmetic shows a conflict with a client deadline, state the conflict in the note.
7. **Recovery steps.** Offer only options on the authorised list. An option whose conditions already hold on the facts supplied is offered. An option whose condition can still be met, such as a client approval by a future date, is offered as conditional, with the condition stated in the reply and in the note. An option whose condition cannot be met, or cannot be judged from the facts supplied, is not offered; list it under Decisions needed. If a step would help but is not authorised, list it under Decisions needed, not under Proposed recovery steps. Credits, fee changes, free work and extra scope are never proposed; if the client asks for one, record the request as a decision for whoever authorises it.
8. **Draft the reply** in the reply settings. Open with what the client is concerned about, in their terms, without admitting fault or blaming anyone. Then give the confirmed facts that answer each point, in the client's order. Then the recovery steps that are authorised and whose conditions hold, as things the agency can do, never as promises of results. Then what the agency needs from the client and by when, only if a confirmed fact or the scope notes support the deadline; a deadline that falls on the day of sending is stated with its date and flagged under Before sending. If asking for feedback could open a further round that the scope notes say is quoted, say so under Left open. Close with the next contact, as a decision gap if the director has not set it. If no subject line or contact name was supplied, address the contact by role, give a plain subject drawn from the deliverable in the milestone record, and list the subject and the missing name under Before sending as wording the director must check. Put each unapproved item in square brackets as `[DECISION n: …]`, naming the decision.
9. **Never in the reply:** an apology that accepts fault, any comment on a colleague, the words "credit", "refund" or "discount" unless the client used them and then only to say it is being considered by the person who decides, any date without a confirmation, any statement about responsibility.
10. **Write the internal action note** in the output format. State plainly what has not been checked. Print "None." for any empty section.
11. **Return both** to the account director only.

## Exceptions and stop conditions

- **Client message, milestone record, approval history or delivery status missing:** stop; list what is needed.
- **Header mismatch:** stop; ask which column is which.
- **The client names a deliverable that is not in the milestone record:** note it, do not draft a statement about it, and make it a decision for the director.
- **A delivery date is wanted and none is confirmed:** the reply contains a decision gap; the note says the delivery lead must confirm first.
- **The client demands a credit, refund or concession:** record it as a decision for the person who authorises; do not respond to it in the reply except to say it is being considered.
- **The client threatens to end the relationship, names a lawyer, or cites a contract remedy:** stop; tell the director this goes beyond a reply.
- **Asked to admit fault, blame the client, offer a credit, state an unconfirmed date, or send the reply:** decline; these belong to the director.
- **Asked for any step involving a password, a login code or a client system:** decline.

## Output format

```
DRAFT REPLY: not sent

To: [client contact, role]
Channel: [channel]
Subject: [subject]

[Body, in the reply settings. Each unapproved item appears as [DECISION n: what the director must choose or fill in].]

[Sender]

---

INTERNAL ACTION NOTE: [client], [project], [today's date]

Client's points checked
1. "[quoted words]": [Supported / Contradicted / Not in the records / Records disagree / Responsibility disputed / Request]. [Record(s), quoted or cited; for a request, the decision or fact it maps to.]

Timeline
[Date] [event] ([source]). Elapsed: [arithmetic, calendar days and working days].

Confirmed facts
- [Fact] ([source]).

Proposed recovery steps
- [Step] ([authorised by], conditions: [conditions], date: confirmed by [name], [date] / date not confirmed).

Decisions needed
- DECISION [n]: [what must be decided]. Decides: [role]. Facts: [facts]. Needed by: [client deadline, if any].

Left open
- [Items the records cannot settle, including any responsibility question and anything not checked.]

Before sending
- [Checks the director makes, each tied to a decision gap or record.]

Nothing has been sent, offered or committed. The account director approves the
reply, any concession and any revised commitment.
```

Print "None." under any section with no content.

## Reviewer checklist

1. Every fact in the reply and the note traces to a named record. (Account director)
2. Every future date in the reply is delivery-confirmed, or sits inside a decision gap. (Delivery lead)
3. Every elapsed-day figure is recomputed from the dates in the timeline. (Account manager)
4. No recovery step is outside the authorised list, and every condition holds. (Account director)
5. The reply admits no fault, assigns no responsibility, and mentions no credit the client did not raise. (Account director)
6. Every decision gap in the reply has a matching entry under Decisions needed. (Account director)
7. Where two records disagree, both are quoted and neither is chosen. (Account director)
8. Nothing is marked as sent. (Account director)

## Acceptance tests

Proposed tests. None has been run as a set.

1. **Claim contradicted.** Client says nothing arrived; the approval history shows a submission two days earlier. Expected: labelled Contradicted with both records quoted, and the reply states the submission as a fact without suggesting the client is wrong.
2. **Records disagree.** The scope notes say two rounds are included; an earlier email says the second is extra. Expected: labelled Records disagree, both quoted, a decision for the director, and a decision gap in the reply.
3. **Duration but no date.** The delivery lead confirmed four working days from approval and no date. Expected: the date appears in the note as arithmetic only and in the reply only in a decision gap.
4. **Credit demanded.** The client expects no cost. Expected: recorded as a decision for whoever authorises credits; the reply neither offers nor refuses.
5. **No authorised options.** Expected: the note says none is authorised; Proposed recovery steps lists none; steps that might help are listed as decisions.
6. **Header mismatch.** The approval history has `Who` where `By` is expected. Expected: stops and asks which column is which.
7. **Client names a deliverable not in the milestone record.** Expected: noted, no statement about it, a decision for the director.
8. **Asked to send or to admit fault.** Expected: declined.
9. **Option with a future condition.** An authorised option depends on the client approving by a date that has not yet arrived. Expected: offered in the reply as conditional with the condition stated, and shown in the note as not yet met.

## Instructions for the AI assistant

```
You prepare a draft reply and an internal action note for an account
director whose client has challenged a delay, a deliverable or an earlier
commitment. You never send anything, never admit fault, never offer a
credit, refund or discount, never state a date the delivery team has not
confirmed, and never decide who is responsible. The account director
approves the reply, any concession and any revised commitment.
You never ask for passwords, login codes or access to client systems.
Before anything else, read the client message: if the client says they
will end the relationship, names a lawyer or cites a contract remedy,
stop and tell the director this is beyond a reply.
Use only the records the user supplies; add no outside knowledge, such as
public holidays, the client's industry or the law.

The user will supply: the client's message; the milestone record
(Milestone | Deliverable | Date agreed | Where agreed | Owner); scope and
terms notes; the approval history (Date | Item | By | Event | Note); the
commitments and statements record (Date | Said by | Channel | What was
said); the delivery status (Item | Status | Delivery-confirmed date |
Confirmed by | Date confirmed | Condition); the authorised recovery
options (Option | Authorised by | Conditions | Limit); reply settings,
including any public holiday dates and who authorises credits; today's
date. If the client message, milestone record, approval history or
delivery status is missing, stop and say what is needed. If a column
header does not match, stop and ask which column is which. If another
input is missing, say so where it matters and continue.

1. Split the client message into numbered points, one for each claim,
   request or demand (a sentence holding several is split), and quote
   the words. If the client names a deliverable that is not in the
   milestone record, say so, make no statement about it and make it a
   decision for the director.
2. Build a dated timeline from all records, each entry with its source.
   Compute elapsed days by calendar and by working day and show the sums,
   between consecutive events and across every gap that bears on a claim,
   a deadline or a milestone. Count every Monday to Friday unless public
   holiday dates are supplied, and say which. Unless the reply settings
   say otherwise, count working days after the day of the event, not
   including it.
3. Label each claim exactly one of: Supported, Contradicted, Not in the
   records, Records disagree, Responsibility disputed. Mark a request
   or demand "Request" and match it to a fact or a decision. Quote the
   records. Where records disagree, quote both and do not choose.
4. Sort statements into confirmed facts, proposed recovery steps and
   decisions needed. A future date is confirmed only if "Confirmed
   by" and "Date confirmed" are both filled and the "Delivery-confirmed
   date" cell holds a date. Otherwise show any arithmetic in
   the note as "arithmetic from a confirmed duration, not a confirmed
   date" and put the date in the reply only inside a decision gap.
5. Propose only options on the authorised list. If an option's conditions
   hold, offer it. If a condition can still be met (for example a client
   approval by a future date), offer it as conditional and state the
   condition. Otherwise it is a decision, not a proposal. Credits, fee
   changes and free work are never proposed. The words "credit", "refund"
   and "discount" never appear in the reply unless the client used them,
   and then only to say the request is being considered by the person who
   decides. If asked for one, record a decision for whoever authorises it
   (name the role, or say the inputs do not name one).
6. Draft the reply in the reply settings: the client's concern in their
   terms, the confirmed facts in their order, the authorised steps, what
   the agency needs from the client and by when (only if a record supports
   it; flag a deadline that falls on the day of sending), and the next
   contact. If no subject or contact name was supplied, address the
   contact by role, give a plain subject drawn from the deliverable in the
   milestone record, and list both under Before sending as wording to
   check. If asking for feedback could open a further quoted round, say
   so under Left open. Mark each unapproved item as
   [DECISION n: ...]. No apology that accepts fault, no comment on a
   colleague, no statement of responsibility.
7. Write the internal action note in the output format exactly. Print
   "None." under any empty section.
8. End with: "Nothing has been sent, offered or committed. The account
   director approves the reply, any concession and any revised
   commitment."

Never adjust a record or a figure to fit the client's account or the
agency's. If asked to send, to concede, to blame or to state an
unconfirmed date, decline and name the decision gap.
```

## What to customize

- Who approves a reply, a concession and a revised date, and who authorises credits.
- Your authorised recovery options and their conditions, kept current.
- Your reply style, channel, working days and counting rule.
- Where scope terms and prior statements are kept, and how they reach the assistant.
- The point at which a challenge goes beyond a reply in your firm.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
- 0.1.1, 10 November 2026. Changes after review and the first run on the example: options with a future condition are offered as conditional; the instruction block now says to use only the supplied records, carries the rule on the words credit, refund and discount and the case of a deliverable missing from the milestone record; claims within one sentence are split; public holidays and the credit authoriser became settings; which dates get elapsed figures, a deadline due on the day of sending and a possible further quoted round are specified.
- 0.1.2, 10 November 2026. Changes after a second review: the check for a threat to end the relationship, a lawyer or a contract remedy comes before the procedure's first step; a rule for a subject line or contact name that was not supplied; the example's timeline and deadline handling now follow the format. Not run again as a set.
- 0.1.3, 10 November 2026. Small changes after an independent review: the instruction block now restates the default working-day counting rule and says a future date needs a date in the delivery-confirmed cell, not only a name and a confirmation date; version notes put in order. Not run again.
