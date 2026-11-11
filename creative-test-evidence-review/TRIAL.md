# Creative test evidence review: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (Client A, Agency X, the October pan range: eight creatives, the conversion definitions and the three-line change log, with the default settings). No client data was used. The assistant followed the fenced instruction block and the output format in `member/template.md` and had no access to any ad account.

This is the third run on the same day. The first run, on the earlier wording, flagged that the change log's scope named an ad set and an event the export could not resolve, and that several formatting rules were open. The template was then revised (scopes are now creative IDs only, with a stop rule; a finished run's needs are written as a re-run; one-line roll-up for an event with no readable creative; "Vary: none" allowed; a gap equal to the threshold is directional) and the example's change log was rewritten with creative-ID scopes. A review then asked for small changes to the instruction block (the missing change log case, the personal-data stop, the return-on-spend decline, the budget or bid note on a pair, the shared-change note, the one-attribute option when there is no clean pair, the heading and "Change log not supplied." rules, a tracking entry applying to the creatives its scope names, settings written without brackets, no gap figure for creatives that are not a clean pair, and "Hold the same: not applicable" for a check). Because the block and the example's learning and option 4 changed, the template was run on the example again. This record replaces the second and is of the run on the final wording.

Two caveats about how blind the trial was, both unchanged and made worse by the third run. The file holding the example's inputs also holds its published output, and both were displayed together when it was opened, so the output was seen before the trial output was written. The same session also made the revisions and then ran the template, so it knew what the new rules were meant to produce. A blind re-run by a session that has seen neither the published output nor the revisions would be stronger evidence and has not been done. The trial output below was still worked out from the inputs and the rules, row by row, and not pasted; where it matches the published example, the figures recompute from the inputs.

## What came out

```
CREATIVE TEST EVIDENCE REVIEW: October pan range

For: Creative strategist and media lead. Batch ran 5 October 2026 to 18 October 2026; export as of 20 October 2026. 8 creatives, spend $6,520.00. Extra columns ignored: none.

Conversion definitions used:
- Purchase: a paid order on the store, 7-day click. Confirmed: yes, checked against store order records matched on 19 October.
- Quiz completed: a shopper finishes the product-finder quiz, 7-day click. Confirmed: no, no second record.

Change log for the period:
- 9 October, tracking, C-07 and C-08: quiz-completed tag added to the quiz page. Treatment: conversions unconfirmed: C-07, C-08.
- 12 October, offer, C-05 and C-06: 10% launch discount added to the two Gift giving creatives only. Treatment: held back: C-05. C-06 ended on 7 October, before the change, so it is not touched.
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
- C-01 cost less per purchase than C-04 ($25.00 against $30.65). C-01's daily budget doubled on 14 October. The two differ in angle, format and hook at once and are not a clean pair, so the difference cannot be put down to any one of them and no gap is given.
- Nothing can be said about Gift giving, the Carousel format, the Number in headline, Close-up first frame or Price in first card hooks, or the quiz-completion creatives, because every creative that carries them is held back.

Next-test options (options only, none chosen):
1. Do Time saved and Craftsmanship cost the same per purchase in a video? Vary: angle (Craftsmanship against Time saved). Hold the same: Video 15s format, Question opener hook, dates, budget and offer. First: a Craftsmanship video with a question opener has to be made and run alongside C-01, or C-01 re-run beside it.
2. Does format matter for the Craftsmanship customer-quote creative? Vary: format (Video 15s against Static). Hold the same: Craftsmanship angle, Customer quote hook, Purchase event, dates, budget and offer. First: a Video 15s version of C-04 has to be made and run alongside it.
3. Can the Gift giving angle be read at all? Vary: none; this is a clean re-run. Hold the same: one offer across Gift giving and at least one other angle. First: a person decides whether the 10% launch discount applies to every creative or to none.
4. Can the quiz completions be trusted? Vary: none; this is a check. Hold the same: not applicable. First: someone matches the quiz completions to a second record. C-07 and C-08 already exceed the 30-conversion minimum, with 64 and 41, but their tag went live on 9 October, inside the run, so they could be readable only on a re-run with the tag live throughout and the completions matched to a second record.

Questions for you:
1. Did the 14 October budget increase on C-01 also change its audience or placements?
2. Is the 10% launch discount for Gift giving meant to continue? If it is, Gift giving can only be compared with creatives that carry it too.
3. Who can match the quiz completions to a second record, and by when?

Every figure was calculated from the export, conversion definitions and change log supplied, using simple division and addition on the rows given. No winner or loser is named, nothing has been changed in any ad account, and what to test next is yours to decide.
```

## What was observed

- **Every required part was produced.** All headings in the format were printed, and no stop condition was triggered: the headers matched, each creative appeared once, both events had a definition, every change-log scope was creative IDs that appear in the export, dates and numbers were valid, clicks did not exceed impressions, and there was no personal data.
- **The figures match the acceptance test for this batch.** C-01 and C-04 readable; C-02, C-03 and C-06 thin; C-05 held back for offer and size; C-07 and C-08 unconfirmed; readable spend $2,150.00 of $6,520.00 (33.0%); no clean pair. The costs per conversion and the batch line (159 purchases on $4,970.00, 105 quiz completions on $1,550.00) recompute from the inputs.
- **Differences from the published example.** The substance is the same. The differences are wording only: the trial phrases the C-06 note, the second sentence of the learning's first line and option 1 a little differently. Neither output contains a figure that is not in the inputs.
- **Points from the first run that this run settled.** No guess about ad set membership was needed, because the scopes name C-05, C-06, C-07 and C-08. The "Needs" lines for finished runs read as re-runs. The quiz roll-up is one line, and Number in headline names only C-02 under Purchase, because creatives of another event are not named. "Vary: none" is allowed for options 3 and 4. The table heading carries the creative count. Option 4, a check, now reads "Hold the same: not applicable", so every option carries that element. The learning no longer prints a gap figure for C-01 and C-04, which are not a clean pair.
- **Still open or not exercised.**
  - Step 2 makes conversions unconfirmed whenever a tracking entry falls inside a run, so matching quiz completions to a second record would not by itself make C-07 and C-08 readable for this run. The "Needs" text says a re-run with the tag live throughout, which follows from the rule.
  - Table padding and the bracketed settings, both noted in earlier runs, were addressed in the template (cells are separated by " | " and padding is optional; the instruction block names the settings without brackets). This run used the defaults, so it does not show how a person's own settings are entered.
- **Shortcomings of this trial.** It was a single run on one invented batch, by the same product that is named on the template. It exercised the happy path plus the offer, thin and unconfirmed rules. It did not exercise the stop conditions (including the unresolvable-scope and personal-data stops), the declines (winner, return on spend, lowering a minimum), the shared-change case, the missing change log case, the clean pair arithmetic or the exact-threshold gap; acceptance tests 2 to 12 were not run.
