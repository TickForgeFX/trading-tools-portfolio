# Prop Firm Auto Close and Drawdown Lockout

**Automatically enforce your prop-firm risk limits.**

The Prop Firm Enforcer watches your daily-loss and overall drawdown limits, and when a limit is about to be hit it closes every position, cancels your pending orders, and locks out new trades. It is built to stop one bad run before it breaches your limit and fails your challenge. You set the limits; it does the discipline for you. It fires no signals and opens no trades of its own.

## What it enforces
- **Daily loss limit**, measured on equity (floating trades count), from your start-of-day balance
- **Overall / maximum drawdown**, Static from your initial balance or Trailing from peak equity
- **FTMO-style defaults** (5% daily, 10% overall), configurable to any firm's rules
- Acts at a **buffer before the limit** (default 90%), so the close completes before you actually breach
- On trigger: closes all positions, deletes pendings, then **locks out** new trading (a new position is closed on open) until the next day, or until you reset
- Optional daily **profit-target** stop, and a published global lock flag your other EAs can honor

## Built to be safe
- A **readiness gate + multi-cycle warm-up**, so a transient bad reading on startup or reconnect can never trigger a false close
- **Per-account state that survives a restart**, so a lock you hit stays in force
- Handles a **prop-firm account reset on the same login**, so it never inherits an old account's lock
- Account-wide or symbol-only, on both **netting and hedging** accounts
- Clear reset via a panel button or an input

## Honest about what it can and cannot do
It can only act while MetaTrader is running with **Algo Trading enabled** (the panel says so when it is off). It closes at a buffer before the limit to leave room, but a sudden gap can still overshoot, so set the buffer to give yourself margin. It enforces the limits you set; it makes no prediction and no profit claim.

## The panel
A clean, draggable, lockable forge panel showing both rails as live progress bars with room-left, a SAFE / CAUTION / DANGER / LOCKED status, and your P/L for the day. No signals, no entries, no predictions.
