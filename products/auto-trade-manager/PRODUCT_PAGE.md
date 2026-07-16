# Auto Breakeven Trailing Stop and Partial Close by TickForgeFX

A clean, free position manager for MT5. Attach it to a chart and it looks after the trades
you already have open: moves them to break-even, trails the stop as they run, and takes a
partial off at your target. It never opens trades and never fires a signal. It only manages
what is already there.

## What it does

Attach it and it watches every open position that passes your filter, then applies three
independent, point-based rules:

- **Auto break-even.** Once a trade is a set number of points in profit, the stop jumps to
  entry (plus an optional buffer so it locks a few points rather than exactly flat).
- **Trailing stop.** After a further threshold, the stop follows price at a fixed distance,
  tightening only when it improves by at least your step, so it never spams tiny changes.
- **Partial take-profit.** At your target it closes part of the position (any percent you
  set), once per position, and can move the rest to break-even straight after.

Each rule is toggled independently, so you can run just break-even, just trailing, just a
partial, or all three together.

## Trigger units, your choice

Read every threshold above in whichever unit fits how you trade. One setting switches the
unit for break-even, trailing and the partial together:

- **Points** (default) — the classic fixed-distance behaviour. Existing setups are unchanged.
- **ATR multiples** — the same setup adapts to each symbol's volatility (ATR period and
  timeframe are configurable).
- **R multiples** — 1R is the trade's initial stop distance, so break-even and targets are
  expressed in risk. For the truest R, attach the manager when the trade opens; it reads 1R
  from the stop present when it first sees the position. If a position has no stop when first
  seen, R cannot be established and the panel says so.
- **Money** — in your account currency, so a trade moves to break-even after a set profit and
  trails a set amount behind.

## Alerts when it acts

The manager works silently, so this tells you the moment it does something. You can get an
alert the instant a trade moves to break-even, the trailing stop starts, or a partial closes:

- **Your channels.** Popup, sound, push notification to the MetaTrader mobile app, or email.
  Each channel is toggled on or off independently.
- **One alert per event, per trade.** Each event is announced once and never repeats, even
  after a chart reload or a terminal restart, so you are not pinged on every tick.
- **Per-event switches.** Get only the partial alert, or only break-even, if that is all you
  want to hear about.

## Who and what it manages

- **This chart's symbol, or every symbol.** One toggle. Leave it on one chart to manage
  everything, or pin it per symbol.
- **By magic number, or everything.** Set a magic to manage only one EA's trades, or leave
  it at 0 to manage every position on the account, including trades you placed by hand.

It works the moment you attach it to any symbol; with the default point triggers no per-symbol
tuning is required, and ATR or R modes adapt automatically when you want them to.

## Built to be safe

- **No signals, no entries.** It manages risk on open trades. It cannot open a position.
- **Stops only ever move to protect.** A stop is never loosened, only tightened toward
  profit.
- **One partial per position, and it remembers.** The partial-taken state is stored durably,
  so a chart reload, recompile, or terminal restart can never take a second partial off the
  same trade.
- **Respects the broker.** It normalizes volume to the symbol's lot step and keeps every stop
  the broker's minimum distance away, so modifications are accepted, not rejected.

## The panel

A compact forge panel shows what it is managing and which rules are live. It is draggable
from anywhere on it, lockable in place, and always clamped fully on-screen, the same standard
as the rest of the TickForgeFX toolset.

## What it does not do

It does not open trades, predict direction, or fire buy and sell signals. It is a management
utility: you (or another EA) open the trade, this looks after it.

Note: in the MetaTrader Strategy Tester it opens small sample trades so it has activity to show
(a manager that only watches would otherwise do nothing in a backtest). On a live or demo
account it never opens a trade, it only manages what is already there.

## Recommended use

Works on any symbol and any timeframe. A common setup: break-even at roughly your average
stop distance, trailing a little beyond that, and a partial at your first target. Tune the
point triggers to the symbol's typical range.

## A note on account type

On a **hedging** account each position is managed on its own. On a **netting** account there
is one position per symbol, so adding to it will not trigger a second partial (the partial is
tracked per position, and a netted add is still the same position).

## Notes

Free, and built to the same forge standard as the rest of the TickForgeFX toolset: honest,
clean, no hype. If you find it useful, an honest review helps more than you know.

## Changelog

**v1.2**
- New: alerts when the manager acts. Get a popup, sound, push notification, or email the moment
  a trade moves to **break-even**, the **trailing stop** starts, or a **partial** closes.
- One alert per event, per trade, with durable memory, so nothing repeats after a chart reload
  or a terminal restart. Each channel and each event has its own on/off switch.
- No change to the management logic: stops still only ever tighten, the partial is still once
  per position, and the tool still never opens a trade.

**v1.1**
- New: trigger-unit modes. Read break-even, trailing and the partial in **points, ATR
  multiples, R multiples, or money (account currency)** — one setting for all three.
- Points stays the default, so existing setups behave exactly as before.
- Panel now shows the active trigger unit, and flags when a unit cannot be read yet (for
  example R mode on a position that has no stop).
- No change to the safety model: stops still only ever tighten, the partial is still once per
  position with durable memory, and the tool still never opens a trade.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
