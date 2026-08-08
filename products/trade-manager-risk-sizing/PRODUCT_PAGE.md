# Trade Manager with Risk Sizing and Trailing Stops

**MetaTrader 5 Expert Advisor / Utilities / Risk management / paid**

You said one percent a trade. Your last ten say otherwise, because the stop moves and the
lot size does not follow it. Put entry, stop and target on the chart as three draggable
lines. Drag the stop to where the trade is actually wrong and the size follows it, so one
percent is one percent whether that stop sits ten points away or two hundred. One click then
sends it at exactly that size. After that it runs the trade for you: partial closes,
break-even, a trailing stop, and a daily limit that stops you entering when the day has gone
badly enough.

**It never decides to trade. You do.** There are no signals, no entry rules and no strategy
anywhere in it. You choose the direction and the levels; this places that trade at the
correct size and then manages it exactly the way you configured.

![Drag the stop, the size follows](../../screenshots/TradeManagerRS/banners/tmrs-hero-dark.png)

## Plan it on the chart

- Drag Entry, Stop and Target. Grab them anywhere along the line, not at one hidden weld
  point.
- Lot size, money at risk, stop distance and reward-to-risk recompute as you drag.
- Risk as a percent of balance or equity, or a fixed amount in your account currency.
- Prefer a rule to a drag? Put the stop a fixed number of points or an ATR multiple behind
  price, and lock the target to a reward-to-risk multiple so it follows.
- Your plan is saved per symbol and restored when you come back, so a timeframe change or a
  restart never quietly rebuilds it from wherever price happens to be.

## Enter it in one click

- Buy or sell at the planned size, with the stop and target taken straight from your lines.
- Place the entry line away from price and it becomes the right pending order by itself, a
  stop order or a limit order depending on which side you put it.
- The button names what it is about to do before you press it, including the order type and
  the size.
- An optional second click confirms, and the confirmation expires on its own and dies the
  moment you move a line.

## Then it manages the trade

![What happens after the fill](../../screenshots/TradeManagerRS/banners/tmrs-manage-dark.png)

| Stage | What it does |
| --- | --- |
| Partial close | Takes part of the position off at your first target |
| Break-even | Stop to entry plus a buffer, so it locks a little rather than sitting on your fill |
| Second partial | A percent of what is left, not of the original size |
| Trailing stop | Fixed distance, ATR, Chandelier below the high since entry, or behind the last N closed candles |

Triggers read in whichever unit suits you: points, ATR multiples, R multiples, or your
account currency. Everything reads closed bars, so nothing repaints, and the stop only ever
moves toward you. It is never widened, in any mode.

## And it stops you when the day is done

![A limit that acts](../../screenshots/TradeManagerRS/banners/tmrs-limits-dark.png)

Set a daily limit and an overall limit as a percent of your account. The panel shows the
headroom you have left before either one bites. On a breach it cancels its working orders,
closes what it opened and refuses new entries until the day rolls. It is a limit that acts,
not a progress bar that watches.

## The parts nobody advertises

![It refuses to size a bad plan](../../screenshots/TradeManagerRS/banners/tmrs-guard-dark.png)

- **It refuses to size a bad plan.** Put the stop a hair from the entry and most panels hand
  back a confident 77 lot number. This one prints two dashes and tells you the stop is too
  tight to size. That is the single most expensive mistake a sizing tool can make, and it is
  one click from being an order.
- **A button that cannot fire tells you why.** Market closed, trading disabled, daily limit
  reached, not enough free margin, stop too close to the current price. Ten distinct
  reasons, in plain words, instead of a control that silently does nothing.
- **The sizing arithmetic is right on instruments where it usually is not.** A stop is a loss
  and a target is a gain, and on many CFDs and crosses your broker values those two
  differently. Sizing off the wrong one quietly risks more than you asked for. This reads the
  correct value for each leg.
- **A level you cannot see still tells you where it is.** Zoom in until a line leaves the view
  and it pins to the edge of the chart as a chip showing its name and price. Click it and the
  chart refits.
- **If price runs through your stop while the entry is tracking price, the plan voids.** It
  does not silently flip into the opposite trade, which is what reading direction from
  geometry alone would do.

## Good to know

- Works on netting and hedging accounts, on any symbol your broker offers.
- It manages the positions it opened, identified by its own magic number, so it will not
  touch your other trades or another tool's.
- Partials, break-even, trailing, the target line and the account limits can each be switched
  off. With all of them off it is simply a risk-sized one-click entry panel.
- Every stage fires at most once per position, and that memory survives a restart, a
  recompile and a change of ticket.

## About the demo, stated plainly

On the MQL5 Market a paid product's demo runs only in the Strategy Tester, and MetaTrader
does not deliver click events to an Expert Advisor's panel there. That is a platform
limitation and it is not something this product can fix. So the demo will draw the panel,
size the trade and run the full management engine in visual mode, and you can watch all of
it work, but the one-click controls need a live chart. The gallery video shows the panel
being driven on a real chart.

---

Part of the [TickForgeFX](https://github.com/TickForgeFX/trading-tools-portfolio) toolkit.
