# Zirodelta

Prediction markets for crypto funding rates. Trade the crowd, not the price.

## Products

### [Settled](https://www.settled.pro) — Funding Rate Prediction Markets

Binary prediction markets on whether crypto funding rates will be positive or negative at the next settlement. Markets auto-create, auto-resolve from live exchange data, and auto-pay winners in USDC on Solana.

- 3,700+ perpetual futures tracked across 5 exchanges
- Markets settle every 1–8 hours — no waiting days or weeks
- Proprietary OU pricing model calibrated on 9.2M historical settlements
- No price exposure, no liquidation — pure crowd positioning

### [Zidee](https://t.me/ZideeBot) — Funding Rate Sniper Bot

Telegram bot that detects extreme funding rate opportunities and executes delta-neutral hedges (spot + perp) in real-time. Open before settlement, collect funding, close after.

## Open Source

| Repo | Description |
|------|-------------|
| [resolver](https://github.com/Zirodelta/resolver) | Permissionless resolver daemon — earn 10 bps per market resolved |
| [docs](https://github.com/Zirodelta/docs) | Protocol documentation — [docs.settled.pro](https://docs.settled.pro) |
| [landing](https://github.com/Zirodelta/landing) | Zirodelta marketing site |

## Data & Research

We operate one of the largest private funding rate datasets in crypto — spanning 6 exchanges since 2019. We track funding interval changes in real time, detecting when exchanges silently modify settlement frequencies.

- [Funding Rate Data](https://www.settled.pro/rates) — 3,700+ pairs across 5 exchanges
- [Interval Change Tracker](https://www.settled.pro/funding-intervals) — 7,800+ regime changes detected
- [Crowd Positioning](https://www.settled.pro/crowd) — Real-time YES/NO sentiment across all markets
- [API Documentation](https://docs.settled.pro) — Public endpoints for market data
- [Blog & Research](https://www.settled.pro/blog) — Funding rate analysis, market structure, trading guides

## Links

- [www.settled.pro](https://www.settled.pro) — Trade
- [devnet.settled.pro](https://devnet.settled.pro) — Free $1,000 test USDC
- [docs.settled.pro](https://docs.settled.pro) — API Docs
- [learn.settled.pro](https://learn.settled.pro) — Guides
- [@zirodelta](https://x.com/zirodelta) — X/Twitter
- [Discord](https://discord.gg/f9QJfZgs9V)

## Stack

Go · Next.js · Solana · ClickHouse · PostgreSQL · Redis · Docker

---

*Building in public. Settling in production.*
