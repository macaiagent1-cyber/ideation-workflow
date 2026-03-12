# Delivery Strategy Format

## MWP Workspace Outline

For each MWP-track item, produce:

```markdown
### [Workspace Name]

**Serves:** [Which cluster/ideas this addresses]
**Pipeline:** [Input] → [Stage 1 purpose] → [Stage 2 purpose] → ... → [Final output]
**Stage count:** [N]
**Stages:**
1. **[Stage name]** — [What it does, one sentence]
2. **[Stage name]** — [What it does, one sentence]
...

**Scope:** [Workspace-builder compatible / Custom design required]
**Estimated effort:** [Hours/days to build and test]
**Community handoff:** [How this gets delivered — shared as folder, walkthrough video, etc.]

**Content opportunities:**
- [ ] Build walkthrough (process of creating the workspace)
- [ ] Demo video (running the workspace end to end)
- [ ] Use-case story (community member using it to solve their problem)
- [ ] Research angle (how this demonstrates the MWP/ICM thesis)
```

## Software Outline

For each Software-track item, produce:

```markdown
### [Project Name]

**Serves:** [Which cluster/ideas this addresses]
**What it is:** [One paragraph describing the deliverable]
**Technical approach:** [Stack, key components, integrations]
**Key decisions:** [2-3 technical choices that need to be made early]

**MWP components:** [Any parts of the workflow that could be MWP workspaces feeding into the software]
**Estimated effort:** [Rough scope — small/medium/large]
**Dependencies:** [What needs to exist before this can be built?]

**Content opportunities:**
- [ ] Build log / dev diary
- [ ] Technical deep-dive
- [ ] Community beta program
```

## Delivery Sequence Format

```markdown
## Delivery Sequence

### Phase 1: Quick Wins (Target: [timeframe])
1. **[Name]** — [MWP/Software] — [Why first: high impact + low effort]
2. ...

### Phase 2: High Impact (Target: [timeframe])
3. **[Name]** — [MWP/Software] — [Why this phase: high value, moderate effort]
4. ...

### Phase 3: Strategic Bets (Target: [timeframe])
5. **[Name]** — [MWP/Software] — [Why later: high effort or dependent on earlier work]
6. ...

### Parked
- **[Name]** — [Why parked: low priority, blocked, or needs more research]
```

## Content Plan Format

```markdown
## Content Alignment

| Deliverable | Content Piece | Pillar | Thesis Connection |
|-------------|--------------|--------|-------------------|
| [Workspace/project name] | [Type: walkthrough/demo/story] | [Pillar name] | [How it demonstrates MWP/ICM] |
```
