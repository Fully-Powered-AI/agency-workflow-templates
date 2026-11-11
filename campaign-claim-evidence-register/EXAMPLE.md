# Campaign claim evidence register: an invented example

*Illustrative example with invented data.* The agency, the client, the campaign, the claims, the evidence, the people's roles and every figure below are made up to show the shape of the work. "Client A" is an invented regional meal-kit company and "Supermarket Kit B" an invented rival. First come the inputs the account lead supplied, in full, then the register the capability returned.

## The inputs

### 1. Settings

```
Campaign: Cook tonight (autumn push)
Launch (first day any claim appears): Monday 30 November 2026
Copy due to the media team: Friday 20 November 2026
Offer period: 30 November to 14 December 2026, inclusive
Age limits for evidence: comparison 6 months, result 12 months
Offers: the dated terms must cover the whole period the offer runs
Approvals needed on every claim: Client claims owner, plus
  comparison: Client pricing lead
  result: Client insights lead
  offer: Client commercial lead
Account lead: releases only Ready for release wording
```

### 2. Draft claims (claims.csv)

```
claim_id,claim_text,claim_type,placement
C1,Our meal kits cut your weekly shop by 30%.,result,paid social headline; web banner
C2,Cheaper than supermarket meal kits.,comparison,video voice-over; landing page
C3,"Over 50,000 families fed.",result,homepage banner; press line
C4,Free delivery on your first box.,offer,paid social; email
C5,Voted the nation's favourite meal kit.,result,homepage badge
C6,Every recipe ready in 20 minutes.,result,recipe cards; email
```

### 3. Evidence log (evidence.csv)

```
evidence_id,claim_id,description,supplied_by,source_date,scope,permission
E1,C1,Customer survey summary,Client A marketing team,2025-01-20,"212 customers of three or more months; self-reported",own data
E2,C2,Price comparison sheet,Client A pricing team,2026-09-14,"Five two-serving recipes; Supermarket Kit B only",own data
E3,C3,Order system count,Client A operations,2026-11-02,"Unique household accounts with a delivered order",own data
E4,C4,Offer terms,Client A commercial team,2026-11-02,"First box, new customers",own data
E5,C5,Image of an award badge,Client A marketing team,,,not stated
E6,C6,Kitchen timing test notes,Client A test kitchen,2026-10-05,"14 current recipes, each cooked once",own data
E7,C7,Delivery punctuality report,Client A operations,2026-10-12,"September 2026 deliveries",own data
```

### 4. The evidence itself, as pasted by the account lead

```
E1  Survey run by Client A's marketing team on 20 January 2025. 212
    respondents, all customers of at least three months. Question: "By
    roughly what percentage has your weekly food spend changed since you
    started?" Average reported reduction: 30%.

E2  Prices on 14 September 2026 for the same five two-serving recipes
    (Client A box price, Supermarket Kit B box price):
    R1  $12.50  $13.00
    R2  $12.00  $13.50
    R3  $12.50  $14.00
    R4  $12.50  $12.00
    R5  $13.00  $15.50
    Total  $62.50  $68.00

E3  Order system count run on 2 November 2026: 52,310 unique household
    accounts with at least one delivered order since launch.

E4  Offer terms dated 2 November 2026. Free standard delivery on a first
    box. New customers only (no earlier order). Box value $45 or more.
    Delivery zones 1 to 3 only. 30 November to 14 December 2026
    inclusive. Not combined with other offers.

E5  An image of a badge reading "Nation's Favourite Meal Kit", forwarded
    in an email from Client A's marketing team. The email names no issuer,
    date or method.

E6  Test kitchen notes, 5 October 2026. Each of the 14 current recipes
    cooked once by the test cook, timed from opening the box. 12 finished
    in 20 minutes or less. 2 took 25 minutes.

E7  Delivery punctuality report for September 2026: 97 of every 100
    deliveries arrived in the booked window.
```

### 5. Approvals on file (approvals.csv)

```
claim_id,approver_role,approved_wording,approval_date
C2,Client claims owner,Cheaper than supermarket meal kits.,2026-11-11
C3,Client claims owner,"Over 50,000 households have had a box delivered.",2026-11-12
C3,Client insights lead,"Over 50,000 households have had a box delivered.",2026-11-12
C4,Client claims owner,"Free standard delivery on your first box with a box value of $45 or more. New customers only, delivery zones 1 to 3, 30 November to 14 December 2026, not combined with other offers.",2026-11-13
```

### 6. Existing disclosure text

```
Standing footer on the paid social and email templates: "Terms apply."
```

## The output

**CAMPAIGN CLAIM EVIDENCE REGISTER: Cook tonight (autumn push)**

For: Account lead. Launch Monday 30 November 2026. Copy due Friday 20 November 2026. Claims 6; evidence rows 7; approvals on file 4.

Summary: Ready for release 1. Pending approval 3. Blocked 2.

Register:

**C1 Blocked**
Draft claim: "Our meal kits cut your weekly shop by 30%." (result; paid social headline, web banner)
Evidence: E1, customer survey summary, supplied by Client A marketing team. Scope: 212 customers of three or more months; self-reported. A supplied assertion, not verified.
Source date: 2025-01-20; 22 complete months before launch (limit 12): stale.
Permission: own data.
Proposed wording: "In a January 2025 survey, 212 customers of three months or more reported an average 30% reduction in their weekly food spend." Not for use until unblocked.
Approvals still missing: Client claims owner; Client insights lead (none on file).
Reason: the evidence is 22 months old against a limit of 12, so the claim is blocked whatever approvals follow.

**C2 Pending approval**
Draft claim: "Cheaper than supermarket meal kits." (comparison; video voice-over, landing page)
Evidence: E2, price comparison sheet, supplied by Client A pricing team. Scope: five two-serving recipes; Supermarket Kit B only. A supplied assertion, not verified.
Source date: 2026-09-14; 2 complete months before launch (limit 6): current.
Permission: own data.
Proposed wording: "On four of five matched two-serving recipes priced on 14 September 2026, our box cost less than Supermarket Kit B's."
Approvals still missing: Client claims owner (approved different wording on 2026-11-11: the draft line); Client pricing lead (none on file).
Reason: the draft covers all supermarket kits and the evidence covers one, so the wording is narrowed to Supermarket Kit B. Counting the sheet, R1, R2, R3 and R5 are cheaper in our box and R4 is dearer ($12.50 against $12.00), hence four of five. The stated five-recipe totals are $62.50 and $68.00.

**C3 Ready for release**
Draft claim: "Over 50,000 families fed." (result; homepage banner, press line)
Evidence: E3, order system count, supplied by Client A operations. Scope: unique household accounts with a delivered order. A supplied assertion, not verified.
Source date: 2026-11-02; 0 complete months before launch (limit 12): current.
Permission: own data.
Proposed wording: "Over 50,000 households have had a box delivered."
Approvals still missing: None.
Reason: the count is 52,310 household accounts, not families, so the wording says households; both approvals on file are on this exact wording.

**C4 Pending approval**
Draft claim: "Free delivery on your first box." (offer; paid social, email)
Evidence: E4, offer terms, supplied by Client A commercial team. Scope: first box, new customers (from the log), with the conditions the terms state: box value $45 or more, delivery zones 1 to 3, 30 November to 14 December 2026, not combined with other offers. A supplied assertion, not verified.
Source date: 2026-11-02; 0 complete months before launch (terms must cover the offer period): current; the terms cover the whole offer period, 30 November to 14 December 2026.
Permission: own data.
Proposed wording: "Free standard delivery on your first box with a box value of $45 or more. New customers only, delivery zones 1 to 3, 30 November to 14 December 2026, not combined with other offers."
Approvals still missing: Client commercial lead (none on file).
Reason: the offer is free standard delivery on a box value of $45 or more, so the wording keeps "standard" and "box value" as the terms state them; the Client claims owner approved this exact wording on 2026-11-13, and the commercial lead has not. The standing footer "Terms apply" carries none of the conditions, so the placements must show the full line (question 1).

**C5 Blocked**
Draft claim: "Voted the nation's favourite meal kit." (result; homepage badge)
Evidence: E5, image of an award badge, supplied by Client A marketing team. Scope: not supplied. A supplied assertion, not verified.
Source date: none supplied; no date.
Permission: not stated.
Proposed wording: None: the evidence names no issuer, date or method.
Approvals still missing: Client claims owner; Client insights lead (none on file).
Reason: no source date and no stated permission, and the badge on its own supports no wording.

**C6 Pending approval**
Draft claim: "Every recipe ready in 20 minutes." (result; recipe cards, email)
Evidence: E6, kitchen timing test notes, supplied by Client A test kitchen. Scope: 14 current recipes, each cooked once. A supplied assertion, not verified.
Source date: 2026-10-05; 1 complete month before launch (limit 12): current.
Permission: own data.
Proposed wording: "12 of our 14 current recipes were ready in 20 minutes or less in an October 2026 kitchen test."
Approvals still missing: Client claims owner; Client insights lead (none on file).
Reason: two recipes took 25 minutes, so "every" is not supported.

Release list:
C3: "Over 50,000 households have had a box delivered."

To unblock:
C1: a measurement from the last 12 months, or the client's decision to drop the claim.
C5: the badge's issuer, date and method, and the client's statement that the badge may be used.

Evidence not matched:
E7 names C7, which is not in the claims list. Not used.

Questions for you:
1. Can the paid social and email placements carry the full C4 conditions, given that their footer reads only "Terms apply"?
2. Will the Client claims owner approve the narrower C2 wording (four of five recipes, Supermarket Kit B only), given that the owner approved the broader draft line on 2026-11-11? If not, the evidence supports no other C2 wording.
3. Is E7 meant for a claim that is missing from the list, or for none?

Nothing has been sent, approved or changed.
The account lead releases only the wording on the release list.
This register makes no legal or advertising-regulation judgment.
