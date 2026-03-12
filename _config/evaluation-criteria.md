# Evaluation Criteria & Weights

These weights determine how the five scoring dimensions combine into a composite priority score. They reflect strategic priorities set during onboarding.

## Scoring Dimensions

| Dimension | Weight | What It Measures |
|-----------|--------|-----------------|
| Impact | {{WEIGHT_IMPACT}} | How many people this serves and how deeply |
| Feasibility | {{WEIGHT_FEASIBILITY}} | How quickly and realistically this can be delivered |
| Channel Alignment | {{WEIGHT_CHANNEL}} | How well this reinforces content pillars and brand |
| Research Alignment | {{WEIGHT_RESEARCH}} | How well this demonstrates or advances the MWP/ICM thesis |
| Novelty | {{WEIGHT_NOVELTY}} | How differentiated this is from existing solutions |

## Weight Guidelines

Weights must sum to 1.0. Default configuration:

| Priority Profile | Impact | Feasibility | Channel | Research | Novelty |
|-----------------|--------|-------------|---------|----------|---------|
| **Balanced** (default) | 0.30 | 0.20 | 0.20 | 0.20 | 0.10 |
| **Community-first** | 0.40 | 0.25 | 0.15 | 0.10 | 0.10 |
| **Research-driven** | 0.20 | 0.15 | 0.20 | 0.35 | 0.10 |
| **Content-driven** | 0.25 | 0.15 | 0.35 | 0.15 | 0.10 |
| **Ship fast** | 0.25 | 0.35 | 0.20 | 0.10 | 0.10 |

The user selects a profile during onboarding (Q3 in questionnaire) or provides custom weights.

## How Weights Are Applied

```
Composite = (Impact × W_impact) + (Feasibility × W_feasibility) + (Channel × W_channel) + (Research × W_research) + (Novelty × W_novelty)
```

Maximum possible composite score: 5.0
Minimum: 1.0

## Strategic Override

The user can override any ranking at the Stage 04 checkpoint. Overrides are noted in the output with rationale. The scoring provides a starting point for discussion, not a final answer.
