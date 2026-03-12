# Ideation Workflow

Community request analysis and workspace delivery pipeline. Takes raw ideas and requests from community DMs, analyzes patterns, evaluates feasibility, prioritizes by impact, and classifies each into MWP-workspace (deliverable as a folder-based workflow) or software-required (needs custom code/app/infrastructure). The final output is an actionable strategy that aligns deliverables with channel content and the MWP research paper.

## Folder Map

```
ideation-workflow/
├── CLAUDE.md                          (you are here)
├── CONTEXT.md                         (task routing)
├── setup/
│   └── questionnaire.md               (one-time onboarding)
├── _config/
│   ├── evaluation-criteria.md          (scoring dimensions for ideas)
│   └── mwp-fit-checklist.md            (criteria for MWP vs. software)
├── shared/
│   └── channel-alignment.md            (content pillars and audience)
└── stages/
    ├── 01-intake/
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   ├── extraction-format.md    (standardized idea card format)
    │   │   └── dedup-rules.md          (how to handle overlapping ideas)
    │   └── output/
    ├── 02-pattern-analysis/
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   └── clustering-guide.md     (how to identify and name patterns)
    │   └── output/
    ├── 03-critical-evaluation/
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   └── analysis-framework.md   (structured evaluation approach)
    │   └── output/
    ├── 04-prioritization/
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   └── scoring-rubric.md       (how to score and rank)
    │   └── output/
    └── 05-strategy/
        ├── CONTEXT.md
        ├── references/
        │   └── delivery-templates.md   (strategy document format)
        └── output/
```

## Naming

- Folders and files: `lowercase-with-hyphens`
- Stage folders: zero-padded `01-`, `02-`, etc.
- Output artifacts: `[batch-slug]-[artifact-type].md`

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run onboarding questionnaire in `setup/questionnaire.md` |
| `status` | Show pipeline completion for current batch |
| `intake` | Start Stage 01 with new batch of ideas |
