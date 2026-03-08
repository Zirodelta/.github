# Architecture

## Overview

Zirodelta runs a delta-neutral funding rate arbitrage engine (Beta-X1) across multiple centralized exchanges. The system is fully automated with AI-operated monitoring and self-healing capabilities.

## Components

### Beta-X1 Engine (Contabo VPS)
- **Temporal** — Workflow orchestration (farming loop, allocation, fund routing, smart exit)
- **Redis** — State management, caching
- **ClickHouse** — Time-series data (funding rates, 3.1M+ snapshots)
- **PostgreSQL** — Relational data (hedge executions, users, API keys)
- **Workers** — Heavy (trading operations) + Light (monitoring, tracking)
- **API** — FastAPI backend serving dashboard + external integrations

### Transparency Dashboard
- **Frontend** — Nuxt.js, deployed on Vercel
- **Data** — Reads from Beta-X1 API (positions, funding payments, hedge history)
- **URL** — transparency.zirodelta.ag

### AI Operations Layer (Mac mini)
- **Paco** — AI operator: engine development, monitoring, auto-fix pipeline
- **Raka** — Marketing agent: @zirodelta content, engagement, community intel
- **Crons** — Health check (45min), PR review (45min), content cycles

## Data Flow

```
Exchanges (31) → Capacity Scan → Opportunity Ranking → Allocation
→ Hedge Execution (long + short) → Funding Tracking → Smart Exit
→ SWEEP (return capital to treasury) → Next cycle
```

## Infrastructure

| Service | Host | Details |
|---------|------|---------|
| Engine | Contabo VPS (194.233.91.149) | Docker Compose, 8 containers |
| Dashboard | Vercel | Auto-deploy from GitHub |
| AI Ops | Mac mini (Tailscale) | OpenClaw, Claude, cron pipeline |
| Treasury | Solana mainnet | ZDLTVdBtzuBXAhmjN5LnYHZ8cysRH2bXuTtxBum8u34 |
