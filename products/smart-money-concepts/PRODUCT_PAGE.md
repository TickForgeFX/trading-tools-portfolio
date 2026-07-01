# SMC and ICT: Structure, Liquidity, Dashboard

No indicator makes you profitable on its own, and any product showing perfect arrows is just
screenshotting the winners. This one will not sell you that. It is a clean, no-repaint Smart
Money Concepts (SMC) and ICT toolkit that reads the chart for you: market structure, order
blocks, fair value gaps, liquidity, premium and discount, killzone sessions, and a
multi-timeframe dashboard. You see the whole picture at a glance instead of marking it by hand,
and you still make the call, just with the structure laid out cleanly in front of you.

## What it maps

- **Market structure**: confirmed Break of Structure and Change of Character on a major swing
  layer, plus an optional internal layer.
- **Order blocks**: the last opposing candle before a structural break, drawn as a zone and
  tracked until price mitigates it.
- **Fair value gaps**: the three-candle imbalance, size-filtered for noise, with same-impulse
  merging so a cascade stays readable.
- **Liquidity**: buy-side and sell-side levels with an unswept-only option, equal highs and
  lows, and previous day high and low.
- **Premium and discount**: the active dealing range split at equilibrium, with an optional
  OTE band.
- **Killzone sessions**: Sydney, Tokyo, London and New York, with a broker GMT offset you set
  once.
- **Multi-timeframe dashboard**: bias, nearest point of interest and nearest liquidity across
  M15, H1, H4 and D1, plus a plain-English line that sums up the read.
- **Alerts**: popup, push and email on the events you choose, confirmed on the bar close.

## Built to not repaint

No-repaint is the first thing a serious trader checks, so it is the first thing this gets
right. Detection runs on closed bars only. Nothing is drawn from the forming bar, and once an
object prints it does not move or vanish. The only changes are deliberate and happen on a bar
close: a level flips to swept, a zone to mitigated, or a zone extends its edge. What you saw
yesterday is still there today.

## Clean by default

Every module toggles on its own, and every colour, swing strength, count and session hour is
an input. Three presets are included: Minimal for the cleanest view, Balanced out of the box,
and Full for everything. An automatic light and dark theme reads your chart background and
keeps the labels and zones readable either way.

## What it does not do

This is an analysis tool. It does not place trades, fire buy or sell signals, or predict
direction. It marks structure clearly and consistently. The decisions stay yours.

## Recommended use

Works on any symbol and any timeframe; many traders run it M15 to H4 with the dashboard
carrying the higher-timeframe context. Built to the TickForgeFX standard: clean, honest, and
regression-tested updates that do not break what you rely on. Questions or requests, reach me
through the Comments or MQL5 messaging.

## Changelog

- v1.1: dashboard upgrade. The Read is promoted to a prominent context line, a confluence
  panel shows bias, zone, session, and the nearest point of interest as plain factual state,
  and a new Key Levels section lists named prices: premium, equilibrium, discount, the OTE
  band, nearest buy-side and sell-side liquidity, and previous day high and low. Panel
  readability pass on the text. No repaint, no new chart objects, all closed-bar.
- v1.0: first release. Market structure, order blocks, fair value gaps, liquidity, premium
  and discount with OTE, killzone sessions, the multi-timeframe dashboard, and closed-bar
  alerts.
