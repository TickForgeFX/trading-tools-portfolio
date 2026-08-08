# Prop Firm Challenge Objectives Tracker

**Free MetaTrader 5 indicator. Monitor only: it never places, modifies or closes an order.**

A funded-account challenge is decided by three numbers, and your terminal shows you none
of them. This panel tracks all three on your chart: how much of the profit target you have
made, how many trading days you have banked, and how much of your total profit came from
your single best day.

That last one is the consistency rule, and it costs more traders their payout than drawdown
does.

---

## The three objectives

**Profit target.** Progress as a percentage with the cash still to go. Measured on closed
trades plus open ones, or closed only, whichever your firm counts. Deposits, withdrawals,
credits and bonuses are never profit. Separately billed costs count against you the way
your firm sees them: commission posted as its own daily entry, charges, swap and exchange
fees all reduce the figure, not just the profit printed on the trade.

**Minimum trading days.** Counts days you actually opened a trade, so one position scaled
out across a week stays one trading day rather than four. Switchable to count any trading
activity. The day boundary follows your firm's reset hour, not your broker's midnight.

**Consistency.** Your largest winning day as a share of total profit, on closed results.
Stays blank until the sample is large enough for the cap to be reachable at all: on a 45
percent cap that is three winning days, because one winning day is always 100 percent of
your profit and two can never be under 50. A number that is certain in advance tells you
nothing.

## It tells you when it does not know

The account size and the challenge start are worked out from your deal history. When the
history does not reach far enough back to see where the account began, the panel shows
dashes and asks for the two numbers rather than showing a confident wrong one.

This matters because a tool like this is usually installed in the middle of a challenge,
not on day one.

## Built for how challenges actually run

- A reset, a retry, a new deposit or a payout begins a new cycle, and the panel follows it
  instead of carrying the last attempt forward.
- Small broker movements such as rebates and loyalty credits do not disturb the window.
- Nothing is stored between sessions. Every figure is recomputed from history, so there is
  no stale state to clear and nothing to reset by hand.
- Two accounts in one terminal never share a baseline.

## Alerts

Popup when the profit target is reached and when the best day passes the cap, with optional
push to the MetaTrader app. Attaching it to an account you have already been trading never
announces something that happened before you installed it.

## What it does not do

This is the objectives side of a challenge, the part that decides whether you pass. It does
not watch your daily loss limit or your maximum drawdown. It cannot know your firm's exact
wording either, so the target percent, minimum days, cap and reset hour are all yours to
set. Defaults are generic.

---

## How it was built

- **254 replica cases** covering the target arithmetic, day counting across the reset-hour
  boundary, the consistency sample gate, the deal-type partition against real MQL5 enum
  values, and the refusal paths.
- **Three rounds of adversarial review**, each run as parallel independent passes over the
  whole source. Round one returned 75 findings, round two around 50, round three 26. Every
  round's fixes were themselves reviewed, which is how the last two rounds found that the
  previous round's repairs had introduced new defects.
- **Panel rendered from its own layout constants** before ever being attached to a chart, so
  geometry defects are caught in a drawing rather than over screenshot rounds.
- **Layout drift is detected by parsing the source**, not by comparing constants to
  themselves. Verified by injecting a real change and confirming the suite fails.

Built for MetaTrader 5. Compiled X64 Regular.
