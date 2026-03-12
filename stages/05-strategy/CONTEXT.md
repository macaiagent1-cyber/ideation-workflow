# Stage 05 — Strategy & Delivery Plan

Take the prioritized and classified list from Stage 04 and produce an actionable delivery strategy. For MWP-track items, outline the workspace that would be built. For Software-track items, outline the technical approach. Align everything to a content calendar that reinforces the channel.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Previous stage | `../04-prioritization/output/` | Most recent priorities file (full) | Ranked and classified ideas |
| Previous stage | `../01-intake/output/` | Most recent idea cards (full) | Original detail for deliverable specs |
| Config | `../../_config/mwp-fit-checklist.md` | Full file | MWP workspace requirements |
| Shared | `../../shared/channel-alignment.md` | Full file | Pillars, audience, goals |
| Reference | `references/delivery-templates.md` | Full file | Strategy document format |

## Process

1. Read priorities from `../04-prioritization/output/`
2. For each **MWP-track** item (starting from highest priority):
   - Outline the workspace: how many stages, what each stage does, what the pipeline transforms
   - Note which content pillar it feeds and what channel content the build process would generate
   - Estimate scope: can it be built with the workspace-builder, or does it need custom design?
   - Note what community value it delivers and how it would be handed off
3. For each **Software-track** item (starting from highest priority):
   - Outline the technical approach: what needs to be built, what stack, what integrations
   - Note whether any MWP components could handle part of the workflow
   - Estimate scope and key technical decisions
4. For **Hybrid** items: split into MWP portion and software portion with clear boundaries
5. Sequence the delivery order:
   - Quick wins first (high impact, low effort, MWP-track)
   - Then high-impact items that take longer
   - Group items that share infrastructure or can be built together
6. Map deliverables to a content plan:
   - Each MWP workspace build can generate: a build walkthrough, a demo, a use-case story
   - Each delivery reinforces the thesis: "folder structure as agent architecture"
7. **[Checkpoint]** Present strategy to user
   - User validates delivery sequence
   - User confirms content plan alignment
   - User approves or adjusts scope for top priorities
8. Incorporate feedback
9. Run audit checks
10. Save to output/

## Checkpoint

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 7 | Full strategy: MWP workspace outlines, software specs, delivery sequence, content plan | Validate sequence, adjust scope, approve top priorities for execution |

## Audit

| Check | Pass Condition |
|-------|---------------|
| Full coverage | Every item from Stage 04's top priorities has a delivery outline |
| MWP workspace specs | Every MWP-track item has: stage count, stage purposes, pipeline transformation, scope estimate |
| Software specs | Every Software-track item has: technical approach, stack, key decisions |
| Delivery sequence | Items are ordered with rationale (not just priority score — considers dependencies and quick wins) |
| Content mapping | At least the top 5 deliverables have associated content plan entries |
| Thesis reinforcement | Strategy explicitly notes which deliverables demonstrate the MWP/ICM thesis |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Delivery strategy | `output/[batch-slug]-strategy.md` | Markdown with workspace outlines, software specs, delivery sequence, content plan |
