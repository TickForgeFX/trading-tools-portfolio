# Session and Killzone Tracker by TickForgeFX

A clean, free tool that tells you which trading session is live, how long is left, and
when the next one opens, with each session's high and low range drawn on the chart. No
signals, no repaint, no fuss.

## What it does

Drop it on any chart and you get two things:

- A **live panel** with a GMT clock and a row for each session (Sydney, Tokyo, London, New
  York). Each row shows whether the session is **active with the time left**, or **how long
  until it opens**. The active session is highlighted in its colour.
- A **range box** on the chart for each session, drawn from the session's high to its low
  across its hours, labelled and colour-coded, for the last few days. The current
  session's box grows in real time as the session runs.

That is the whole tool: know where you are in the trading day at a glance, and see each
session's range without marking it by hand.

## Why it exists

Session timing drives a huge amount of intraday trading: the London open, the New York
open, the Asian range. Most traders track it in their head or with a separate clock and a
mental note of broker time. This puts it on the chart, in your account's view, accurate on
any broker because it runs on GMT.

## Adjustable to your killzones

The session times are plain GMT inputs (standard time). Leave them on the defaults for the
standard Sydney, Tokyo, London and New York sessions, or set them to your exact killzone
windows (for example a London killzone of 07:00 to 10:00 GMT). The labels are editable too,
so the panel and the boxes read the way you trade.

## Automatic daylight saving

You do not have to re-time anything twice a year. Each session carries a daylight-saving rule
(Europe, US, Australia, or none for Tokyo), and the tool shifts that session by an hour
through its local summer so the panel and boxes stay correct year-round. It is on by default
and can be turned off if you would rather drive the times manually.

## What it does not do

It does not place trades, fire buy or sell signals, or predict direction. It tracks
sessions and draws their ranges. The decisions stay yours.

## Recommended use

Works on any symbol. Best on intraday timeframes (M1 to H1), where the session ranges are
meaningful. Times run on GMT with automatic daylight-saving adjustment, so the sessions stay
aligned through the year without manual re-timing.

## Notes

Free, and built to the same forge standard as the rest of the TickForgeFX toolset: honest,
clean, no hype. If you find it useful, an honest review helps more than you know.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
