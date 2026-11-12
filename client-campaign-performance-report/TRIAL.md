# Client campaign performance report: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Sonnet 5.5 (model ID claude-sonnet-5-5), which did not write the original template; the same session made the later revisions to the template and the example, so this is not a blind run
- **Date:** 2026-11-10
- **Template version:** 0.1.0

This is a record of one run of the workflow template on its own invented example. Client A, the platforms and every figure are invented, and no client data was used. It shows what the template produced once, on one set of inputs. It is not a test in any company's environment.

This is the second run on the same example. An earlier run the same day followed the template as first written and showed where it left room to guess: goal statuses, blank cells, spend added across platforms, the days used for clicks against sessions, whether a general note covers a flag, hypotheses about source differences, the placeholders, the prepared date and the currency symbol. The instruction block, the output format and the example were revised, and the run recorded here was made on the revised instructions with the revised example. The earlier run's record was replaced by this one. What the earlier run found, and what was changed, is at the end.

This run was made by the same session that revised the template and the example, so it had read the example's output before it began; it is not a blind run. The output below was written from the instruction block and the example's inputs, and its totals, ratios, changes and bounds were recomputed by script.

## Inputs used

The run settings, definitions, goals, notes, the Platform A, Platform B and analytics exports, and last week's totals, all as listed under "What the analyst supplies" in [example.md](example.md). Nothing else was added. The analyst's and account lead's names were not supplied, so the report uses their roles. Settings were the template's defaults (25% movement; a day at or above 1.5 times or at or below 0.5 times the average of the other days; default rounding).

## What came out

Every part of the output format was produced. The full output follows.

```
CLIENT PERFORMANCE REPORT: Client A, week of Monday 2 November 2026
DRAFT. Figures await the analyst's check. The narrative awaits the account lead's approval. Nothing has been sent.

For: the analyst and the account lead. Prepared 9 November 2026, from the Platform A export (6 rows), the Platform B export (7 rows), the analytics export (14 rows), the reporting definitions, the client goals, last week's report (totals only), the media buyer's notes (3) and the default format.
Window: Monday 2 November to Sunday 8 November 2026 (7 days). Compared with: Monday 26 October to Sunday 1 November 2026 (7 days), from last week's report.
Definitions: Platform A, completed purchases, 30-day click window. Platform B, completed purchases, 7-day click and 1-day view window. Analytics, transactions credited to the last non-direct click source. Currency USD. Ratios are built from summed figures. Changes are per-day averages over the days with data.

REPORTING WINDOW AND GAPS
Platform A: 6 of 7 days for every metric. Not available: Sunday 8 November. Per the notes, the saved date range on the export ended on 7 November. Shown as a gap, not zero.
Platform B: spend, impressions and clicks 7 of 7 days; conversions and conversion value 5 of 7 days. Not recorded: Wednesday 4 November and Thursday 5 November. Per the notes, conversion tracking was down on 4 and 5 November and fixed on 6 November. Shown as not recorded, not zero.
Analytics (search / cpc and social / paid): 7 of 7 days each. No gaps in the window.
Previous period: totals only, from last week's report.

SOURCE FIGURES
Platform A, platform-reported (30-day click; 6 of 7 days)
Spend $710.00 ($118.33 per day; previous $105.00; +12.7%). Impressions 34,900 (5,817 per day; previous 5,200; +11.9%). Clicks 1,404 (234.00 per day; previous 208.00; +12.5%).
Conversions 66 (11.00 per day; previous 10.00; +10.0%). Conversion value $7,770.00 ($1,295.00 per day; previous $1,150.00; +12.6%).
Click-through rate 4.02% (previous 4.00%; +0.02 points). Cost per click $0.506 (previous $0.505; +0.2%). Cost per conversion $10.76 (previous $10.50; +2.5%). Return on ad spend 10.94 (previous 10.95; -0.1%).

Platform B, platform-reported (7-day click and 1-day view; spend, impressions and clicks 7 of 7 days; conversions and value 5 of 7 days)
Spend $669.00 ($95.57 per day; previous $80.00; +19.5%). Impressions 163,800 (23,400 per day; previous 20,400; +14.7%). Clicks 2,387 (341.00 per day; previous 300.00; +13.7%).
Conversions 34 on 5 days (6.80 per day; previous 6.00; +13.3%). Conversion value $3,470.00 on 5 days ($694.00 per day; previous $600.00; +15.7%).
Click-through rate 1.46% (previous 1.47%; -0.01 points). Cost per click $0.280 (previous $0.267; +5.1%). Cost per conversion $14.79, built from the spend of the 5 days with conversions ($503.00) (previous $13.33; +11.0%). Return on ad spend 6.90, built from the same 5 days (previous 7.50; -8.0%).

Analytics, search / cpc (last non-direct click; 7 of 7 days)
Sessions 1,567 (223.86 per day; previous 210.00; +6.6%). Transactions 63 (9.00 per day; previous 8.57; +5.0%). Revenue $7,330.00 ($1,047.14 per day; previous $985.71; +6.2%).

Analytics, social / paid (last non-direct click; 7 of 7 days)
Sessions 2,139 (305.57 per day; previous 260.00; +17.5%). Transactions 31 (4.43 per day; previous 3.86; +14.8%). Revenue $3,160.00 ($451.43 per day; previous $385.71; +17.0%).

AGAINST CLIENT GOALS
Search return on ad spend of at least 8.00: 10.94 on 6 of 7 days (Platform A). Not calculable for the full window: Sunday 8 November is missing. Met on the 6 days available. Bound: with no conversion value on 8 November, the week falls below 8.00 only if that day's spend is above $261.25.
Social cost per conversion of at most $15.00: $14.79 on the 5 days with conversions recorded (Platform B). Not calculable for the full window: conversions are not recorded for 4 and 5 November. Met on the 5 days available, by $0.21. Bound: the week's $669.00 of spend stays within $15.00 a conversion only if those two days had at least 11 conversions between them; with none, it would be $19.68.
Total ad spend within $1,500.00 across both platforms: $1,379.00 on the days available ($710.00 Platform A, 6 days; $669.00 Platform B, 7 days). Not calculable for the full window: Sunday 8 November is missing for Platform A. Within the budget on the days available. Bound: the budget is exceeded if Platform A's spend on 8 November is above $121.00.

WHERE SOURCES DIFFER
Platform A and search / cpc, 6 days (2 to 7 November): platform-reported 66 conversions and $7,770.00; analytics 54 transactions and $6,320.00. Platform A is higher by 12 conversions (22.2% of the analytics figure) and $1,450.00 (22.9%). Clicks 1,404 against sessions 1,341: higher by 63 (4.7%). The windows differ (30-day click against last non-direct click). Not reconciled.
Platform B and social / paid, conversions and value on the 5 days both recorded (2, 3, 6, 7, 8 November): platform-reported 34 conversions and $3,470.00; analytics 22 transactions and $2,230.00. Platform B is higher by 12 (54.5%) and $1,240.00 (55.6%). Clicks against sessions on all 7 days, 2,387 against 2,139: higher by 248 (11.6%). The windows differ (7-day click and 1-day view against last non-direct click). Not reconciled.
On 4 and 5 November Platform B has no conversions recorded; analytics recorded 9 transactions and $930.00 of revenue on those two days. Shown as a separate fact, not used in place of the platform figures.
Hypothesis: the platforms' longer windows and view credit count purchases that analytics credits to another source. To confirm: compare analytics transactions credited to other sources on the same days. Who can check: the analyst.

ANOMALIES
1. Platform B, Friday 6 November, spend: $160.00, 1.89 times the $84.83 average of the other six days. The same day: Platform B clicks 520 (average of the others 311), conversions 11 and value $1,150.00; analytics social / paid sessions 470 (average of the others 278), transactions 7, revenue $760.00. No note covers it; the notes say only that nothing else was changed, which does not name this day.
Hypothesis 1: spend or bid settings changed on 6 November without a note. To confirm: the platform's change history for that day. Who can check: the media buyer.
Hypothesis 2: spend rose once conversion tracking was restored on 6 November. To confirm: the hourly spend on 6 November against the tracking fix time. Who can check: the media buyer.
No source-level movement of 25% or more. No other day outside the spend range.

DRAFT NARRATIVE (for the account lead's approval)
Platform-reported, Platform A spent $710.00 over six days, 12.7% more per day than last week, and reported 66 conversions worth $7,770.00, a return on ad spend of 10.94. Platform B spent $669.00 over seven days, 19.5% more per day, and reported 34 conversions worth $3,470.00 on the five days with tracking, a cost per conversion of $14.79 on those days. Analytics credited search / cpc with 63 transactions and social / paid with 31 over the seven days, up 5.0% and 14.8% per day.

All three goals are not calculable for the full window. On the days available the search return on ad spend is 10.94 against a goal of 8.00, the social cost per conversion is $14.79 against $15.00, and spend is $1,379.00 against $1,500.00. Platform A has no row for 8 November, and Platform B has no conversions recorded for 4 and 5 November; search stays at or above 8.00 unless 8 November spend is above $261.25 with no value, and social needs at least 11 conversions on 4 and 5 November to stay within $15.00.

Platform B's spend on 6 November was $160.00, 1.89 times the average of the other days, and no note covers it. The platforms report more conversions than analytics on the same days, by 22.2% for Platform A and 54.5% for Platform B, and their attribution windows differ from the analytics tool's.

DISCUSSION POINTS
1. Platform B spent $160.00 on 6 November, 1.89 times its usual day (Anomalies 1). What changed that day?
2. Platform B's conversions are not recorded for 4 and 5 November (Gaps). Can the platform supply them, or does the client accept the week as incomplete? The goal needs at least 11 conversions on those days.
3. Platform A is missing 8 November (Gaps). The spend and return goals cannot be confirmed until it is supplied.
4. Platform conversions are 22.2% and 54.5% above analytics on the same days (Where sources differ). Which source does the client treat as the number of record?

OPEN QUESTIONS
1. The Platform A row for 8 November, re-exported with the date range extended: from the media buyer or analyst.
2. Platform B conversions and conversion value for 4 and 5 November, if the platform can restore them: from the media buyer.
3. The cause of the 6 November spend on Platform B: from the media buyer.
4. Whether the goals are for the full week or may be reported on the days available: from the account lead.
5. Which source the client counts as the number of record: from the account lead.

FOR THE ANALYST TO VERIFY
Platform A totals: sum of 6 rows. Spend 120+118+125+130+122+95 = 710; per day 710/6. Previous per day = 735/7 = 105.00. Impressions 34,900; clicks 1,404; conversions 66; value 7,770.
Platform A ratios: click-through rate 1,404/34,900; cost per click 710/1,404; cost per conversion 710/66; return on ad spend 7,770/710. Previous: 1,456/36,400; 735/1,456; 735/70; 8,050/735.
Platform B totals: spend 669 over 7 rows; clicks 2,387; impressions 163,800; conversions 34 and value 3,470 over 5 rows. Spend on the 5 days with conversions (2, 3, 6, 7, 8 November) = 80+85+160+90+88 = 503. Cost per conversion 503/34; return on ad spend 3,470/503; click-through rate 2,387/163,800; cost per click 669/2,387. Previous: 560/42; 4,200/560; 2,100/142,800; 560/2,100.
Per-day changes: (current per day - previous per day) / previous per day, previous per day = previous total / 7. Click-through rate in points.
Analytics totals: search / cpc sessions 1,567, transactions 63, revenue 7,330; social / paid sessions 2,139, transactions 31, revenue 3,160; previous per day = previous total / 7.
Source differences: Platform A against search / cpc on 2 to 7 November (conversions 66 against 54; (66-54)/54 = 22.2%; value (7,770-6,320)/6,320 = 22.9%; clicks 1,404 against 1,341 sessions). Platform B against social / paid on 2, 3, 6, 7, 8 November (34 against 22 = 54.5%; 3,470 against 2,230 = 55.6%); clicks 2,387 against sessions 2,139 on 7 days.
Goals: spend 710+669 = 1,379; headroom 1,500-1,379 = 121. Return bound: (7,770 + V) / (710 + S) >= 8 requires V >= 8S - 2,090; with V = 0, S <= 261.25. Cost per conversion: 669 / 15 = 44.6, so at least 11 conversions beyond the 34; 669/34 = 19.68.
Spend swing: 160 / ((80+85+82+84+90+88)/6 = 84.83) = 1.89; clicks, sessions averages likewise.

Draft for the analyst's check and the account lead's approval. Nothing has been sent, posted or changed in any account.
```

## What was observed

The run needed no stop: the headers matched, no date fell outside the window, no figure was text, and no rows repeated. The blank conversion cells on 4 and 5 November were treated as not recorded, as the revised template says. Every section of the format was filled. Totals, ratios, per-day changes, source differences and bounds were recomputed by script and matched the example's figures.

Where this run differed from the example:

- Wording only: the example's narrative leads with search and social separately, this run's second paragraph leads with the three goals; the example gives two open questions, this run gives five (it adds the cause of the 6 November spend, whether goals may be reported on the days available, and the number of record).
- This run's anomaly entry adds analytics transactions and revenue for 6 November; the example adds Platform B's conversion average.
- Hypothesis wording differs slightly (this run's source-difference check is to compare analytics transactions credited to other sources; the example's is a last-click re-run of the platform export).
- The example notes that daily gaps in the previous week cannot be checked; this run did not.
- The "for the analyst to verify" list is longer here, with a formula for every ratio and each bound.

Points where the revised template was still open to a choice:

- **Window wording for goals.** The template says "Not calculable for the full window" and the example says "for the full week". This run used "window", as the template does.
- **Which note covers a flag.** The note "nothing else was changed" was quoted beside the 6 November flag and "No note covers it" was still written. The revised template asks for this; the run did it, but a reader could still prefer to quote the note under "per the notes".
- **Empty spend-range line.** With one day flagged, the run wrote "No other day outside the spend range", which is the format's empty line adapted. The template does not say what to print when one day is flagged and no others are.
- **The cutoff date as the prepared date.** The run used the cutoff date, 9 November, as the revised template says.

Facts in the outputs not in the inputs: weekdays, which come from the calendar, and hypotheses, which are labelled as such. No figure lacks a source in the inputs.

## What the earlier run found, and what was changed

The earlier run reported these points; each was addressed in the template and the example:

- Goal status: the template said "not calculable" in one place and "true for the days available" in another, and the example said "met". Now one rule: not calculable for the full window, the status on the days available, and the bound; the example gives the bounds.
- A blank cell is not a stop. Spend alone may be added across platforms for a budget goal. Clicks against sessions use the days both cover, printed separately from the conversion days.
- A general note does not cover a flag. The hypothesis limit applies to differences between sources too. The anomaly rule names the analytics measures (sessions, transactions, revenue).
- The thresholds' defaults are now in the instruction block, with "at or above" and "at or below". The prepared date is the cutoff date and money carries the currency symbol supplied.
- The example's analytics source labels were made neutral ("search / cpc", "social / paid"), its second hypothesis for 6 November was re-grounded, and its narrative no longer assumes the missing Sunday will arrive.

After this run, an independent review asked for small edits, and they were made without a new run. The default rounding and the rule for the spend-range line (the choice noted above, where this run wrote "No other day outside the spend range") were written into the instruction block, and the output format's empty line now allows that wording. In the example, "week" became "window" in the goal lines, the search clicks against sessions line gained its difference (higher by 63, 4.7%) and its check, the narrative says "platform-reported", the first open question names who can supply Sunday, and the spend-range line was added. This run's recorded output above is unchanged; it already used these defaults and wording, so the edits bring the template and the example into line with it.

This was one run by one model. It shows the template can be followed on the example; it does not show how it performs in a client's environment.
