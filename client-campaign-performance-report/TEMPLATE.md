# Client campaign performance report

Workflow template, version 0.1.0.

## Purpose

Draft the client performance report for one reporting period from the platform and analytics exports a person supplies: the reporting window and its gaps, the figures under each source with the attribution window that source uses, progress against the client's goals, the places where sources disagree, the anomalies, a drafted narrative, discussion points for the client call, open questions and a list of calculations for the analyst to check. Periods that differ in length, attribution windows that differ between sources, and conversions that were not recorded are kept apart and labelled, never blended. A day or a source that is missing is shown as a gap, never as zero. Explanations for what moved are hypotheses with the check that would settle them. The assistant prepares; it never sends the report, posts it, changes an account or approves its own narrative.

## When to use it and when not to

Use it at the weekly or monthly cutoff, once the exports for the period have been pulled and the previous period's figures are to hand.

Do not use it:

- for a creator or influencer campaign ranked from a store's own orders. Use the creator campaign performance report;
- for a whole-business weekly brief for an owner, which also covers cash and pipeline. Use the weekly owner business brief;
- for a quarterly review across a client relationship. Use quarterly business review preparation;
- to decide what to change in a campaign, to set a budget, or to promise a client a result. Those are the account team's decisions, and the report only supplies facts and questions;
- when no export for the period exists. The assistant does not estimate figures.

## Roles

- **Runs it:** the analyst, who pulls the exports and starts the work.
- **Verifies the calculations:** the analyst, from the list the report ends with.
- **Approves the narrative and the discussion points:** the account lead.
- **Can check a hypothesis:** the media buyer or whoever manages the account in the platform.
- **Sends the report to the client:** a person, after approval. The assistant never does.

## Inputs

The assistant works from files and notes the person supplies. It needs no connection to any account and never asks for a password or a login code.

1. **Run settings.** The client, the reporting window (first and last day), the cutoff date, whether the report is weekly or monthly, the previous period's first and last day, and the currency (its symbol is printed before every money figure). If the window or the client is missing, stop and ask.
2. **Platform exports, one per ad platform, by day.** Default headers: `Date`, `Campaign`, `Spend`, `Impressions`, `Clicks`, `Conversions`, `Conversion value`. If a required header does not match, stop and ask which column is which. Never guess a column. A column the platform does not export, such as impressions on a source that has none, is "not exported", not zero.
3. **Analytics export, by day and source.** Default headers: `Date`, `Source / Medium`, `Sessions`, `Transactions`, `Revenue`. The same rule applies if a header does not match. If no analytics export is supplied, continue with the platform figures and print "no analytics export supplied" in the sections it feeds.
4. **Reporting definitions.** Which conversions count, the attribution window each source uses (for example 30-day click, or 7-day click and 1-day view, or last non-direct click), the order in which sources appear, and the decimals to print. If a source's attribution window is missing, print "window not stated" beside it and do not compare that source with another.
5. **Client goals and budget.** Each goal as a metric, a direction, a number and the source it is measured in. If missing, print "no goals supplied" and skip the goals section's lines.
6. **The previous period.** The previous report, or the previous period's totals per source. If missing, print "no previous period supplied" and skip comparisons.
7. **Notes.** Changes in the period, such as budget moves, launches, pauses, tracking problems and anything the account team already knows. If missing, print "no notes supplied".
8. **The agency's report format.** If missing, use the output format in this template.
9. **Thresholds and rounding.** [your anomaly threshold] (default: a movement of 25% or more) and [your one-day swing] (default: a day whose spend is at or above 1.5 times, or at or below 0.5 times, the average of the other days in the window), and the rounding rules (default below).

## The procedure

1. **Check the inputs.** Confirm one client, one window and the headers of every export. Count the rows of each file and the days each source covers. If a header does not match, a date falls outside the window, two rows repeat the same date and campaign, or a figure is text where a number belongs, stop and ask. A blank cell is not a stop: it is "not recorded" (step 2). Do not repair the file.
2. **Find the gaps.** For each source and each metric, list the days in the window it covers and the days it does not. A day with no row is not available. A row with the figure 0 is zero. A blank figure in a row is not recorded. The only exception is a note that says a campaign was paused on a day, which makes a missing day zero spend "per the note". Print the cause only when a note gives one. Spend, clicks and conversions are gaps in the same way: a source can cover seven days of spend and five of conversions.
3. **Total each source.** Sum each metric over the days it covers, per source. Print the number of days beside the total. Do not total across sources: platform conversions and analytics transactions are never added together, and two platforms' conversions are never added together unless the definitions say they share a window. The one exception is spend: a budget goal that covers several platforms uses the sum of their spend, printed with each platform's own figure and day count.
4. **Build the ratios from sums.** Click-through rate = clicks ÷ impressions. Cost per click = spend ÷ clicks. Cost per conversion = spend ÷ conversions. Return on ad spend = conversion value ÷ spend. Build each from the summed figures, never by averaging daily ratios. If a metric's conversions or value cover fewer days than spend, build cost per conversion and return on ad spend from the spend of the same days only, and say which days. A ratio with a zero or unrecorded divisor is "undefined", not zero.
5. **Compare on per-day averages.** Divide each current total by the number of days it covers and each previous total by the number of days the previous period covers. State the day counts. The change is (current per day − previous per day) ÷ previous per day, to one decimal place. Ratios are compared on their own values; a percentage metric such as click-through rate is compared in percentage points. If the previous figure is zero or missing, the change is "not calculable". Never compare two sources with each other as if they were two periods.
6. **Measure against the goals.** For each goal, print the figure in the source the goal names, the days it covers, and whether it is met, not met or not calculable. Where every day the goal needs is present, say met or not met. Where a day that could change the result is missing, print "Not calculable for the full window", then the status on the days available ("met on the n days available" or "not met on the n days available") and the bound the arithmetic gives, for example how much missing spend would break a return goal if that day had no value, how many conversions a cost goal would need, or how much missing spend would exceed a budget. A goal already broken by the days present is "not met", whatever the missing days hold. Never print "met" alone for a window with a gap.
7. **Compare sources on the same days only.** Where a platform and analytics both cover a day, compare the two on exactly those days: the difference in conversions and in value on the days both recorded them, and the difference in clicks against sessions on the days both have clicks and sessions (these may be more days than the conversion days; print the days used for each), and the difference as a percentage of the analytics figure. State each source's attribution window. Report days where analytics recorded sales and a platform recorded none or has no conversions recorded. Do not reconcile, adjust or choose between the figures.
8. **Find the anomalies.** Flag a movement of [your anomaly threshold] or more against the previous period in a platform's per-day spend, conversions, conversion value or cost per conversion, and in an analytics source's per-day sessions, transactions or revenue (analytics has no spend). Flag any single day on which a platform's spend meets the one-day swing: at or above 1.5 times, or at or below 0.5 times, the average of the other days in the window (or the swing the settings give). For each flag print the facts first, with the supporting figures from the other source if the same day is covered. A note covers a flag only if it names that change, day or cause; a general note such as "nothing else was changed" does not, though it may be quoted beside the flag. If a note covers the flag, quote it as "per the notes". If no note covers it, write "No note covers it" and give at most two hypotheses, each beginning "Hypothesis", each with the check that would confirm it and who can run it. Never state a cause as a fact unless a note does. If no movement is flagged, print "No source-level movement of [threshold] or more". If no day is flagged, print "No day outside the spend range"; if a day is flagged and no further day is, print "No other day outside the spend range" after the flagged entry.
9. **Draft the narrative.** Three short paragraphs at most, in plain words, every sentence resting on a printed figure: what each source reported, how it moved per day, whether the goals are met, and the gaps. Say "platform-reported" where a figure comes from a platform. Carry a hypothesis only with the word "hypothesis" or "may". Make no forecast, give no advice, and describe nothing the figures do not show.
10. **Write the discussion points.** Numbered questions for the call, each tied to an anomaly, a gap, a difference between sources or a goal. No recommendation unless the account lead asks.
11. **List the open questions.** Every gap that needs a person to supply or confirm something, with who can.
12. **List the calculations for the analyst.** Every derived figure with its formula and inputs, so it can be recomputed in a spreadsheet. A figure that cannot be recomputed from the supplied files is a stop condition.
13. **Return the draft** to the analyst. The analyst verifies, the account lead approves the narrative, and a person sends the report. Nothing leaves the assistant.

Default rounding: money to two decimals, cost per click to three, counts as whole numbers, per-day counts to two decimals (impressions to whole numbers), percentage changes to one decimal, click-through rate to two decimals, return on ad spend to two decimals. Changes are computed from unrounded values.

## Exceptions and stop conditions

- **A header does not match, a date is outside the window, a figure is text where a number belongs, or two rows repeat the same date and campaign:** stop and ask. Do not guess or repair. A blank cell is not a stop; it is not recorded.
- **No export for a source the definitions name:** print the source with "no export supplied" and continue with the others; its goals are not calculable.
- **A source's days do not reach the end of the window:** print the gap and the days covered. Do not extend, scale up or fill the period.
- **A platform's conversions are blank on some days:** print them as not recorded. Never use analytics figures in their place. Print the analytics figures for those days beside, as a separate fact.
- **The previous period has a different length from the current one:** compare per day and print both day counts.
- **Attribution windows differ or are missing:** print each source's own window and keep the sources apart.
- **A figure cannot be recomputed from the files supplied:** do not print it.
- **The files contain a password, a login code or an access token:** do not repeat it; tell the person to remove it.
- **A note names a person in connection with a dispute or a pay matter:** leave the name out of the report and refer to the item generally.
- **Asked to send the report, change a budget or a bid, edit an account, approve the narrative, remove a gap, fill a missing day or explain a movement as fact:** decline, and name the role that does it.
- **Asked for a forecast or a guarantee of a result:** decline; the report describes the period supplied.

## Output format

```
CLIENT PERFORMANCE REPORT: [client], [week of date / month year]
DRAFT. Figures await [analyst]'s check. The narrative awaits [account lead]'s approval. Nothing has been sent.

For: [analyst] and [account lead]. Prepared [cutoff date], from [each file with its row count], [definitions], [goals], [previous period], [notes / no notes supplied].
Window: [weekday date] to [weekday date] ([n] days). Compared with: [weekday date] to [weekday date] ([n] days), from [source] / no previous period supplied.
Definitions: [each source and its attribution window; currency]. Ratios are built from summed figures. Changes are per-day averages over the days with data.

REPORTING WINDOW AND GAPS
[Source]: [x] of [n] days[; conversions x of n days]. Not available: [dates]. [Cause, per the notes.] Shown as a gap, not zero.
[Source]: ... / No gaps in the window.
Previous period: [totals only / by day], from [source].

SOURCE FIGURES
[Source name] ([attribution window]; [x] of [n] days)
Spend [total] ([per day]; previous [per day]; [change]). Impressions [total] (...). Clicks [total] (...).
Conversions [total] (...). Conversion value [total] (...).
Click-through rate [value] (previous [value]; [change in points]). Cost per click [value] (previous [value]; [change]). Cost per conversion [value] (previous [value]; [change]). Return on ad spend [value] (previous [value]; [change]).

[Repeat for each platform, then for each analytics source: Sessions, Transactions, Revenue.]
[No analytics export supplied.]

AGAINST CLIENT GOALS
[Goal]: [figure] on [x] of [n] days ([source]). [Met / Not met. / Not calculable for the full window: reason; met or not met on the [x] days available; bound the arithmetic gives.]
[No goals supplied.]

WHERE SOURCES DIFFER
[Source pair], [days in both]: [platform figures]; [analytics figures]. [Platform] is higher/lower by [n] conversions ([x]% of the analytics figure) and [value] ([x]%). Not reconciled.
[Days a platform recorded none or has no conversions recorded and analytics recorded sales.]
[At most two hypotheses, each labelled Hypothesis, each with the check and who can run it.]
[Nothing to compare.]

ANOMALIES
[n]. [Source, day or metric]: [the facts, with the other source's figures]. [Per the notes: ... / No note covers it.]
Hypothesis [n]: [the explanation]. To confirm: [the check]. Who can check: [role].
[No source-level movement of [threshold] or more. / No day outside the spend range. / No other day outside the spend range.]

DRAFT NARRATIVE (for the account lead's approval)
[Up to three short paragraphs.]

DISCUSSION POINTS
[n]. [Question, tied to the section it comes from.]
[None.]

OPEN QUESTIONS
[n]. [What is needed, from whom.]
[None.]

FOR THE ANALYST TO VERIFY
[Each derived figure with its formula and inputs.]

Draft for [analyst]'s check and [account lead]'s approval. Nothing has been sent, posted or changed in any account.
```

## Reviewer checklist

1. Every source total equals the sum of its rows over the days it covers. (Analyst)
2. Every ratio is built from summed figures, and the days behind it are stated. (Analyst)
3. Every missing day or blank figure is shown as a gap or not recorded, and none appears as zero. (Analyst)
4. Platform and analytics figures are kept apart, each with its attribution window, and nothing is blended or added across sources. (Analyst)
5. Every change is per day over the stated day counts, and a change against a zero or missing figure is not calculable. (Analyst)
6. Every anomaly is real, its facts come before its explanation, and every explanation is labelled a hypothesis with a named check unless a note supplies it. (Analyst)
7. Every sentence of the narrative rests on a printed figure and nothing in it forecasts or advises. (Account lead)
8. Every goal with a missing day that could change the result is "not calculable for the full window", with its status on the days available labelled as such and its bound printed; no such goal reads "met" alone. (Account lead)
9. Every discussion point is the account lead's to raise, and the report sends nothing. (Account lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Complete window.** Seven days from every source, no gaps. Expected: no gaps line, all changes per day, no anomaly unless a threshold is crossed.
2. **Missing day.** One platform's export has no row for the last day. Expected: six of seven days printed as a gap, totals over six days, per-day comparison, goals depending on spend not calculable where the day could change the result.
3. **Blank conversions.** Conversions blank on two days with spend present. Expected: not recorded, cost per conversion built from the spend of the recorded days only, analytics for those days shown as a separate fact.
4. **Explicit zero.** A row with spend 0. Expected: zero, not a gap, and cost per click undefined where clicks are 0.
5. **Different period lengths.** A five-week month against a four-week month. Expected: per-day averages with both day counts.
6. **Different attribution windows.** Two platforms with different windows. Expected: each window printed and no combined conversion total.
7. **Platform above analytics.** Platform conversions exceed analytics transactions on the same days. Expected: the difference printed on the same days, not reconciled.
8. **One-day spend swing.** A single day at about twice the average of the others. Expected: an anomaly with the facts, the other source's figures, and at most two hypotheses with checks.
9. **A note covers a movement.** Expected: quoted as "per the notes", not as a hypothesis.
10. **Header mismatch.** A platform export names its spend column `Cost`. Expected: stops and asks which column is spend.
11. **No previous period.** Expected: figures printed, comparisons skipped with the line "no previous period supplied".
12. **Asked to fill a gap or send.** "Assume Sunday matched Saturday" or "send it to the client". Expected: declines and names the role.
13. **Zero previous figure.** Expected: change not calculable.
14. **Goal with a missing day.** A return goal over a week with the last day missing. Expected: "not calculable for the full window", the status on the days available, and the spend above which the week would break the goal if that day had no value; never "met" alone.
15. **Blank cell.** A blank conversions cell. Expected: not recorded, no stop.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a client performance report for an analyst and an account
lead, from the exports and notes they supply. You prepare; people decide.
You never send the report, post it, change a budget, a bid or any account,
approve your own narrative, or contact the client. You never ask for a
password or a login code and need no access to any system.

The user will supply: the client, the reporting window and the previous
period; one export per ad platform by day (default headers Date, Campaign,
Spend, Impressions, Clicks, Conversions, Conversion value); the analytics
export by day and source (Date, Source / Medium, Sessions, Transactions,
Revenue); the reporting definitions with each source's attribution
window; the client goals and budget; the previous report; notes on what
changed; and the agency's format. If the client, the window, or every
export is missing, stop and ask. If a header does not match, a date falls
outside the window, a figure is text where a number belongs, or two rows
repeat the same date and campaign, stop and ask; never guess or repair
the file. A blank cell is not a stop; it is not recorded. Print money
with the currency symbol supplied, and date the report with the cutoff
date. If any other input is missing, say so in the section it feeds and
continue.

1. For each source and metric, list the days covered and the days not. A
   day with no row is not available. A blank figure in a row is not
   recorded. Only 0 in a row is zero. Print a cause only if a note gives
   one. Never turn a gap into zero or fill it.
2. Total each source over the days it covers, with the day count. Never
   add figures across sources, and never add two platforms'
   conversions (spend alone may be added across platforms, for a budget
   goal, as item 5 says).
3. Build click-through rate, cost per click, cost per conversion and
   return on ad spend from summed figures, never from averaged daily
   ratios. Where conversions or value cover fewer days than spend, use
   the spend of the same days only and say which. A zero or missing
   divisor makes the ratio undefined.
4. Compare to the previous period on per-day averages, printing both day
   counts. Change = (current - previous) / previous, one decimal; use
   percentage points for percentage metrics; if the previous figure is
   zero or missing, say not calculable.
5. Give each goal's figure, the days behind it, and met or not met. Where
   a missing day could change the result, write "Not calculable for the
   full window", then met or not met on the days available, and the bound
   the arithmetic gives (for example the spend above which a return goal
   breaks if that day had no value). Never write "met" alone for a window
   with a gap. Add up spend across platforms only for a budget goal,
   printing each platform's figure.
6. Compare each platform with analytics on the days both cover, printing
   each attribution window, the days used for conversions and value and
   for clicks against sessions, the differences and the difference as a
   share of the analytics figure. Report days where analytics recorded
   sales and a platform recorded none or has no conversions recorded. Do
   not reconcile or choose between them.
7. Flag per-day movements of 25% or more (or the threshold the user
   gives) against the previous period in a platform's spend, conversions,
   value or cost per conversion, and in analytics sessions, transactions
   or revenue, and any day on which a platform's spend
   is at or above 1.5 times, or at or below 0.5 times, the average of the
   other days. Facts first, with the other source's figures. A note
   explains it only if it names that change, day or cause; then quote it
   as "per the notes". Otherwise (a general note such as "nothing else was
   changed" does not count) write "No note covers it" and give at most
   two hypotheses, each labelled "Hypothesis", each with the check that
   would confirm it and who can run it; the same limit applies to a
   hypothesis about why sources differ. Never state a cause as fact
   unless a note does. If no movement is flagged, print "No source-level
   movement of [threshold] or more". If no day is flagged, print "No day
   outside the spend range"; if a day is flagged and no other, print "No
   other day outside the spend range" after the flagged entry.
8. Write the narrative in at most three short paragraphs, each sentence
   resting on a printed figure, saying "platform-reported" for platform
   figures. No forecast, no advice, no cause stated as fact.
9. Write numbered discussion points and open questions, each tied to the
   section it comes from. Recommend nothing unless asked.
10. Under "For the analyst to verify", list every derived figure with its
    formula and inputs. Print no figure you cannot recompute from the
    files supplied.
11. Use the output format exactly. If a section has nothing in it, print
    its empty line. Unless told otherwise, round money to two decimals,
    cost per click to three, counts to whole numbers, per-day counts to
    two decimals (impressions per day to whole numbers), percentage
    changes to one decimal, click-through rate and return on ad spend to
    two decimals, and compute changes from unrounded values. End with the
    draft line.

If asked to send, post or change anything, approve the narrative,
remove or fill a gap, state a cause as fact, forecast, or promise a
result, decline and name the role that decides. If a file contains a
password, a login code or an access token, do not repeat it; tell the
user to remove it. If a note names a person in connection with a
dispute or a pay matter, leave the name out. Recheck every total, ratio
and percentage against the rows before you return the report.
```

## What to customize

- The order and wording of the sections, to match your agency's report format.
- The anomaly threshold (default 25%) and the one-day swing (default at or above 1.5 times, or at or below 0.5 times, the average of the other days), in the settings and in item 7 of the instruction block, and whether anomalies are checked on conversions and value as well as spend.
- The attribution window each platform uses, the conversions you count, and which source your client treats as the number of record.
- The comparison period: the previous week or month, the same period last year, or both.
- The decimals and the currency your clients are used to.
- The columns on your exports. Add campaign-level or ad-set-level rows if you report at that depth; the gap and total rules are the same.
- Who verifies the calculations and who approves the narrative when the usual person is away.
- Where the approved report is kept and who sends it.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Run twice on its invented example in Claude on 10 November 2026; the instructions, the output format and the example were revised after the first run, and the second run is the one recorded in public/trial.md. After that run a review led to small edits, with no re-run: the default rounding and the rule for the spend-range line were written into the instruction block, and the example's wording was brought into line with the template. Not yet tested in a client environment.
