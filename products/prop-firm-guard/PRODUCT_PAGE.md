# Prop Firm Drawdown and Daily Loss Guard

![Know your rails before you breach them: daily loss and max drawdown as progress bars toward their limits](../../screenshots/PropFirmGuard/banners/pfg-hero-dark.png)

A free risk panel for MetaTrader 5. It watches the two rails that end most prop-firm accounts, the **daily loss limit** and the **overall (max) loss limit**, and shows you exactly how close you are, live, with progress bars and an alert before you breach. It never trades and fires no signals. It just keeps your limits in front of you.

## What it shows

- **Today's P/L** in account currency and percent, color-coded.
- **Daily loss** as a progress bar toward your daily limit, plus the exact cash room left before you breach.
- **Overall drawdown** as a second bar toward your max loss limit, with room left.
- **SAFE / CAUTION / DANGER** status, and an alert at a warning level (80% by default) and again if a limit is breached.

## Built for prop-firm rules

- **Daily limit** as a percent of account size (default 5%), measured on current equity so open floating losses count, the way most firms breach. You choose what it measures from: the start-of-day balance, equity, whichever is higher, or the day's highest equity so far, for firms that count the day's loss from your best point rather than from the open.
- **Daily reset hour** you set to your firm's server timezone.
- **Overall limit** (default 10%) as Static (a fixed floor below your starting balance, FTMO style) or Trailing (from your peak equity, for trailing-drawdown accounts).
- **Initial account size** worked out from your own deal history, so it is the balance your challenge actually started at rather than whatever it happened to be the day you installed this. Every limit here is a percentage of that number, so when your history does not reach far enough back to be sure, it says so plainly instead of guessing. You can always set the figure exactly (e.g. 100000 for a 100k challenge).

The day's baseline and your peak are stored durably, so closing the chart, recompiling or restarting the terminal does not reset your day or hide a real drawdown.

## Why it helps

Most challenges are not lost on a bad strategy, they are lost on a single day that quietly ran past the daily limit. This keeps the two numbers that actually matter in front of you, so you size down or stop before the account does it for you.

## What it does not do

It does not place trades, close trades, or fire buy and sell signals. It is a monitor; the decisions stay yours.

Free. Works on any symbol and timeframe.

---

Current version: **1.20**

On the MQL5 Market: [Prop Firm Drawdown and Daily Loss Guard](https://www.mql5.com/en/market/product/184431)
