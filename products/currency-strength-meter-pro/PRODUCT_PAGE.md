# Currency Strength Scanner Pro by TickForgeFX

A currency strength meter that does the next step for you. It ranks the 8 majors by their
strength, then turns that into a ranked table of the strongest-versus-weakest **pairs** to
trade, shows how many timeframes agree on each, and alerts you when the best setup forms.
Everything is computed on closed bars, so nothing repaints. It is monitor-only: it does not
trade or predict.

## Reads the 8 majors

- Ranks EUR, GBP, AUD, NZD, USD, CAD, CHF and JPY by their averaged percent change across the
  28 major pairs.
- **Four timeframes at once**, with momentum arrows showing which currencies are gaining or
  fading.
- **Closed-bar only**, so the reading is stable, not a tick-by-tick flicker.

## Ranks the pairs to trade

- For every pair it measures the **strength spread** (the strong currency minus the weak one)
  and ranks the biggest gaps first.
- Each row shows the pair, the direction (buy the strong, sell the weak), the spread size, and
  **how many of the four timeframes agree** (the conviction read).
- Fully-aligned setups are highlighted, so the highest-conviction pairs stand out at a glance.

## Alerts the best setup

- **Popup, push notification, email and sound**, each independently switchable.
- It alerts the **single best qualifying setup**, the strongest pair that also clears your
  alignment bar, so a trending market that lines up a dozen correlated pairs does not spam you.
- It fires on the **bar close** only, so an alert never repaints or takes itself back, and it
  re-fires only when the best setup changes.
- Set your own spread and alignment thresholds, so it is signal, not noise.

## Built to be honest

- **No repaint.** Everything is closed-bar.
- **No trades, no predictions, no profit claims.** It ranks strength and the pairs that follow
  from it. You decide what to do.
- Robust broker-symbol resolution (auto-detects your suffix); the panel shows how many of the
  28 pairs it found.
- A draggable, lockable forge panel that always stays fully on-screen.

## Recommended use

Attach it to any chart, on any symbol (it reads all the majors regardless). Use the ranked
opportunity table to find where the strongest and weakest currencies meet, check the alignment
column for conviction, and let the alerts tell you when a fresh high-quality setup forms. Tune
the spread and alignment thresholds to how selective you want to be.

## Notes

Built to the same forge standard as the rest of the TickForgeFX toolset: honest, clean, no
hype. If you find it useful, an honest review helps more than you know.

## Support

Reach me through the Comments or MQL5 messaging. I answer honestly and quickly.
