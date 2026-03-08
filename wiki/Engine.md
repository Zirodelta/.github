# Beta-X1 Engine

## Trading Pipeline

The farming loop runs every 45 minutes via Temporal scheduled workflow:

1. **CAPACITY_SCAN** — Fetch funding rates from all connected exchanges, rank by annualized delta
2. **ALLOCATE** — Select top opportunities, size positions based on available capital
3. **HEDGE** — Open simultaneous long/short positions across exchanges
4. **REBALANCE** — Check existing positions, close any that hit exit criteria
5. **SWEEP** — Withdraw freed capital from exchanges back to treasury wallet

## Key Parameters

| Parameter | Value | Description |
|-----------|-------|-------------|
| MIN_DELTA_ANN | 3% | Minimum annualized funding rate delta to enter |
| HARD_FLOOR_DELTA | 0.1% | Emergency exit threshold |
| MAX_CAPITAL_PCT | 80% | Max % of treasury to deploy |
| MAX_HEDGE_PAIRS | 25 | Max simultaneous hedge pairs |
| MIN_POSITION_USD | $25 | Minimum position size |
| GUARD_POLL_INTERVAL | 30s | FundingGuard rate check frequency |

## Safety Systems

- **FundingGuard** — REST polling every 30s, triggers exit on rate inversion
- **SmartExit** — Emergency close if one side of hedge disappears
- **FundRouting** — Minimum balance guards, dry_run safety defaults

## Connected Exchanges

Gate.io, Bybit, Binance (OKX removed — no API keys configured)

## Database

- **ClickHouse** — `zdlt_web3data` database, funding rate time-series
- **PostgreSQL** — `zdlt_webapp` database, `executor_beta` schema, hedge executions
