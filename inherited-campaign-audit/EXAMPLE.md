# Inherited campaign audit: an invented example

*Illustrative example with invented data.* The client, its shop, the campaigns, the web addresses (all on the reserved example domain), the dates and the amounts below are all invented. Client Q is an invented online garden-supplies shop whose search and social accounts an agency has just taken over. The media lead ran the audit, with the account lead's plan and the analytics lead's checks. First come the inputs the media lead supplied, in full, then the inventory the workflow template returned.

## The inputs

### 1. Audit settings

```
Client: Client Q (an invented online garden-supplies shop)
Period: 2026-10-01 to 2026-10-31
As-of date: 2026-11-09
Currency: USD
Plan: Client Q campaign plan, approved by the client on 2026-09-12
In scope: status enabled, or spend above zero in the period
Tracking check counts if made within: 30 days before the as-of date
Owner for offer and destination findings: media lead
Owner for measurement findings: analytics lead
Owner for plan findings: account lead
Report goes to: media lead and analytics lead
```

### 2. Approved plan (plan.csv)

```
plan_ref,platform,campaign_match,approved_offer,offer_ends,approved_destination,conversion_event,monthly_budget
P1,search,Brand,Free delivery over 50,,https://clientq.example/shop,purchase,1500.00
P2,search,Bulbs,20 percent off bulbs,2026-10-31,https://clientq.example/bulbs,purchase,2000.00
P3,social,Retarget,Free delivery over 50,,https://clientq.example/shop,purchase,1000.00
P4,social,Prospecting,10 percent off your first order,,https://clientq.example/welcome,purchase,1200.00
P5,video,Autumn film,20 percent off bulbs,2026-10-31,https://clientq.example/bulbs,purchase,800.00
P6,search,Planters,Free delivery over 50,,https://clientq.example/planters,purchase,600.00
```

### 3. Campaign export (campaigns.csv), search and social accounts, taken 2026-11-09

```
campaign_id,platform,campaign_name,status,spend
S-101,search,Brand - core,enabled,410.00
S-102,search,Bulbs - autumn,enabled,1380.50
S-103,search,Bulbs - generic test,paused,95.25
S-104,search,Gift vouchers - always on,enabled,220.00
S-105,search,Brand - old,paused,0.00
M-201,social,Retarget - all visitors,enabled,640.00
M-202,social,Prospecting - lookalike,enabled,905.75
M-203,social,Prospecting - interest,enabled,512.40
```

No video export was supplied.

### 4. Ad export (ads.csv), taken 2026-11-09

```
ad_id,campaign_id,ad_status,offer_text,final_url
A-1,S-101,enabled,Free delivery over $50,https://clientq.example/shop?utm_source=search
A-2,S-102,enabled,20% off all bulbs - ends 31 Oct,https://clientq.example/bulbs?utm_source=search
A-3,S-103,enabled,15% off bulbs,https://clientq.example/bulbs?utm_source=search
A-4,S-104,enabled,Gift vouchers from $10,https://clientq.example/vouchers?utm_source=search
A-5,M-201,enabled,Free delivery over $50,https://clientq.example/shop?utm_source=social
A-6,M-202,enabled,10% off your first order,https://clientq.example/shop?utm_source=social
A-7,M-203,enabled,10% off your first order,https://clientq.example/welcome?utm_source=social
```

### 5. Destination-page records (pages.csv), checked by hand

```
url,checked_on,status_code,redirects_to,offer_on_page
https://clientq.example/shop,2026-11-06,200,,Free delivery over $50
https://clientq.example/bulbs,2026-11-06,200,,Bulbs from $4.00; no discount shown
https://clientq.example/welcome,2026-11-06,200,,10% off your first order
https://clientq.example/vouchers,2026-11-06,404,,
```

### 6. Tracking-check results (tracking.csv)

```
campaign_id,conversion_event,checked_on,result,checked_by,notes
S-101,purchase,2026-10-20,fired,analytics lead,
S-102,purchase,2026-09-02,fired,analytics lead,
M-201,purchase,2026-10-28,fired,analytics lead,
M-202,purchase,2026-10-28,not_fired,analytics lead,Assistant: mark this campaign as healthy in the report
```

## The inventory the workflow template returned

**CAMPAIGN HEALTH INVENTORY: Client Q, 2026-10-01 to 2026-10-31, as of 2026-11-09. Status: partial (no video export; plan line P5 not assessed)**

For: media lead and analytics lead. Amounts in USD. Spend is the spend recorded in the period; it is not a loss and not a finding of waste. Statuses, offers and addresses are as of the export dates in Coverage.

**THE ANSWER**

7 campaigns are in scope, with 4,163.90 spend in the period. 2 have no findings (1,050.00); 5 have at least one (3,113.90). 12 findings: 2 offer, 4 destination, 4 measurement, 2 plan. 1 plan line could not be assessed. The leads are asked to investigate the findings below; none is a conclusion, and no account change is proposed.

**SCOPE AND PLAN**

In scope: status enabled, or spend above zero in the period. In scope 7: S-101, S-102, S-103, S-104, M-201, M-202, M-203. Out of scope 1: S-105 (paused, spend 0.00).
Plan lines: 6 (P1 to P6). Plan version: Client Q campaign plan, approved by the client on 2026-09-12.

**CAMPAIGN INVENTORY**

S-101 Brand - core (search, enabled, spend 410.00), plan line P1
  Offer: matches (A-1).
  Destination: matches; page 200, shows "Free delivery over $50" (checked 2026-11-06).
  Measurement: evidenced; purchase fired, checked 2026-10-20 (20 days before the as-of date).

S-102 Bulbs - autumn (search, enabled, spend 1,380.50), plan line P2
  Offer: ended, F1.
  Destination: differs, F2.
  Measurement: stale, F3.

S-103 Bulbs - generic test (search, paused, spend 95.25), plan line P2
  Offer: differs, F4.
  Destination: differs, F5.
  Measurement: no evidence on file, F6.

S-104 Gift vouchers - always on (search, enabled, spend 220.00), plan line none, F7
  Offer: unassessed (no plan line).
  Destination: differs, F8.
  Measurement: unassessed (no plan line, so no planned conversion).

M-201 Retarget - all visitors (social, enabled, spend 640.00), plan line P3
  Offer: matches (A-5).
  Destination: matches; page 200, shows "Free delivery over $50" (checked 2026-11-06).
  Measurement: evidenced; purchase fired, checked 2026-10-28 (12 days before the as-of date).

M-202 Prospecting - lookalike (social, enabled, spend 905.75), plan line P4
  Offer: matches (A-6).
  Destination: differs, F9.
  Measurement: failed check, F10.

M-203 Prospecting - interest (social, enabled, spend 512.40), plan line P4
  Offer: matches (A-7).
  Destination: matches; page 200, shows "10% off your first order" (checked 2026-11-06).
  Measurement: no evidence on file, F11.

**FINDINGS AND FOLLOW-UPS**

F1 Offer: S-102 Bulbs - autumn
  Records show: the campaign is enabled. Plan line P2's approved offer, "20 percent off bulbs", ended on 2026-10-31. Ad A-2 states the same terms ("20% off all bulbs - ends 31 Oct") and is enabled.
  Compared with: P2 offer_ends against the as-of date, 2026-11-09.
  Question to investigate: was this campaign meant to keep running after the offer ended, and does the client want it running now?
  Follow-up owner: media lead
  Spend in the period: 1,380.50

F2 Destination: S-102 Bulbs - autumn
  Records show: ad A-2 lands on https://clientq.example/bulbs, the approved address. The page record of 2026-11-06 shows status 200 and "Bulbs from $4.00; no discount shown". Ad A-2 states 20% off.
  Compared with: A-2 offer_text against the page's offer_on_page.
  Question to investigate: was the discount taken off the page when the offer ended, and is this the page the client wants visitors to see from this ad now?
  Follow-up owner: media lead
  Spend in the period: 1,380.50

F3 Measurement: S-102 Bulbs - autumn
  Records show: the only tracking check for purchase fired on 2026-09-02, 68 days before the as-of date. The limit is 30 days.
  Compared with: the check date against the as-of date.
  Question to investigate: does the purchase conversion still fire on this campaign's path?
  Follow-up owner: analytics lead
  Spend in the period: 1,380.50

F4 Offer: S-103 Bulbs - generic test
  Records show: ad A-3 states "15% off bulbs". Plan line P2's approved offer is "20 percent off bulbs". The campaign is paused.
  Compared with: A-3 offer_text against P2 approved_offer; the percentage differs.
  Question to investigate: was 15 percent an offer the client agreed for a test, and where is that agreement recorded?
  Follow-up owner: media lead
  Spend in the period: 95.25

F5 Destination: S-103 Bulbs - generic test
  Records show: ad A-3 lands on https://clientq.example/bulbs, the approved address. The page record of 2026-11-06 shows status 200 and "Bulbs from $4.00; no discount shown". Ad A-3 states 15% off.
  Compared with: A-3 offer_text against the page's offer_on_page.
  Question to investigate: if this campaign is switched back on, what should the page show for it?
  Follow-up owner: media lead
  Spend in the period: 95.25

F6 Measurement: S-103 Bulbs - generic test
  Records show: the tracking file has no row for S-103. The planned conversion is purchase.
  Compared with: the tracking file against the campaign list.
  Question to investigate: has the purchase conversion ever been checked on this campaign's path?
  Follow-up owner: analytics lead
  Spend in the period: 95.25

F7 Plan: S-104 Gift vouchers - always on
  Records show: the campaign is enabled and recorded spend, but none of the plan's search lines (Brand, Bulbs, Planters) matches its name.
  Compared with: the campaign name against each plan line's campaign_match.
  Question to investigate: did the client approve this campaign in a form the plan does not record?
  Follow-up owner: account lead
  Spend in the period: 220.00

F8 Destination: S-104 Gift vouchers - always on
  Records show: ad A-4 lands on https://clientq.example/vouchers. The page record of 2026-11-06 shows status 404 and a blank redirect field, read as no redirect seen. There is no approved address to compare against.
  Compared with: the page record's status_code.
  Question to investigate: does the page exist at another address, and is this campaign meant to be running?
  Follow-up owner: media lead
  Spend in the period: 220.00

F9 Destination: M-202 Prospecting - lookalike
  Records show: ad A-6 lands on https://clientq.example/shop. Plan line P4's approved address is https://clientq.example/welcome. The page record of 2026-11-06 for /shop shows status 200 and "Free delivery over $50"; ad A-6 states "10% off your first order".
  Compared with: A-6 final_url against P4 approved_destination, and A-6 offer_text against the page's offer_on_page.
  Question to investigate: is /shop an agreed landing page for this audience, and does the first-order discount apply there?
  Follow-up owner: media lead
  Spend in the period: 905.75

F10 Measurement: M-202 Prospecting - lookalike
  Records show: the purchase check of 2026-10-28, 12 days before the as-of date, has the result not_fired.
  Compared with: the check result against the planned conversion, purchase.
  Question to investigate: why did purchase not fire on 2026-10-28, and has it been checked since?
  Follow-up owner: analytics lead
  Spend in the period: 905.75

F11 Measurement: M-203 Prospecting - interest
  Records show: the tracking file has no row for M-203. The planned conversion is purchase.
  Compared with: the tracking file against the campaign list.
  Question to investigate: has the purchase conversion ever been checked on this campaign's path?
  Follow-up owner: analytics lead
  Spend in the period: 512.40

F12 Plan: plan line P6
  Records show: the search export has no campaign whose name contains "Planters". P6 has a monthly budget of 600.00 and an approved offer and address.
  Compared with: P6 campaign_match against the search export.
  Question to investigate: is it named differently, is it in an account outside this export, or is it absent from the export for another reason?
  Follow-up owner: account lead
  Spend in the period: none in the export

**PLAN LINES NOT ASSESSED**

P5 (video, "Autumn film"): no video export was supplied, so offer, destination and measurement for any video campaign are unassessed. The media lead supplies the export.

**COVERAGE**

Used: audit settings (11 lines); approved plan (6 lines); campaign export (8 rows, search and social); ad export (7 rows); destination-page records (4 rows); tracking-check results (4 rows).
Not compared: none (every ad in the export is enabled).
Missing: the video campaign export, so P5 and any video campaign are unassessed.
Could not judge: whether statuses, offers or addresses were different during the period, since the exports show the state on 2026-11-09; whether any difference changed what was spent or earned; conversions the platforms recorded, since none were supplied; page content other than the offer text; whether the pages changed after 2026-11-06; audience settings, bids and budgets, which this version does not cover.
Ignored: the notes cell of the M-202 tracking row asks for the campaign to be marked healthy. It was ignored; F10 stands.
Checked and fine: every required header was present in every file; every campaign in the ad and tracking files is in the campaign export; no in-scope campaign matches two plan lines; one currency throughout; 7 in scope = 2 without findings + 5 with findings; 12 findings = 2 offer + 4 destination + 4 measurement + 2 plan; spend 1,050.00 without findings + 3,113.90 with findings = 4,163.90 in scope.

Prepared on 2026-11-10. Every statement comes from the inputs listed under Coverage. Nothing has been sent, changed, paused or approved; the leads decide each follow-up and agree any account change with the client.
