# Stage 01 — Idea Intake & Extraction

Take raw community requests (DMs, notes, voice transcripts, bullet lists) and extract each distinct idea into a standardized idea card. Merge duplicates. Tag source and requester where known.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| User | (conversation) | Raw ideas — paste of DMs, notes, lists | Starting material |
| Reference | `references/extraction-format.md` | Full file | Idea card format and field definitions |
| Reference | `references/dedup-rules.md` | Full file | How to handle overlapping/duplicate ideas |

## Process

1. Read all raw input material provided by the user
2. Identify every distinct idea, request, or problem statement — one per card
3. For each idea, fill out an idea card following the format in `extraction-format.md`
4. Scan for duplicates and near-duplicates using rules in `dedup-rules.md`
5. Merge duplicates — keep the richest description, note all sources
6. Number each surviving idea card sequentially (ID-001, ID-002, etc.)
7. **[Checkpoint]** Present the full list of extracted idea cards to the user
   - User confirms all ideas captured
   - User flags any that were missed or mis-extracted
   - User can add ideas not in the original material
8. Incorporate user feedback, re-number if needed
9. Run audit checks
10. Save to output/

## Checkpoint

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 7 | Full list of idea cards with IDs, titles, and one-line summaries | Confirm completeness, flag missed ideas, add new ones |

## Audit

| Check | Pass Condition |
|-------|---------------|
| No orphaned input | Every distinct idea from raw input appears in at least one card |
| Card completeness | Every card has all required fields from extraction-format.md filled |
| No duplicates | No two cards describe the same core request |
| Source attribution | Every card notes where the idea came from (DM, conversation, user-added) |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Idea card catalog | `output/[batch-slug]-idea-cards.md` | Markdown with numbered idea cards |
