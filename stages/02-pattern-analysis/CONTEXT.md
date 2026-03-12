# Stage 02 — Pattern Recognition & Grouping

Read the idea card catalog from Stage 01. Identify recurring themes, cluster related ideas into groups, name the patterns, and surface the underlying needs driving multiple requests.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Previous stage | `../01-intake/output/` | Most recent idea cards file (full) | The ideas to analyze |
| Reference | `references/clustering-guide.md` | Full file | How to identify and name clusters |
| Shared | `../../shared/channel-alignment.md` | "Content Pillars" section | Map clusters to existing pillars |

## Process

1. Read all idea cards from `../01-intake/output/`
2. Read through every card and note recurring domains, problems, and request types
3. Identify natural clusters — groups of 2+ ideas that share a common underlying need
4. Name each cluster with a descriptive theme label (see `clustering-guide.md`)
5. For each cluster, write:
   - Theme name and one-sentence description
   - Which idea card IDs belong to it
   - The underlying need that connects them
   - How this theme maps to existing content pillars (if at all)
6. Identify orphan ideas — cards that don't fit any cluster
7. Note cross-cluster connections (ideas that bridge two themes)
8. **[Checkpoint]** Present cluster map to user
   - User validates groupings make sense
   - User can rename themes, move ideas between clusters, or split/merge clusters
9. Incorporate feedback
10. Run audit checks
11. Save to output/

## Checkpoint

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 8 | Cluster map: theme names, member ideas, underlying needs, pillar alignment | Validate groupings, rename themes, adjust membership |

## Audit

| Check | Pass Condition |
|-------|---------------|
| Full coverage | Every idea card from Stage 01 appears in exactly one cluster or is marked as orphan |
| No empty clusters | Every cluster contains at least 2 idea cards |
| Named needs | Every cluster has a one-sentence underlying need statement |
| Pillar mapping | Every cluster notes whether it aligns with an existing content pillar or represents a new one |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Pattern map | `output/[batch-slug]-pattern-map.md` | Markdown with named clusters, member IDs, underlying needs, pillar alignment, orphans |
