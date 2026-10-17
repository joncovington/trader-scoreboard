# Trader Scoreboard

Weekly P&L results for the traders on two public trade feeds: the tastylive Follow Feed and
Lossdog VIP. Updated every Saturday morning.

- **Live page:** https://joncovington.github.io/trader-scoreboard/ shows both boards with a 7-day,
  30-day and all-time switch. Click a trader to see their trade history.
- **Weekly reports:** [`reports/`](reports/) holds one snapshot per week.

## How positions are scored

Neither feed reports P&L, so it is worked out from the orders the traders post.

- All of a trader's orders on the same contracts (opens, adds, rolls, partial closes) count as one
  position. Its P&L is the sum of their net cash once every leg is closed.
- **tastylive** is in actual dollars, at the trader's own size.
- **Lossdog** is per one unit, because its feed publishes no position size.
- **untrk** counts closes of positions opened before tracking began. They are counted but never
  priced.
- **open** includes options that expired without a closing order. They stay out of P&L until
  settlement prices are known.

## Disclaimer

These are unofficial numbers, worked out automatically from public posts. They may be incomplete
or wrong, and they are not financial advice. No affiliation with tastylive or Lossdog. Read the
full [disclaimer](DISCLAIMER.md) before relying on anything here.
