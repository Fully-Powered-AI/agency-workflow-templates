# Inherited campaign audit: trial on the invented example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5), run as a coding-agent session that read the template and followed its instruction block.

Date: 2026-11-10

The inputs were the invented example in `public/example.md` (Client Q, an invented garden-supplies shop). No client data was used.

## Inputs used

The six invented inputs from `public/example.md`: audit settings, approved plan (6 lines), campaign export (8 rows, search and social), ad export (7 rows), destination-page records (4 rows) and tracking-check results (4 rows). No video export was supplied. The block was followed with the template's output format.

## A limit on this trial

The trial was meant to read only the example's inputs before writing the output. The first read of the example file returned the whole file, including its published inventory, so the output below was written after the published inventory had been seen. It was still worked out from the template's rules and checked against the inputs (dates counted, spend added up), but it is not an independent blind run, and its likeness to the published example should not be taken as proof that the instructions alone would produce it.

## What came out

```
CAMPAIGN HEALTH INVENTORY: Client Q, 2026-10-01 to 2026-10-31, as of 2026-11-09. Status: partial (no video export; plan line P5 not assessed)

For: media lead and analytics lead. Amounts in USD. Spend is the spend recorded in the period; it is not a loss and not a finding of waste. Statuses, offers and addresses are as of the export dates in Coverage.

THE ANSWER
7 campaigns are in scope, with 4,163.90 spend in the period. 2 have no findings (1,050.00); 5 have at least one (3,113.90). 12 findings: 2 offer, 4 destination, 4 measurement, 2 plan. 1 plan line could not be assessed. The leads are asked to investigate the findings below; none is a conclusion, and no account change is proposed.

SCOPE AND PLAN
In scope: status enabled, or spend above zero in the period. In scope 7: S-101, S-102, S-103, S-104, M-201, M-202, M-203. Out of scope 1: S-105 (paused, spend 0.00).
Plan lines: 6 (P1 to P6). Plan version: Client Q campaign plan, approved by the client on 2026-09-12.

CAMPAIGN INVENTORY
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

FINDINGS AND FOLLOW-UPS
F1 Offer: S-102 Bulbs - autumn
  Records show: the campaign is enabled. Plan line P2 gives its approved offer ("20 percent off bulbs") an end date of 2026-10-31, before the as-of date. Ad A-2 ("20% off all bulbs - ends 31 Oct") is enabled.
  Compared with: P2 offer_ends against the as-of date 2026-11-09.
  Question to investigate: should this campaign still be running after the offer's end date?
  Follow-up owner: media lead
  Spend in the period: 1,380.50
F2 Destination: S-102 Bulbs - autumn
  Records show: ad A-2 goes to https://clientq.example/bulbs, the approved address. The page record (2026-11-06) shows 200 and "Bulbs from $4.00; no discount shown". A-2 says 20% off.
  Compared with: A-2 offer_text against the page record's offer_on_page.
  Question to investigate: does the page need to carry the discount while this ad runs, or should the ad change?
  Follow-up owner: media lead
  Spend in the period: 1,380.50
F3 Measurement: S-102 Bulbs - autumn
  Records show: the only purchase check fired on 2026-09-02, 68 days before the as-of date; the limit is 30 days.
  Compared with: the check date against the as-of date and the freshness limit.
  Question to investigate: does purchase still fire for this campaign?
  Follow-up owner: analytics lead
  Spend in the period: 1,380.50
F4 Offer: S-103 Bulbs - generic test
  Records show: enabled ad A-3 says "15% off bulbs"; P2's approved offer is "20 percent off bulbs". The campaign is paused.
  Compared with: A-3 offer_text against P2 approved_offer; the percentage differs.
  Question to investigate: was 15 percent agreed with the client for this test, and where is that recorded?
  Follow-up owner: media lead
  Spend in the period: 95.25
F5 Destination: S-103 Bulbs - generic test
  Records show: A-3 goes to https://clientq.example/bulbs, the approved address. The page record (2026-11-06) shows 200 and "Bulbs from $4.00; no discount shown". A-3 says 15% off.
  Compared with: A-3 offer_text against the page record's offer_on_page.
  Question to investigate: if this campaign runs again, what should the page show?
  Follow-up owner: media lead
  Spend in the period: 95.25
F6 Measurement: S-103 Bulbs - generic test
  Records show: the tracking file has no row for S-103. The planned conversion is purchase.
  Compared with: the tracking file against the campaign list.
  Question to investigate: has purchase ever been checked for this campaign?
  Follow-up owner: analytics lead
  Spend in the period: 95.25
F7 Plan: S-104 Gift vouchers - always on
  Records show: the campaign is enabled and has spend, but none of the search plan lines (Brand, Bulbs, Planters) appears in its name.
  Compared with: the campaign name against each campaign_match.
  Question to investigate: is there client approval for this campaign that the plan does not record?
  Follow-up owner: account lead
  Spend in the period: 220.00
F8 Destination: S-104 Gift vouchers - always on
  Records show: ad A-4 goes to https://clientq.example/vouchers. The page record (2026-11-06) shows status 404 and no redirect. With no plan line there is no approved address to compare.
  Compared with: the page record's status_code.
  Question to investigate: does this page exist at another address, and should the campaign be running?
  Follow-up owner: media lead
  Spend in the period: 220.00
F9 Destination: M-202 Prospecting - lookalike
  Records show: ad A-6 goes to https://clientq.example/shop; P4's approved address is https://clientq.example/welcome. The /shop page record (2026-11-06) shows 200 and "Free delivery over $50"; A-6 says "10% off your first order".
  Compared with: A-6 final_url against P4 approved_destination, and A-6 offer_text against the page record's offer_on_page.
  Question to investigate: is /shop an agreed landing page for this ad, and does the first-order discount apply there?
  Follow-up owner: media lead
  Spend in the period: 905.75
F10 Measurement: M-202 Prospecting - lookalike
  Records show: the purchase check of 2026-10-28 (12 days before the as-of date) has the result not_fired.
  Compared with: the check result against the planned conversion, purchase.
  Question to investigate: why did purchase not fire on 2026-10-28, and has it been checked since?
  Follow-up owner: analytics lead
  Spend in the period: 905.75
F11 Measurement: M-203 Prospecting - interest
  Records show: the tracking file has no row for M-203. The planned conversion is purchase.
  Compared with: the tracking file against the campaign list.
  Question to investigate: has purchase ever been checked for this campaign?
  Follow-up owner: analytics lead
  Spend in the period: 512.40
F12 Plan: plan line P6
  Records show: the search export holds no campaign whose name contains "Planters". P6 carries a monthly budget of 600.00.
  Compared with: P6 campaign_match against the search export.
  Question to investigate: is the campaign named differently, not yet created, or in an account outside this export?
  Follow-up owner: account lead
  Spend in the period: none in the export

PLAN LINES NOT ASSESSED
P5 (video, "Autumn film"): no video export was supplied, so offer, destination and measurement for any video campaign are unassessed; the media lead supplies the export.

COVERAGE
Used: audit settings (11 lines); approved plan (6 lines); campaign export (8 rows); ad export (7 rows); destination-page records (4 rows); tracking-check results (4 rows).
Missing: the video campaign export, so P5 and any video campaign are unassessed.
Could not judge: whether statuses, offers or addresses were different during the period (the exports show 2026-11-09); whether any difference changed what was spent or earned; conversions the platforms recorded; page content other than the offer text; whether pages changed after 2026-11-06; audience settings, bids and budgets.
Ignored: the notes cell of the M-202 tracking row (tracking-check results) asks for the campaign to be marked healthy; not followed, and F10 stands.
Checked and fine: every required header was present; every campaign in the ad and tracking files is in the campaign export; no in-scope campaign matches two plan lines; one currency; 7 in scope = 2 without findings + 5 with; 12 findings = 2 offer + 4 destination + 4 measurement + 2 plan; spend 1,050.00 + 3,113.90 = 4,163.90.

Prepared on 2026-11-10. Every statement comes from the inputs listed under Coverage. Nothing has been sent, changed, paused or approved; the leads decide each follow-up and agree any account change with the client.
```

## What was observed

- Every part of the output format was produced. Nothing in the inputs triggered a stop: all headers matched, one currency, as-of date after the period, no repeated campaign_id, no campaign matching two plan lines.
- The counts reconcile (7 in scope, 12 findings, 4,163.90 in spend), and the day counts were worked out from the dates (20, 68 and 12).
- The one instruction inside an input (the note on the M-202 tracking row) was listed as ignored and the finding stood.
- Comparison with the published example: the inventory, the 12 findings, their kinds, owners and spend figures agree. Differences are in wording only: shorter questions in several findings (F1, F2, F7, F8), the F1 record names the end date in the plan's own terms, and the Coverage "Checked and fine" line also states the spend sum. Because the published inventory had been seen first (see the limit above), agreement is weak evidence.
- Facts not in the inputs: none found in either output. Every figure and date traces to a file row.

Where the instructions were ambiguous and a guess was needed:

- The offer comparison treated "20% off all bulbs" as the same terms as "20 percent off bulbs". "All" arguably adds a term; the template does not say. It also treated the ad's "31 Oct" (no year) as 2026-10-31.
- A blank `redirects_to` on a 200 page was read as "no redirect". The template says a blank cell is unknown, never "none", so strictly the redirect part is unknown.
- It does not say that the page check (offer on the page against the ad's offer) uses the same terms comparison as the offer check; this was assumed.
- A paused campaign (S-103) with an enabled ad was compared on the ad's own status. The template does not say whether a paused campaign's ads should be compared; it does say the "ended" outcome needs an enabled campaign.
- The fenced instruction block refers to "the freshness limit" and the as-of date without the defaults (30 days, today) that the body of the template gives, so a run from the block alone, with settings that omit them, has no value to use.
- The block omits two rules the body states: ask once if the period, as-of date or currency is missing, and put an unclear offer pair in a question.
- Non-enabled ads are meant to be "counted under Coverage", but the output format has no place for that count. The example has no such ads, so it did not come up.
- Findings are "one per campaign per kind", but a destination finding can combine an address difference and an offer-on-page difference (F9); the question then has to cover both.

Nothing in the run was something the template told the assistant to stop for.
