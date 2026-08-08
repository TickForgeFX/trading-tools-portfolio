# SMC and ICT: Structure, Liquidity, Dashboard

A clean, no-repaint Smart Money Concepts (SMC) and ICT toolkit for MetaTrader 5.
Market structure (BOS and CHoCH), order blocks, fair value gaps, liquidity, premium
and discount, ICT killzone sessions, and a multi-timeframe dashboard, so you can read
the chart at a glance instead of marking it up by hand.

Everything is detected on closed bars and never repaints.

## What it does

- Market structure: confirmed swings with Break of Structure and Change of Character,
  on a major swing layer plus an optional internal layer.
- Order blocks: the last opposing candle before a structural break, drawn as a zone
  and tracked until price mitigates it.
- Fair value gaps: the three-candle imbalance, with a size filter for noise and
  same-impulse merging so a cascade stays readable.
- Liquidity: buy-side and sell-side levels with an unswept-only option, equal highs
  and lows, and previous day high and low.
- Premium and discount: the active dealing range split at equilibrium, with an
  optional OTE band.
- Killzone sessions: Sydney, Tokyo, London, and New York as time markers, aligned to
  your broker automatically and adjusted for daylight saving.
- Multi-timeframe dashboard: bias, nearest point of interest, and nearest liquidity
  draw across M15, H1, H4, and D1, plus a plain-English line that sums up the picture.
- Alerts: popup, push, and email on the events you choose, on closed-bar confirmation.

## What you see on the chart

Green is bullish and buy-side, red is bearish and sell-side, gold flags an attention
state (a change of character, a swept level, a mitigated zone), and grey is quiet
context. Order blocks are a bordered zone, fair value gaps a clean outline, liquidity
a dashed line, premium and discount a soft wash. The panel doubles as a live colour
key, so you always know what you are looking at.

## Inputs and presets

Every module turns on and off on its own, and every colour, swing strength, count, and
session hour is an input. Three presets are included: Minimal for the cleanest view,
Balanced out of the box, and Full for everything. An automatic light and dark theme
reads your chart background and keeps the labels and zones readable either way.

## No repaint

Detection runs on closed bars only. Nothing is drawn from the forming bar, and once an
object prints it does not move or vanish. The only changes are deliberate and happen on
a bar close: a level flips to swept, a zone to mitigated, or a zone extends its right
edge. No-repaint is the first thing a serious trader checks, so it is stated plainly.

## What it does not do

This is an analysis tool. It does not place trades, it does not fire buy or sell
signals, and it does not predict direction. It marks structure clearly and
consistently. The decisions stay yours.

## Recommended use

Works on any symbol and any timeframe. Many traders run it on M15 to H4 for intraday
structure with the dashboard carrying the higher-timeframe context. The sessions find
your broker's clock on their own, so there is nothing to set up first. These are
recommendations only, nothing is locked to a symbol, timeframe, or account.

## Changelog

- v1.4: sessions that place themselves, and distances on the key levels. The broker's
  GMT offset is now read from the terminal instead of typed in, so the session ribbons
  and the dashboard's session line land correctly on the first attach rather than two or
  three hours out on a typical broker. Sessions also follow daylight saving now, with
  London on the European rule, New York on the United States rule, Sydney on the
  Australian one, and Tokyo correctly fixed because Japan keeps none. Each bar is judged
  on its own date, so a changeover weekend splits correctly instead of re-timing recent
  history. Both behaviours can be switched off, and the manual offset field still works
  exactly as before. Separately, the Key Levels section now shows how far premium,
  equilibrium, discount and the nearest buy-side and sell-side liquidity sit from the
  last closed bar, in pips.
- v1.3: fixed the OTE band label colliding with a Change of Character label where the two
  overlapped. The OTE tag now sits at the right edge of its bracket, clear of the
  structure labels on the left.
- v1.2: HH / HL / LH / LL swing labels on the major structure layer, theme-adaptive and
  suppressed at any swing that already carries a BOS or CHoCH so nothing stacks. Plus a
  declutter: the defaults now keep four order blocks and three fair value gaps per side
  instead of five each.
- v1.1: dashboard upgrade. The Read is promoted to a prominent context line, a confluence
  panel shows bias, zone, session, and the nearest point of interest as plain factual
  state, and a new Key Levels section lists named prices: premium, equilibrium, discount,
  the OTE band, nearest buy-side and sell-side liquidity, and previous day high and low.
  Panel readability pass on the text. No repaint, no new chart objects, all closed-bar.
- v1.0: first release. Market structure, order blocks, fair value gaps, liquidity,
  premium and discount with OTE, killzone sessions, the multi-timeframe dashboard, and
  closed-bar alerts.

## Support

Reach me through the product Comments or MQL5 messaging. I answer honestly and quickly,
and updates are tested against the previous version so they do not break what you rely
on.
