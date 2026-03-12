# Stage 04 — Prioritization & Classification

Take the evaluation report from Stage 03 and produce two outputs: a ranked priority list (most to least important) and a classification of each idea as MWP-workspace or software-required.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Previous stage | `../03-critical-evaluation/output/` | Most recent evaluations (full) | Evidence for scoring |
| Previous stage | `../02-pattern-analysis/output/` | Most recent pattern map (full) | Cluster structure |
| Config | `../../_config/evaluation-criteria.md` | Full file | Scoring weights |
| Config | `../../_config/mwp-fit-checklist.md` | Full file | MWP vs. software classification criteria |
| Shared | `../../shared/channel-alignment.md` | "Content Pillars" and "Strategic Goals" sections | Alignment weighting |
| Reference | `references/scoring-rubric.md` | Full file | How to apply scores |

## Process

1. Read evaluations from `../03-critical-evaluation/output/`
2. Score each cluster and orphan across all dimensions using `scoring-rubric.md`
3. Apply weights from `evaluation-criteria.md` to produce a composite score
4. Rank all ideas from highest to lowest composite score
5. For each idea, run the MWP fit checklist from `mwp-fit-checklist.md`:
   - Ideas that pass: classify as **MWP Workspace** (deliverable as folder-based workflow)
   - Ideas that fail: classify as **Software Required** (needs custom code/app/infrastructure)
   - Ideas that partially pass: classify as **Hybrid** (MWP core + software components)
6. Produce two ranked lists: MWP-track and Software-track
7. **[Checkpoint]** Present ranked and classified lists to user
   - User validates priority order matches their strategic judgment
   - User can override classifications or re-rank based on context agent doesn't have
   - User confirms top 3-5 priorities for the strategy stage
8. Incorporate feedback
9. Run audit checks
10. Save to output/

## Checkpoint

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 7 | Two ranked lists (MWP-track, Software-track) with scores and classifications | Validate rankings, override classifications, confirm top priorities |

## Audit

| Check | Pass Condition |
|-------|---------------|
| Full coverage | Every cluster and orphan from Stage 03 has a score and classification |
| Scoring transparency | Every score shows how it was calculated (dimension scores + weights = composite) |
| Classification rationale | Every MWP/Software/Hybrid classification cites specific checklist items |
| Rank consistency | No lower-scored idea ranks above a higher-scored idea without explicit user override noted |
| Two-track split | Final output has two clean lists: MWP-track and Software-track (hybrids appear in both with notes) |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Priority & classification report | `output/[batch-slug]-priorities.md` | Markdown with scored rankings, two-track classification, user overrides noted |
