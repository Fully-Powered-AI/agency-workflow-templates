# Creative test evidence review

Workflow template, version 0.1.0.

## Purpose

Take one batch of ad creative that has finished running, with its results export, its conversion definitions and the campaign change log, and return one page for the creative strategist and media lead: an evidence table by creative, angle, format and hook, a clear mark on each creative saying whether its results can be read, roll-ups of the readable ones, tentative learning, and several next-test options. The assistant prepares the evidence. It never names a winner or a loser where samples are small, offers changed or conversions are unconfirmed, it never changes anything in an ad account, and it never decides what to test next.

## When to use it and when not to

Use it when a batch of creative has finished running and the team is about to decide what to make, test or retire next.

Do not use it for the following.

- Testing whether one result beats another by more than chance. That is the comparison claim check.
- Reporting on creators, their orders and their costs. That is the creator campaign performance report.
- Working out return on spend or revenue. This version reads cost per conversion only.
- Pausing, scaling or editing anything in an ad account. The assistant has no access to one and a person makes every change.
- Judging copy for claims a regulator or a platform might object to. That needs its own review.

## Roles

- **Starts it and supplies the inputs:** the creative strategist or a media analyst.
- **Checks the figures:** the media lead or an analyst, who recomputes the table from the export.
- **Decides what to test next and what needs more evidence:** the creative strategist and the media lead together. The assistant never does.

## Inputs

1. **The creative export,** one row per creative for the batch. Default headers: `creative_id`, `angle`, `format`, `hook`, `conversion_event`, `start_date`, `end_date`, `spend`, `impressions`, `clicks`, `conversions`. Extra columns are ignored and named in the output. If a header does not match, stop and ask which column is which; never guess. If a `creative_id` appears more than once, stop and ask whether the rows should be added together.
2. **The conversion definitions,** one row per event. Default headers: `conversion_event`, `meaning`, `window`, `confirmed`, `checked_against`. `confirmed` is yes, no or partly. Every `conversion_event` in the export must have a row; if one does not, stop and ask.
3. **The change log,** one row per change in the period. Default headers: `date`, `change_type`, `scope`, `description`. `change_type` is one of offer, price, landing_page, audience, budget, bid, tracking, creative or other. `scope` is "all" or a list of creative IDs from the export; the export has no ad set column, so a scope that names an ad set, a conversion event or anything else is not accepted and the assistant stops and asks which creatives it covers. If the change log is not supplied, say so at the top of the page and treat the batch as "change log not supplied": no creative can be marked readable on offer grounds, so every creative is marked Held back with the reason "change log not supplied".
4. **The batch name and the export date.** If the date is missing, write "export date not supplied".
5. **Optional settings.** Defaults: [your minimum conversions] of 30, [your minimum impressions] of 1,000 and [your gap threshold] of 20 per cent of the lower cost per conversion.

## The procedure

1. **Check the inputs.** Headers match; each creative appears once; every event has a definition; dates read as dates and `end_date` is not before `start_date`; every change-log `scope` is "all" or creative IDs that appear in the export; spend, impressions, clicks and conversions are numbers of zero or more; clicks do not exceed impressions. On any failure, stop and name the rows. If a change-log scope names something the export cannot resolve to creative IDs, stop, name the entry and ask which creatives it covers; never infer membership from an angle or any other name.
2. **Settle the reading of each conversion event.** An event confirmed "yes" counts as confirmed. "No", "partly" or blank counts as unconfirmed. A tracking entry in the change log dated inside a creative's run, whose scope is "all" or names that creative, makes that creative's conversions unconfirmed, because conversions before the date may be missing.
3. **Apply the change log.** A change touches a creative when its date falls between the creative's start and end dates inclusive and its scope is "all" or names that creative.
   - Offer, price, landing_page and audience: a creative is held back when, for any part of its run, it ran under a state that differs from the one the other creatives in the batch ran under at the same time. A change that touched every creative running that day is a shared change: no creative is held back, and the page notes that the batch's learning applies to the state after the change.
   - Creative: an edit to the asset itself during its run holds that creative back.
   - Budget and bid: noted only, never a reason to hold a creative back, because they change how much was delivered rather than what was offered. They are named beside the creative in the learning.
   - Other: noted only, and a question is asked if its effect is unclear.
4. **Check the size.** A creative is thin when its conversions are fewer than [your minimum conversions] or its impressions are fewer than [your minimum impressions].
5. **Mark each creative.** Readable when no reason applies. Held back when any reason applies, and every reason is listed: thin, offer changed, creative edited, conversions unconfirmed, change log not supplied. For each reason write what would make the creative readable. The run has finished, so more conversions, a matched record or a shared offer can only come from a re-run under the same conditions; write the need that way, for example "a re-run under the same conditions that reaches 30 confirmed conversions".
6. **Build the table.** One row per creative, in creative ID order. Cost per conversion is spend divided by conversions, to the cent; with no conversions, write "no conversions" and never divide by zero. Held-back creatives are shown with their figures as reported and their status, and are left out of every roll-up and comparison after the table. Add a batch line: total spend and the number of creatives, then conversions and spend for each event. Conversions of different events are never added together.
7. **Roll up the readable creatives.** Group by conversion event first. Within an event, list every angle, format and hook carried by any creative of that event. For each value give the readable creatives under it, their summed spend, summed conversions and cost per conversion (summed spend divided by summed conversions). A value with no readable creative says "no readable creative" and names the held-back creatives of the same event under it; creatives of another event are not named. An event with no readable creative at all gets one line, "[Event]: no readable creative ([IDs held back]). Nothing to roll up.", not a list of values. State what share of the batch spend sits on readable creatives.
8. **Find the clean pairs.** A clean pair is two readable creatives with the same conversion event that differ in exactly one of angle, format and hook. For each pair give both costs per conversion, the gap in money and the gap as a percentage of the lower cost. If the gap is less than [your gap threshold], say there is no gap worth reading. If it is equal to the threshold or more, say it is directional: one pair, one batch. If the two creatives had different budget or bid changes, say so. Never say which creative is better.
9. **Write the tentative learning.** A few sentences using only readable creatives and clean pairs. A gap in money or per cent is given only for a clean pair; for two readable creatives that are not a pair, say which costs less and that the gap cannot be put down to any one attribute, without a gap figure. If there is no clean pair, say so and say which attributes the readable creatives differ in. Then list, in one sentence, what cannot be said because creatives are held back. Words allowed: "cost less", "cost more", "is consistent with", "cannot be told apart". Words never used: winner, loser, best, worst, worked, failed, proved.
10. **Write two to four next-test options,** not ranked and not recommended. Each has the question it answers, the one attribute to vary (or "none" for a check or a re-run), what to hold the same (write "not applicable" for a check) and what must happen first. At least one option must be a one-attribute pair when no clean pair exists. Options that clear a held-back creative say how many conversions or what confirmation it needs.
11. **List the questions for the strategist and media lead,** at most five, each one whose answer could change the reading.
12. **Return it to the person who asked,** with the trace line.

## Exceptions and stop conditions

- **Header does not match, a creative appears twice, or an event has no definition:** stop and ask.
- **A change-log scope names an ad set, an event or anything the export cannot resolve to creative IDs:** stop and ask which creatives it covers.
- **Dates, numbers or clicks and impressions do not make sense:** stop and name the rows.
- **No creative is readable:** not a stop. Print the table and the held-back list, write "None." under roll-ups, learning and clean pairs, and give options that clear the most creatives.
- **Asked to name a winner or loser, to say which creative to scale or pause, or to make any change in an ad account:** decline; the strategist and media lead decide, and any change is made by a person.
- **Asked to ignore an offer change, count unconfirmed conversions as confirmed, or lower a minimum to make a creative readable:** decline. A person may change a setting before the run; the page then states the setting used.
- **Asked whether the gap in a pair is more than chance:** decline and point to the comparison claim check.
- **Asked for return on spend or revenue:** say this version does not read revenue.
- **The export contains personal data about people who saw the ads:** stop and ask for an export without it.

## Output format

```
CREATIVE TEST EVIDENCE REVIEW: [batch name]

For: [creative strategist and media lead]. Batch ran [start] to [end]; export as of [date]. [n] creatives, spend [total]. Extra columns ignored: [names, or "none"].

Conversion definitions used:
- [Event]: [meaning], [window]. Confirmed: [yes / no / partly], [checked against what, or "no second record"].

Change log for the period:
- [date], [type], [scope]: [what changed]. Treatment: [held back: IDs / conversions unconfirmed: IDs / noted only / shared change / no creative touched].

Evidence by creative, [n] creatives (cost per conversion is spend divided by conversions; creatives held back are left out of everything below this table):
Header row, printed first: ID | Angle | Format | Hook | Event | Ran | Spend | Impressions | Clicks | Conversions | Cost per conversion | Status
[one row per creative]
Batch: spend [total] on [n] creatives. [Event]: [conversions] conversions on [spend]. [Event]: [conversions] on [spend]. Events are never added together.

Held back from comparison:
- [ID]: [every reason]. Needs: [what would make it readable].

Readable creatives: [n] of [n], [spend] of [total] spend ([%]).
By angle ([event]): [value]: [n] creative(s) ([IDs]), spend [amount], [conversions] conversions, [cost] per conversion. [value]: no readable creative ([IDs held back]).
By format ([event]): [same layout]
By hook ([event]): [same layout]
[Event with no readable creative]: no readable creative ([IDs held back]). Nothing to roll up.

Clean pairs:
- [ID] and [ID], differing only in [attribute]: [cost] against [cost], a gap of [amount], [%] of the lower cost. [Directional: one pair, one batch / under the threshold, nothing to read]. [Budget or bid note, if any.]

Tentative learning:
- [sentence]

Next-test options (options only, none chosen):
1. [Question]. Vary: [one attribute, or "none" for a check or a re-run]. Hold the same: [list]. First: [what must happen].

Questions for you:
1. [question]

Every figure was calculated from the export, conversion definitions and change log supplied, using [tool or method]. No winner or loser is named, nothing has been changed in any ad account, and what to test next is yours to decide.
```

Print every heading in the format. Where a section has nothing to report, write "None." under it. The change log line reads "Change log not supplied." when there is no log. Separate table cells with " | "; padding the cells so the columns line up is optional.

## Reviewer checklist

1. Every figure in the table, the batch line and the roll-ups recomputes from the export. (Media lead)
2. Each held-back creative lists every reason that applies, and each reason traces to the export, the definitions or the change log. (Media lead)
3. Each change-log entry has a treatment, and the touched creatives are the ones its date and scope reach. (Media lead)
4. No roll-up, pair or sentence uses a held-back creative. (Creative strategist)
5. Every clean pair differs in exactly one attribute and shares its event. (Creative strategist)
6. The learning uses none of the banned words and claims nothing a pair of creatives cannot carry. (Creative strategist)
7. Every next-test option varies one attribute, says what is held the same and is not ranked. (Creative strategist)
8. The decision on what to test next is left with the strategist and media lead. (Both)

## Acceptance tests

Proposed tests. Only the first has been run, in the trial recorded with the example.

1. **The invented batch in the example.** Expected: C-01 and C-04 readable; C-02, C-03 and C-06 thin; C-05 held back for offer and size; C-07 and C-08 unconfirmed; readable spend $2,150.00 of $6,520.00 (33.0%); no clean pair.
2. **Header mismatch.** A column named "ad" instead of `creative_id`. Expected: stops and asks which column is which.
3. **Duplicate creative.** C-03 appears twice. Expected: stops and asks whether to add the rows.
4. **Event with no definition.** An event named "lead" with no row. Expected: stops and asks.
5. **Zero conversions.** A creative with 400 impressions and no conversions. Expected: cost shown as "no conversions"; held back as thin.
6. **Clean pair.** Two readable creatives with the same event, angle and format, differing only in hook, at $25.00 and $31.00 per conversion. Expected: gap $6.00, 24.0% of the lower cost, called directional.
7. **Gap under the threshold.** The same pair at $25.00 and $28.00. Expected: gap $3.00, 12.0%, "nothing to read". A pair at $25.00 and $30.00 is a gap of exactly 20.0% and is called directional.
8. **Shared change.** An offer change that touches every creative running. Expected: noted as a shared change; no creative held back for it.
9. **Change log not supplied.** Expected: stated at the top; every creative held back with that reason.
10. **Asked for a winner.** Expected: declines, offers the table and options.
11. **Asked to count unconfirmed conversions as confirmed.** Expected: declines.
12. **Change-log scope names an ad set.** An entry with scope "Gift giving ad set". Expected: stops, names the entry and asks which creatives it covers.

## Instructions for the AI assistant

```
You prepare a creative test evidence review for a creative strategist and
a media lead. You never change anything in an ad account, send anything, or
decide what to test next. You have no access to an ad account; you work
only from the files a person supplies. Never ask for a password or a login
code.

The user will supply: the creative export (headers creative_id, angle,
format, hook, conversion_event, start_date, end_date, spend, impressions,
clicks, conversions); the conversion definitions (conversion_event,
meaning, window, confirmed, checked_against); the change log (date,
change_type, scope, description, where scope is all or creative IDs from
the export); the batch name and export date; and
optionally the settings: the minimum conversions (default 30), the
minimum impressions (default 1,000) and the gap threshold (default 20
per cent of the lower cost). If a header does not match, a creative_id
repeats, or an event has no definition, stop and ask. Do not guess. If
the export contains personal data about people who saw the ads, stop and
ask for an export without it.

1. Check the inputs: dates, numbers of zero or more, clicks not above
   impressions, every change-log scope being all or creative IDs in the
   export. On any failure stop and name the rows. If a scope names an ad
   set, an event or anything else the export cannot resolve to creative
   IDs, stop and ask which creatives it covers; never infer it from an
   angle or a name.
2. An event counts as confirmed only if its confirmed value is yes. A
   tracking entry inside a creative's run, whose scope is all or names
   that creative, makes that creative's conversions unconfirmed.
3. Apply the change log by date and scope. Offer, price, landing_page and
   audience changes hold a creative back if it ran under a state that
   differed from the rest of the batch at the same time; a change that
   touched every running creative is a shared change and is only noted,
   with a note that the batch's learning applies to the state after the
   change. A creative edit during a run holds that creative back. Budget,
   bid and other changes are noted only. If the change log is not
   supplied, say "Change log not supplied." at the top and mark every
   creative Held back with the reason "change log not supplied".
4. A creative is thin if conversions are under the minimum conversions or
   impressions are under the minimum impressions.
5. Mark each creative Readable, or Held back with every reason and what
   would make it readable. The run has finished, so write the need as a
   re-run under the same conditions.
6. Build the table in creative ID order. Cost per conversion is spend
   divided by conversions to the cent; with no conversions write "no
   conversions". Show held-back creatives as reported. Add the batch line.
   Never add conversions of different events together.
7. Roll up readable creatives by event, then by angle, format and hook,
   listing every value carried by a creative of that event, with summed
   spend, summed conversions and cost per conversion; name held-back
   creatives of the same event only. An event with no readable creative
   gets one line, not a list. Give the share of spend that sits on
   readable creatives.
8. Find clean pairs: two readable creatives, same event, differing in
   exactly one of angle, format and hook. Give both costs, the gap in
   money and as a percentage of the lower cost. Under the gap threshold,
   say there is nothing to read; at the threshold or over it, call it
   directional (one pair, one batch). If the two had different budget or
   bid changes, say so. Never say which creative is better.
9. Write the tentative learning from readable creatives only. Say what
   cannot be said because creatives are held back. Give a gap figure only
   for a clean pair. Never use the words winner, loser, best, worst,
   worked, failed or proved.
10. Write two to four next-test options: question, one attribute to vary,
    what to hold the same, what must happen first. Vary may be "none" for
    a check or a re-run; for a check, hold the same is "not applicable".
    If there is no clean pair, at least one option must be a
    one-attribute pair. Do not rank or recommend. Add at most five
    questions for the strategist and media lead.
11. Use the output format exactly and print every heading. Where a
    section is empty write "None.". The change log line reads "Change log
    not supplied." when there is no log. Separate table cells with " | ".
    End with the trace line.

If asked to name a winner or loser, to say what to scale or pause, to
ignore an offer change, to count unconfirmed conversions as confirmed, or
to lower a minimum so a creative can be read, decline. If asked whether a
gap is more than chance, decline and point to the comparison claim check.
If asked for return on spend or revenue, say this version does not read
revenue.
```

## What to customize

- [your minimum conversions], [your minimum impressions] and [your gap threshold].
- Which conversion events your team treats as confirmed, and what they are checked against.
- The fixed list of angles, formats and hooks, so every creative is tagged the same way.
- What goes in the change log and who keeps it.
- Who must read the page before a learning is repeated to a client.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried once on its invented example in Claude on 10 November 2026; the record is published with it. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
