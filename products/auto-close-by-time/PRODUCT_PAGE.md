# Auto Close by Time and Weekend

A free scheduled closer for MetaTrader 5. Attach it to a chart, set a time, and it flattens your
open trades for you: at a set time each day, before the weekend gap, or once a trade has been open
too long. It opens nothing and fires no signal. It just gets you flat on the schedule you decide.

## Three ways to be flat
- **Daily time close.** Close every day at a time you set (server time), your session end, before
  rollover, whenever you want to be out.
- **Weekend close.** Be flat before the weekend gap. Pick the day and time (Friday 20:55 server by
  default), so you are not holding through the Monday open.
- **Max holding time.** Close any trade older than a limit you set, so a short-term position never
  quietly becomes an overnight or all-week bag.

Enable one, two, or all three. Each works on its own.

## Which trades it closes
- **This chart's symbol, or every symbol** (one toggle)
- **By magic number, or everything** (0 = every position on the account, including manual trades)
- **Buys, sells, or both** (it can also delete your pending orders on a scheduled close)

## Built to be safe
- **It runs on server time** and keeps its own clock, so the weekend close still fires on a quiet
  Friday evening when ticks go sparse.
- **It waits out a spread spike.** If a scheduled close comes due while the spread is blown out, it
  holds briefly for the spread to settle before flattening. Spread never triggers a close, it only
  makes a scheduled one safer.
- **It will not fire a stale close.** If the terminal starts up well after a scheduled time, that
  one is skipped rather than closing you out at the wrong moment, and it tells you a close was missed.
- **A restart is safe.** A completed close is remembered, so restarting your terminal will not
  re-close trades you have re-opened.
- **No signals, no entries.** It only closes trades you already have open.
- A clear forge panel shows the next close and a live countdown, the count in scope, the current
  spread, and your max-hold setting, and it drags anywhere on the chart.

## What it does not do
It does not open trades, predict direction, or fire buy/sell signals. You place the trades, it
closes them on your schedule. It needs Algo Trading enabled to act.

Free. Works on any symbol and any timeframe. If you have ever forgotten to close before the weekend,
this is the reminder that acts for you.
