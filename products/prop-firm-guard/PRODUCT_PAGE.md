# Prop Firm Drawdown and Daily Loss Guard by TickForgeFX

A clean, free risk panel for MT5. It watches the two rails that end most prop-firm accounts,
the **daily loss limit** and the **overall (max) loss limit**, and shows you exactly how close
you are, live, with progress bars and an alert before you breach. It never trades and fires no
signals. It just keeps your limits in front of you.

## What it shows

Attach it to any chart and a forge panel shows, live:

- **Today's P/L** in account currency and percent, color-coded.
- **Daily loss** as a **progress bar** toward your daily limit, plus the exact cash room left
  before you breach.
- **Overall drawdown** as a second bar toward your max loss limit, with room left.
- A **SAFE / CAUTION / DANGER** status, and an **alert** when you reach a warning level (80% by
  default) and again if a limit is breached.

## Built for prop-firm rules

Firms measure the rails differently, so it is configurable to match yours:

- **Daily limit** as a percent of your account size (default 5%), measured from the
  **start-of-day balance** on **current equity**, so open floating losses count, the way most
  firms breach.
- **Daily reset hour** you set to your firm's server timezone.
- **Overall limit** (default 10%) as either **Static** (a fixed floor below your starting
  balance, the FTMO style) or **Trailing** (measured from your peak equity, for trailing-drawdown
  accounts).
- **Initial account size** auto-detected, or set it exactly (e.g. 100000 for a 100k challenge).

The day's baseline and your peak are stored durably, so closing the chart, recompiling, or
restarting the terminal does not reset your day or hide a real drawdown.

## Why it helps

Most challenges are not lost on a bad strategy, they are lost on a single day that quietly ran
past the daily limit. This keeps the two numbers that actually matter in front of you, so you
size down or stop before the account does it for you.

## What it does not do

It does not place trades, close trades, or fire buy and sell signals. It is a monitor. The
decisions stay yours. (Auto-enforcement is deliberately not in a free indicator, and many firms
forbid trade-closing bots anyway.)

## Recommended use

Attach it once on any chart, set your firm's limits, reset hour, and (for accuracy) your exact
account size. Works on any symbol and timeframe. For the truest daily baseline, have it running
at the start of your trading day.

## Notes

Free, and built to the same forge standard as the rest of the TickForgeFX toolset: honest,
clean, no hype. If you find it useful, an honest review helps more than you know.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
