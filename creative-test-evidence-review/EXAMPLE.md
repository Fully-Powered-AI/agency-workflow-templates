# Creative test evidence review: an invented example

*Illustrative example with invented data.* Client A is an invented online seller of kitchenware, and Agency X is its invented agency. The batch is eight creatives for one pan range, reviewed by the agency's creative strategist and media lead. Nothing here describes a real account or a real result.

## What the person supplies

**Batch:** October pan range. Export dated 20 October 2026. Settings: the defaults (30 conversions, 1,000 impressions, a gap threshold of 20 per cent of the lower cost).

**Creative export** (headers as in the template, one row per creative):

```
creative_id | angle         | format    | hook                 | conversion_event | start_date | end_date   | spend   | impressions | clicks | conversions
C-01        | Time saved    | Video 15s | Question opener      | Purchase         | 2026-10-05 | 2026-10-18 | 1200.00 | 96000       | 1440   | 48
C-02        | Time saved    | Static    | Number in headline   | Purchase         | 2026-10-05 | 2026-10-18 | 900.00  | 81000       | 972    | 27
C-03        | Craftsmanship | Video 15s | Close-up first frame | Purchase         | 2026-10-05 | 2026-10-18 | 1100.00 | 88000       | 1100   | 22
C-04        | Craftsmanship | Static    | Customer quote       | Purchase         | 2026-10-05 | 2026-10-18 | 950.00  | 79000       | 790    | 31
C-05        | Gift giving   | Carousel  | Price in first card  | Purchase         | 2026-10-12 | 2026-10-18 | 700.00  | 52000       | 728    | 29
C-06        | Gift giving   | Video 15s | Question opener      | Purchase         | 2026-10-05 | 2026-10-07 | 120.00  | 9500        | 95     | 2
C-07        | Time saved    | Video 15s | Number in headline   | Quiz completed   | 2026-10-05 | 2026-10-18 | 800.00  | 70000       | 1050   | 64
C-08        | Craftsmanship | Static    | Number in headline   | Quiz completed   | 2026-10-05 | 2026-10-18 | 750.00  | 66000       | 825    | 41
```

**Conversion definitions:**

```
conversion_event | meaning                                 | window       | confirmed | checked_against
Purchase         | A paid order on the store               | 7-day click  | yes       | Store order records, matched on 19 October
Quiz completed   | A shopper finishes the product-finder quiz | 7-day click | no        | (none)
```

**Change log:**

```
date       | change_type | scope                | description
2026-10-09 | tracking    | C-07, C-08           | Quiz-completed tag added to the quiz page
2026-10-12 | offer       | C-05, C-06           | 10% launch discount added to the two Gift giving creatives only
2026-10-14 | budget      | C-01                 | Daily budget raised from $60 to $120
```

## What comes out

```
CREATIVE TEST EVIDENCE REVIEW: October pan range

For: Creative strategist and media lead. Batch ran 5 October 2026 to 18 October 2026; export as of 20 October 2026. 8 creatives, spend $6,520.00. Extra columns ignored: none.

Conversion definitions used:
- Purchase: a paid order on the store, 7-day click. Confirmed: yes, checked against store order records matched on 19 October.
- Quiz completed: a shopper finishes the product-finder quiz, 7-day click. Confirmed: no, no second record.

Change log for the period:
- 9 October, tracking, C-07 and C-08: quiz-completed tag added to the quiz page. Treatment: conversions unconfirmed: C-07, C-08.
- 12 October, offer, C-05 and C-06: 10% launch discount added to the two Gift giving creatives only. Treatment: held back: C-05. C-06 ended on 7 October, before the change.
- 14 October, budget, C-01: daily budget raised from $60 to $120. Treatment: noted only.

Evidence by creative, 8 creatives (cost per conversion is spend divided by conversions; creatives held back are left out of everything below this table):
ID   | Angle         | Format    | Hook                 | Event          | Ran                  | Spend     | Impressions | Clicks | Conversions | Cost per conversion | Status
C-01 | Time saved    | Video 15s | Question opener      | Purchase       | 5 Oct to 18 Oct      | $1,200.00 | 96,000      | 1,440  | 48          | $25.00              | Readable
C-02 | Time saved    | Static    | Number in headline   | Purchase       | 5 Oct to 18 Oct      | $900.00   | 81,000      | 972    | 27          | $33.33              | Held back
C-03 | Craftsmanship | Video 15s | Close-up first frame | Purchase       | 5 Oct to 18 Oct      | $1,100.00 | 88,000      | 1,100  | 22          | $50.00              | Held back
C-04 | Craftsmanship | Static    | Customer quote       | Purchase       | 5 Oct to 18 Oct      | $950.00   | 79,000      | 790    | 31          | $30.65              | Readable
C-05 | Gift giving   | Carousel  | Price in first card  | Purchase       | 12 Oct to 18 Oct     | $700.00   | 52,000      | 728    | 29          | $24.14              | Held back
C-06 | Gift giving   | Video 15s | Question opener      | Purchase       | 5 Oct to 7 Oct       | $120.00   | 9,500       | 95     | 2           | $60.00              | Held back
C-07 | Time saved    | Video 15s | Number in headline   | Quiz completed | 5 Oct to 18 Oct      | $800.00   | 70,000      | 1,050  | 64          | $12.50              | Held back
C-08 | Craftsmanship | Static    | Number in headline   | Quiz completed | 5 Oct to 18 Oct      | $750.00   | 66,000      | 825    | 41          | $18.29              | Held back
Batch: spend $6,520.00 on 8 creatives. Purchase: 159 conversions on $4,970.00. Quiz completed: 105 conversions on $1,550.00. Events are never added together.

Held back from comparison:
- C-02: thin, 27 conversions against a minimum of 30. Needs: a re-run under the same conditions that reaches 30 confirmed conversions.
- C-03: thin, 22 conversions against a minimum of 30. Needs: a re-run under the same conditions that reaches 30 confirmed conversions.
- C-05: offer changed (ran only under the 10% discount that no other running creative had); thin, 29 conversions against a minimum of 30. Needs: a re-run with every creative under the same offer that reaches 30 confirmed conversions.
- C-06: thin, 2 conversions against a minimum of 30. Needs: a re-run under the same conditions that reaches 30 confirmed conversions.
- C-07: conversions unconfirmed (Quiz completed is not confirmed and its tag went live on 9 October). Needs: a re-run with the tag live for the whole run and the quiz completions matched to a second record.
- C-08: conversions unconfirmed (same reason as C-07). Needs: the same.

Readable creatives: 2 of 8, $2,150.00 of $6,520.00 spend (33.0%).
By angle (Purchase): Time saved: 1 creative (C-01), spend $1,200.00, 48 conversions, $25.00 per conversion. Craftsmanship: 1 creative (C-04), spend $950.00, 31 conversions, $30.65 per conversion. Gift giving: no readable creative (C-05, C-06 held back).
By format (Purchase): Video 15s: 1 creative (C-01), spend $1,200.00, 48 conversions, $25.00 per conversion. Static: 1 creative (C-04), spend $950.00, 31 conversions, $30.65 per conversion. Carousel: no readable creative (C-05 held back).
By hook (Purchase): Question opener: 1 creative (C-01), spend $1,200.00, 48 conversions, $25.00 per conversion. Customer quote: 1 creative (C-04), spend $950.00, 31 conversions, $30.65 per conversion. Number in headline: no readable creative (C-02 held back). Close-up first frame: no readable creative (C-03 held back). Price in first card: no readable creative (C-05 held back).
Quiz completed: no readable creative (C-07, C-08 held back). Nothing to roll up.

Clean pairs:
- None. The only two readable creatives with the same event, C-01 and C-04, differ in angle, format and hook.

Tentative learning:
- C-01 cost less per purchase than C-04 ($25.00 against $30.65). C-01's daily budget doubled on 14 October. C-01 and C-04 differ in angle, format and hook at once and are not a clean pair, so the difference cannot be put down to any one of them and no gap is given.
- Nothing can be said yet about Gift giving, the Carousel format, the Number in headline, Close-up first frame or Price in first card hooks, or the quiz-completion creatives, because every creative that carries them is held back.

Next-test options (options only, none chosen):
1. Does the Time saved angle cost less per purchase than Craftsmanship when everything else is the same? Vary: angle. Hold the same: Video 15s format, Question opener hook, dates, budget and offer. First: a Craftsmanship video with a question opener has to be made and run alongside C-01.
2. Does format matter for the Craftsmanship customer-quote creative? Vary: format (Video 15s against Static). Hold the same: Craftsmanship angle, Customer quote hook, Purchase event, dates, budget and offer. First: a Video 15s version of C-04 has to be made and run alongside it.
3. Can the Gift giving angle be read at all? Vary: none; this is a clean re-run. Hold the same: one offer across Gift giving and at least one other angle. First: a person decides whether the 10% launch discount applies to every creative or to none.
4. Can the quiz completions be trusted? Vary: none; this is a check. Hold the same: not applicable. First: someone matches the quiz completions to a second record. C-07 and C-08 already exceed the 30-conversion minimum, with 64 and 41, but their tag went live on 9 October, inside the run, so they could be readable only on a re-run with the tag live throughout and the completions matched to a second record.

Questions for you:
1. Did the 14 October budget increase on C-01 also change its audience or placements?
2. Is the 10% launch discount for Gift giving meant to continue? If it is, Gift giving can only be compared with creatives that carry it too.
3. Who can match the quiz completions to a second record, and by when?

Every figure was calculated from the export, conversion definitions and change log supplied, using simple division and addition on the rows given. No winner or loser is named, nothing has been changed in any ad account, and what to test next is yours to decide.
```
