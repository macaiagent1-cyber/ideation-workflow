# Scoring Rubric

## How to Score

Each idea (cluster or orphan) receives a score from 1-5 on each evaluation dimension. Scores are not gut feelings — they map to specific evidence from the Stage 03 evaluation briefs.

## Dimension Scores

### Impact (weight from evaluation-criteria.md)

| Score | Meaning |
|-------|---------|
| 5 | Serves many community members, fundamentally changes how they work, urgent need |
| 4 | Serves multiple members, significant value, clear demand |
| 3 | Serves a segment, useful but not transformative |
| 2 | Serves few people or provides marginal improvement |
| 1 | Niche request, minimal practical value |

### Feasibility (weight from evaluation-criteria.md)

| Score | Meaning |
|-------|---------|
| 5 | Can be delivered quickly with existing skills and tools |
| 4 | Moderate effort, clear path to delivery |
| 3 | Significant effort but achievable |
| 2 | Major effort, uncertain path, or requires new capabilities |
| 1 | Extremely difficult, requires infrastructure/skills not currently available |

### Channel Alignment (weight from evaluation-criteria.md)

| Score | Meaning |
|-------|---------|
| 5 | Directly reinforces core content pillar, generates multiple content pieces, demonstrates thesis |
| 4 | Aligns with existing pillar, generates content, strengthens brand |
| 3 | Tangentially related, some content potential |
| 2 | Weak connection to channel content |
| 1 | No meaningful channel alignment |

### Research Alignment (weight from evaluation-criteria.md)

| Score | Meaning |
|-------|---------|
| 5 | Perfect MWP case study — demonstrates the thesis, could appear in the paper |
| 4 | Strong MWP fit, advances the body of workspace examples |
| 3 | Partial MWP fit, or demonstrates adjacent principles |
| 2 | Loose connection to MWP thesis |
| 1 | No research relevance |

### Novelty (weight from evaluation-criteria.md)

| Score | Meaning |
|-------|---------|
| 5 | Nothing like this exists. Genuinely new approach |
| 4 | Exists in crude form; this version would be meaningfully better |
| 3 | Alternatives exist but serve a different audience or approach |
| 2 | Good alternatives exist; marginal differentiation |
| 1 | Well-solved problem, building this adds nothing new |

## Composite Score

```
Composite = (Impact × W_impact) + (Feasibility × W_feasibility) + (Channel × W_channel) + (Research × W_research) + (Novelty × W_novelty)
```

Weights come from `../../_config/evaluation-criteria.md`. They are set during onboarding and reflect the user's strategic priorities.

## Tie-Breaking

When two ideas have the same composite score:
1. Higher Impact score wins
2. If still tied, higher Channel Alignment wins
3. If still tied, higher Feasibility wins (ship faster)
4. If still tied, user decides at checkpoint
