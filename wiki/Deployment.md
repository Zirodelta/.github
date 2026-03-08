# Deployment

## Pipeline

```
Code → Branch → PR → CodeQL Scan → Review (1 approval) → Merge → GitHub Actions → Docker Build → Quay.io → Auto-deploy to Contabo
```

## Branch Model

Single branch: `main`. All changes go through PRs. Auto-deploy on merge.

## Ruleset (main-protection)

- Restrict deletions ✅
- Require PR before merging ✅ (1 required approval)
- Block force pushes ✅
- Require CodeQL scan results ✅
- Bypass: kisrafistya (emergency only)

## Autonomous CI/CD

- **Health check cron** (every 45min) — Detects errors, creates issues, writes fixes, opens PRs
- **PR review cron** (every 45min) — Reviews diffs, approves clean PRs, checks deploy status, reruns failed deploys
- Failed deploys auto-rerun. Escalate only if same workflow fails 2+ times.

## Server

- Host: Contabo VPS (194.233.91.149)
- Runtime: Docker Compose (8 containers)
- Registry: Quay.io
