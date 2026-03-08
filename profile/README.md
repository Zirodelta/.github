# Zirodelta

Delta-neutral cross-exchange funding rate arbitrage protocol on Solana.

Automated. Transparent. AI-operated.

## What We Do

Zirodelta captures yield from perpetual futures funding rate differentials across exchanges. The engine opens perfectly hedged positions — long on one exchange, short on another — collecting the spread while maintaining zero directional exposure.

No bets on price. Pure yield extraction from market microstructure.

## How It Works

1. **Scan** — Monitor funding rates across 31 exchanges, 3,600+ symbols, every cycle
2. **Select** — Rank opportunities by annualized delta, filter by liquidity and spread
3. **Hedge** — Open simultaneous long/short positions across exchanges
4. **Guard** — Monitor rate inversions in real-time, exit before yield turns negative
5. **Sweep** — Return capital to treasury after position close, capture realized P&L

The entire pipeline runs autonomously with AI-operated monitoring, issue detection, and self-healing code deployment.

## Architecture

| Component | Purpose |
|-----------|---------|
| **Beta-X1 Engine** | Core arbitrage engine — capacity scanning, hedge execution, funding tracking, smart exit |
| **Transparency Dashboard** | Real-time visibility into positions, funding payments, hedge history, engine health |
| **Vault** | User-facing yield product — deposit stables, earn from funding rate arbitrage |

## Links

- [zirodelta.com](https://zirodelta.com) — Main site
- [zirodelta.ag](https://zirodelta.ag) — Vault product
- [transparency.zirodelta.ag](https://transparency.zirodelta.ag) — Live engine dashboard
- [zirodelta.org](https://zirodelta.org) — Holder hub & analytics
- [@zirodelta](https://x.com/zirodelta) — X/Twitter

## Key Numbers

- 31 exchanges connected
- 3,600+ perpetual symbols tracked
- 3.1M+ funding rate snapshots collected
- 93 days of continuous data (and counting)
- 60/25/15 revenue split (vault yield / operations / buyback burn)

## Team

Built lean by design. Strategy discovery + AI-augmented development and operations.

---

*Building in public. Running in production.*
