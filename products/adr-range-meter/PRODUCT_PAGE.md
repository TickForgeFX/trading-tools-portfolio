# ADR Average Daily Range Meter by TickForgeFX

A clean, free tool that tells you how far this market usually moves in a day, how much of
that range is already gone, and where the day runs out of room. Attach it and read. No
signals, no repaint, no fuss.

## What it does

Drop it on any chart and the panel shows, live:

- The **average daily range (ADR)** over the last N days, the market's typical daily move.
- How much of that range **today has already used**, in points and as a percent.
- The **room left** up and down before the day reaches an average-sized range.
- Today's **high and low**.

It also draws the two projection levels on the chart, confined to today so they read
clearly:

- **ADR High** = today's low + the ADR (where the day tops out if it runs a full average
  range up from its low).
- **ADR Low** = today's high − the ADR (the mirror to the downside).

The level tags pin to the edge of the screen when you zoom in, so you always know where
they are and how far.

## Why it exists

Most traders never ask the simplest question: has this market already done its usual day,
or is there still room? Thinking in ADR answers it. If a pair averages 60 pips and has
already moved 55, chasing a big new move is a bad bet. If it has moved 15, there is room to
run. And when price reaches the projected day high or low, it has spent an average range,
which is where continuation gets less likely and reversals more common. This tool puts that
context on your chart at a glance.

## What it does not do

It does not place trades, fire buy or sell signals, or predict direction. It measures the
range and shows you the context. The decisions stay yours.

## Recommended use

Works on any symbol and any timeframe (the range is always measured from the daily bars, so
it is the same on M5 or H1). Set the ADR period to taste (default 5 days; some prefer 10, 14
or 20). Pair it with your own entries, it is a context tool, not a system.

## Notes

Free, and built to the same forge standard as the rest of the TickForgeFX toolset: honest,
clean, no hype. If you find it useful, an honest review helps more than you know.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
