# Deduplication Rules

## When Two Ideas Are the Same

Merge when: The core request is functionally identical — the same system, tool, or workflow would satisfy both.

Keep separate when: They share a domain but the actual deliverable would be different. "Automate my newsletter" and "Help me write better newsletters" sound similar but are different requests (automation vs. quality).

## Merge Protocol

1. Keep the card with the richer description as the primary
2. Append the other card's raw quote under a `**Also requested by:**` field
3. Update **Recurrence** to reflect multiple sources
4. If one card had more specificity, fold those details into the primary card's core request

## Near-Duplicate Handling

If ideas are related but not identical (e.g., "podcast production workflow" and "podcast editing automation"), keep both but link them: `**Related:** ID-XXX (overlapping domain, different scope)`

These relationships feed into Stage 02 pattern analysis.

## Subsumption

If idea A is a subset of idea B (e.g., "email subject line generator" is a subset of "full email marketing workflow"), keep both. Tag: `**Subsumes:** ID-XXX` on the larger idea and `**Subsumed by:** ID-YYY` on the smaller one. Both survive — the smaller one might be deliverable faster even if the larger one is higher priority.
