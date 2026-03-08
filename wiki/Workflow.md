# Development Workflow

## The Rule (Non-Negotiable)

**Issue → Branch → PR → CodeQL → Review → Merge → Auto-deploy**

No exceptions. No direct pushes to main. No skipping PR review.

## Issue Management

- **Types:** Bug, Task, Feature (set via GraphQL, not labels)
- **Labels:** Area-based (`engine`, `dashboard`, `fund-routing`, `guard`, `tracking`, `temporal`, `monitoring`, `critical`)
- **Milestones:** M1 Engine Stability (Mar 15), M2 Autoresearch (Apr 1), M3 First Profitable Month (May 1)

## Territory

| Area | Owner | Action |
|------|-------|--------|
| Engine (workflows, activities, trading logic) | Health check cron / Paco | Auto-fix with branch + PR |
| Dashboard, monitoring, alerts, UX | camillee-x1 | Assign on GitHub with context |

## PR Review

- PR review cron runs every 45 minutes
- Reviews diff, checks for breaking changes
- Approves clean PRs
- Checks deploy status post-merge
- Auto-reruns failed deploys

## Issue Templates

Engine task template at `.github/ISSUE_TEMPLATE/engine-task.md`
