# Currency Strength Meter Multi Timeframe by TickForgeFX

A clean, free currency strength meter for MT5. It ranks the eight major currencies
(EUR, GBP, AUD, NZD, USD, CAD, CHF, JPY) by how they are actually moving across the 28
major pairs, and shows you which are strong, which are weak, and which way each one is
turning. It computes on closed bars only, so it does not twitch on every tick. It never
trades and fires no signals.

## What it shows

Attach it to any chart and a forge panel shows, live:

- **The eight majors ranked** strongest to weakest, each with its strength value and a
  color-coded bar, so the pecking order reads at a glance.
- **Multi-timeframe alignment.** Four timeframe cells per currency (M15, H1, H4, D1 by
  default, all configurable), colored by strength. When a currency is green across all
  four, it is strong on every horizon, which is the high-conviction read.
- **Momentum direction.** An arrow on each currency showing whether it is gaining or
  losing strength, so you catch a currency turning, not just where it already is.
- **The cleanest pair.** The strongest currency versus the weakest one, named as the
  pair to watch (for example "EUR strongest, JPY weakest, cleanest pair: long EURJPY").
  It is a read, not a signal.

## Honest by design

- **Closed bars only, no repaint.** Strength updates when a bar closes, not tick by
  tick. Most free meters jump around on every price change, which makes them noise. This
  one is stable, so what you read is what actually happened.
- **A transparent method, not a black box.** Strength is the averaged percent change of
  each currency across the pairs that contain it, oriented so up means stronger. No
  hidden formula, no magic.
- **It measures, it does not predict.** No buy and sell arrows, no promises.

## Built to just work on your broker

It auto-detects your broker's symbol naming, including suffixes like `.pro` or `.m`, and
skips any pair your broker does not offer. The panel footer shows how many of the 28
pairs it found, so you always know it is reading the full basket.

## Configure it to your style

- **Four timeframes** you choose for the alignment cells, and which one drives the
  ranking and the main bar.
- **Lookback** in bars for the percent-change window.
- Toggle the momentum arrows and the pair read on or off.

## What it does not do

It does not trade, predict, or fire signals. It measures relative strength from real
price and puts it in front of you. The decisions stay yours.

## Recommended use

Attach it once on any chart. Use the multi-timeframe cells to find currencies aligned
across horizons, the momentum arrows to spot turns, and the cleanest-pair read as a
starting point for your own analysis. Works on any symbol and timeframe.

## Notes

Free, and built to the same forge standard as the rest of the TickForgeFX toolset:
honest, clean, no hype. If you find it useful, an honest review helps more than you know.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
