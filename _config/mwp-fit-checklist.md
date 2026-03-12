# MWP Fit Checklist

Use this checklist to classify each idea as **MWP Workspace**, **Software Required**, or **Hybrid**.

## Core MWP Fit Criteria

An idea is a good MWP workspace candidate when the workflow it describes is:

### Must-Have (all required for MWP classification)

- [ ] **Sequential** — The work follows a clear step-by-step order (Stage 1 → Stage 2 → Stage 3)
- [ ] **Human-reviewable** — A person should check and possibly edit the output at each stage boundary
- [ ] **Repeatable** — The same pipeline runs multiple times with different input (not a one-off task)
- [ ] **Text-based I/O** — The inputs and outputs at each stage can be represented as markdown or JSON

### Strong Signals (not required, but strengthen the case)

- [ ] **Configurable** — The workflow has system-level settings (voice, style, format) that persist across runs
- [ ] **Decomposable** — The workflow naturally breaks into 3-7 distinct stages with clear boundaries
- [ ] **Domain-specific** — The workflow serves a specific domain that benefits from codified reference material
- [ ] **Edit surfaces matter** — The intermediate outputs are things a human would genuinely want to read and tweak
- [ ] **No real-time requirements** — The workflow doesn't need instant responses or live data streams

### Disqualifiers (any one means NOT MWP)

- [ ] **Requires live API integration** — Needs to call external services during pipeline execution (unless via MCP)
- [ ] **Requires concurrent processing** — Multiple steps must happen in parallel, not sequentially
- [ ] **Requires persistent state** — Needs a database, user accounts, or state that survives beyond the filesystem
- [ ] **Requires a UI** — The deliverable is an interactive application, not a document or workflow output
- [ ] **Requires real-time data** — The workflow depends on live feeds, streaming data, or time-sensitive information

## Classification Decision

| All Must-Haves | No Disqualifiers | Classification |
|----------------|------------------|----------------|
| Yes | Yes | **MWP Workspace** |
| Yes | Partial (1 disqualifier) | **Hybrid** — MWP core + software component for the disqualified part |
| No | - | **Software Required** |

## Hybrid Boundary Drawing

For Hybrid items, identify:
1. **MWP portion** — The sequential, reviewable stages that can live in folders
2. **Software portion** — The component that requires code (API integration, UI, database, etc.)
3. **Interface point** — Where does the MWP pipeline hand off to software, or vice versa?

Example: A "client report automation" might be Hybrid — the research and writing stages are MWP, but the final delivery via email requires a script.

## Channel & Paper Value

Ideas classified as MWP Workspace have bonus strategic value:
- Each workspace built is a **case study** for the MWP/ICM research paper
- Each workspace delivered is **content** for the channel (build process, demo, use-case story)
- Each workspace used by the community **validates the thesis** that folder structure replaces frameworks
- Each workspace handed off **demonstrates portability** — the key MWP advantage

Note this value in the Stage 04 evaluation, but don't let it override honest classification. An idea that doesn't fit MWP shouldn't be forced into it just because MWP workspaces have strategic value.
