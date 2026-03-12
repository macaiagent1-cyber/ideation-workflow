# Ideation Workflow — Task Routing

## What This Workspace Does

Processes batches of community requests and ideas through five stages: extraction, pattern analysis, critical evaluation, prioritization, and strategy development. Each batch produces a prioritized list of ideas classified as MWP-workspace deliverables or software-required projects, with a delivery plan aligned to channel content.

## Stage Routing

| You want to... | Go to |
|-----------------|-------|
| Extract and standardize raw ideas from DMs/notes | `stages/01-intake/CONTEXT.md` |
| Find patterns, themes, and clusters across ideas | `stages/02-pattern-analysis/CONTEXT.md` |
| Deeply evaluate feasibility, impact, and risks | `stages/03-critical-evaluation/CONTEXT.md` |
| Score, rank, and classify ideas (MWP vs. software) | `stages/04-prioritization/CONTEXT.md` |
| Build actionable strategy and delivery plan | `stages/05-strategy/CONTEXT.md` |

## Shared Resources

| Resource | Location | Used by |
|----------|----------|---------|
| Evaluation criteria | `_config/evaluation-criteria.md` | Stages 03, 04 |
| MWP fit checklist | `_config/mwp-fit-checklist.md` | Stage 04, 05 |
| Channel alignment | `shared/channel-alignment.md` | Stages 03, 04, 05 |

## Pipeline Flow

```
Raw ideas (DMs, notes, lists)
        │
        ▼
  01-intake ──── Extract & standardize into idea cards
        │
        ▼
  02-pattern-analysis ──── Cluster, theme, find connections
        │
        ▼
  03-critical-evaluation ──── Feasibility, novelty, impact analysis
        │
        ▼
  04-prioritization ──── Score, rank, classify (MWP vs. software)
        │
        ▼
  05-strategy ──── Delivery plan, workspace specs, content alignment
```
