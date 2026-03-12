# Stage 03 — Critical Evaluation

Take the pattern map from Stage 02 and deeply evaluate each cluster and its constituent ideas. Assess feasibility, impact, novelty, audience value, and alignment with channel content and the MWP research. This stage produces the evidence that Stage 04 uses to score and rank.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Previous stage | `../02-pattern-analysis/output/` | Most recent pattern map (full) | Clusters to evaluate |
| Previous stage | `../01-intake/output/` | Most recent idea cards (full) | Original detail for each idea |
| Config | `../../_config/evaluation-criteria.md` | Full file | Dimensions to evaluate against |
| Shared | `../../shared/channel-alignment.md` | Full file | Channel pillars, audience, and research alignment |
| Reference | `references/analysis-framework.md` | Full file | How to structure the evaluation |

## Process

1. Read pattern map from `../02-pattern-analysis/output/`
2. Read original idea cards from `../01-intake/output/` for full detail
3. For each cluster, write an evaluation brief following `analysis-framework.md`:
   - Feasibility assessment (what would it take to build?)
   - Impact assessment (how many people does this serve? how much value?)
   - Novelty assessment (does this exist already? what's the differentiation?)
   - Channel alignment (does this reinforce content pillars? generate content?)
   - Research alignment (does this advance or demonstrate the MWP thesis?)
   - Risk assessment (what could go wrong? what's the downside of attempting this?)
4. For orphan ideas, write individual evaluation briefs (same dimensions, shorter)
5. Flag any cluster where evaluation reveals it should be split or merged differently
6. **[Checkpoint]** Present evaluation briefs to user
   - User validates assessments match their domain knowledge
   - User adds context the agent couldn't know (e.g., "that already exists" or "this person is a key community member")
   - User flags disagreements with feasibility or impact reads
7. Incorporate user feedback into evaluations
8. Run audit checks
9. Save to output/

## Checkpoint

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 6 | Evaluation briefs for each cluster and orphan, with feasibility/impact/novelty/alignment/risk | Validate assessments, add domain context, flag disagreements |

## Audit

| Check | Pass Condition |
|-------|---------------|
| Full coverage | Every cluster and orphan from Stage 02 has an evaluation brief |
| All dimensions | Every brief addresses all six evaluation dimensions |
| Evidence-based | Feasibility claims reference concrete requirements (time, skills, tools) not vague feelings |
| Honest risks | Every brief includes at least one genuine risk or downside |
| Channel connection | Every brief explicitly states how it relates (or doesn't) to channel content |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Evaluation report | `output/[batch-slug]-evaluations.md` | Markdown with per-cluster and per-orphan evaluation briefs |
