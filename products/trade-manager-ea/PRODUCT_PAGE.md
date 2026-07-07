# Trade Manager One Click Risk and Partials by TickForgeFX

The honest trade cockpit for MT5. You decide **when** to trade; it handles the risk sizing,
the one-click execution, the full management and the daily protection. Drag a stop line, read
the exact risk-based lot, open with one click, and let it run your break-even, trailing and
partials. It fires no signals and makes no predictions.

## Size the trade

- **Draggable stop and target lines** right on the chart. Move the stop and the sizing updates
  live.
- **%-risk position sizing.** It shows the exact lot for the percent of balance or equity you
  choose to risk, the money at risk, the stop distance in points, and the reward-to-risk.
- Respects the broker's minimum, maximum and step lot size.

## Execute in one click

- **Buy and Sell buttons on the chart.** A click opens at market with the computed lot, the
  stop from your line, and the target from your target line (or a reward-to-risk multiple if you
  use no target line).
- **Legal-stops safe.** Prices are normalized, kept the broker's minimum distance away, the
  spread is checked, and the trade is pre-validated with the broker's own check before it is
  ever sent.
- The button that matches your stop placement is the one that is armed, so you always open the
  trade you set up.

## Manage it automatically

- **Auto break-even** at a reward-to-risk trigger you set, with an optional buffer.
- **Trailing stop** that follows price and only ever tightens, throttled by your step so it
  never spams tiny changes.
- **Up to three partial take-profits**, each with its own trigger and percent, taken once each.
  The partial state is stored durably, so a reload, recompile or restart can never double-close
  a position.
- Manage only the trades this tool opens, or every position that passes your **symbol** and
  **magic** filter.

## Protect the account

- **Daily-loss lockout.** Set a maximum daily loss (percent of the day's starting balance) and
  an optional maximum number of trades per day. When a limit is hit, new one-click entries are
  blocked for the rest of the day while your open trades keep being managed.
- The lockout latches for the day and survives a restart, so a breach is a breach. A new trading
  day clears it.
- The panel shows why it is locked and your live daily profit or loss against the limit.

## Built to be safe

- **No signals, no prediction, no auto-entries.** You choose the entry. It sizes, executes,
  manages and protects.
- **Stops only ever move to protect.** A stop is never loosened, only tightened toward profit.
- **Respects the broker.** Volume is normalized to the lot step and every stop is kept a legal
  distance away, so orders are accepted, not rejected.
- A draggable, lockable forge panel that always stays fully on-screen, the same standard as the
  rest of the TickForgeFX toolset.

## What it does not do

It does not generate signals, predict direction, or decide when to enter. You click; it sizes,
executes, manages and protects. No profit claims, ever.

Note: in the MetaTrader Strategy Tester it opens small sample trades so it has activity to show
(a button-driven cockpit would otherwise do nothing in an automated backtest). This does not
demonstrate the management; the panel, buttons and management run on a live or demo chart with
algo trading enabled.

## A note on account type

On a **hedging** account each position is managed on its own. On a **netting** account there is
one position per symbol.

## Recommended use

Works on any symbol and any timeframe. A common flow: set your risk percent, drag the stop to
your invalidation level, set a target (or use the reward-to-risk default), then open with one
click and let the management run. Tune the break-even, trailing and partial triggers in R to how
you like to manage.

## Notes

Built to the same forge standard as the rest of the TickForgeFX toolset: honest, clean, no hype.
If you find it useful, an honest review helps more than you know.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
