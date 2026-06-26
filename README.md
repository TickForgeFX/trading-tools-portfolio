# TickForgeFX: Custom Trading Tools for MetaTrader 5

I build and backtest custom trading tools for traders, prop firms, and trading
communities. If you have a strategy, an indicator idea, or a tool you wish
existed, I build it, test it properly, and tell you honestly whether it holds up
before you risk a dollar.

## What I build

- **Expert Advisors (trading bots)** for MetaTrader 5, coded exactly from your
  strategy rules with proper risk management and tested honestly. You bring the
  strategy, I build it faithfully and tell you how it holds up before you risk a
  dollar. MetaTrader 4 (MQL4) builds on request.
- **Custom indicators** for MetaTrader 5: dashboards, alerts, liquidity tools,
  session markers, and more. TradingView (Pine Script) on request.
- **Strategy backtesting and validation.** I test your idea on years of real
  data with conservative, honest assumptions, so you know what is real before
  you trade it.
- **Trading tools and automation.** Risk and position-size calculators, trade
  journals, data scrapers, alert bots, prop-firm drawdown trackers.
- **Fixing and upgrading** existing bots and indicators.

## How I work

Six years in the markets means I speak your language and I understand what
actually matters: clean execution, real risk management, and honest testing. I
will not sell you a "guaranteed profitable bot," because nobody honest can. I
build your idea exactly to spec, test it rigorously, and give you the truth.

## Flagship: Smart Money Concepts by TickForgeFX

A clean, no-repaint Smart Money Concepts indicator for MetaTrader 5. Market
structure (BOS / CHoCH), order blocks, fair value gaps, liquidity (BSL / SSL,
equal highs and lows, previous day levels), premium and discount with an OTE
band, killzone sessions, and a multi-timeframe dashboard. The panel reads the
current bias, zone, session, nearest liquidity, and the named key price levels
at a glance. Detection runs on closed bars only and never repaints. Now live on
the MQL5 Market:
[SMC and ICT Structure Liquidity Dashboard](https://www.mql5.com/en/market/product/182687).

![Market structure, order blocks, FVGs, liquidity and premium/discount on one chart](screenshots/SMC/thumbnails/smc-overview-dark-thumb.png)

![The at-a-glance panel: bias, zone, session, and named key levels, shown on a light chart](screenshots/SMC/thumbnails/smc-dashboard-light-thumb.png)

## Free tool: Visual Risk and Position Size Calculator

A clean, free position-size calculator for MetaTrader 5. Drop it on any chart and
drag three lines, Entry, Stop, and Target, to your levels. The panel reads back the
exact lot size for the percent of your account you choose to risk, the money at risk
in your account currency, the stop distance, and the reward-to-risk with the potential
profit at your target. It respects your broker's minimum, maximum, and step, and it
flags when your account is too small for your chosen risk. No signals, no repaint, just
the number you need before you place the trade. Free on the MQL5 Market:
[Visual Risk and Position Size Calculator](https://www.mql5.com/en/market/product/183000).

![The panel: direction, lot size, money at risk, stop distance, and reward-to-risk read off three dragged lines](screenshots/RiskCalculator/thumbnails/rc-panel-thumb.png)

![The calculator on a EURUSD chart with Entry, Stop, and Target lines in place](screenshots/RiskCalculator/thumbnails/rc-eurusd-thumb.png)

## Free tool: ICT Killzone and Session Tracker

A clean, free session tool for MetaTrader 5. A live panel counts down the Sydney, Tokyo,
London, and New York sessions, which one is open, how long is left, and when the next one
opens, with each session's name colour-coded so the panel doubles as a legend. On the chart,
each session's high and low range is drawn as a clean box. Times run on GMT with automatic
daylight-saving adjustment, so the sessions stay correct through the year without manual
re-timing. No signals, no repaint. Free on the MQL5 Market:
[ICT Killzone and Session Tracker](https://www.mql5.com/en/market/product/183024).

![The session panel and four colour-coded session range boxes on a XAUUSD chart](screenshots/SessionKillzoneTracker/thumbnails/skt-xauusd-thumb.png)

![The same tool on a EURUSD chart, sessions tracked across the day](screenshots/SessionKillzoneTracker/thumbnails/skt-eurusd-thumb.png)

## Free tool: Daily Weekly Monthly Key Levels

A clean, free reference-levels tool for MetaTrader 5. It draws the levels traders watch all
day, previous day high, low and close, previous week high and low, the daily and weekly opens,
and optional previous month high and low, read straight from the broker's own daily, weekly,
and monthly candles, so there is nothing to configure for your timezone. A compact panel lists
each level and how far it sits from price in pips. The labels adapt to the chart theme, light
on dark, dark on a white chart, so they stay readable everywhere. No signals, no repaint. Free
on the MQL5 Market:
[Daily Weekly Monthly Key Levels](https://www.mql5.com/en/market/product/183203).

![Key levels and the distance panel on a dark EURUSD chart](screenshots/KeyLevels/thumbnails/kl-dark-thumb.png)

![The same levels on a white XAUUSD chart, labels still readable](screenshots/KeyLevels/thumbnails/kl-light-thumb.png)

## Case study: Trend Breakout EA

A worked example of how I build and test a strategy, not a product. A trend-filtered
Donchian breakout coded exactly to spec, with real risk management and no grid or
martingale, then backtested honestly with conservative costs. Over two years on US30 H1
it returned a profit factor of 0.98, a marginal, slightly negative baseline, and the
case study reports that plainly. The value here is the transparent method and the clean,
extensible code, never a profit claim.

![Balance and equity curve, range-bound and drifting down over two years](screenshots/TrendBreakoutEA/raw/tbe-equity-curve.png)

Full rules, setup, and numbers: [Trend Breakout EA case study](products/trend-breakout-ea/CASE_STUDY.md).

## Contact

- MQL5: https://www.mql5.com/en/users/tickforgefx
- Email: TickForgeFX@protonmail.com
