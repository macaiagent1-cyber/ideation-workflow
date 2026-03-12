# Ideation Workflow

A 5-stage AI workflow that takes a pile of raw ideas, feature requests, or community DMs and turns them into a prioritized, classified delivery strategy. Built on the [Interpretable Context Methodology (ICM)](https://github.com/RinDig/Model-Workspace-Protocol-MWP-) — folder structure as agent architecture.

No framework. No code. Just folders, markdown files, and one AI agent reading the right context at the right moment.

---

## What It Does

```
Raw ideas (DMs, notes, braindumps)
        │
        ▼
  01 Intake ────────────── Extract & standardize into idea cards
        │
        ▼
  02 Pattern Analysis ──── Cluster by theme, find connections
        │
        ▼
  03 Critical Evaluation ── Feasibility, impact, risk analysis
        │
        ▼
  04 Prioritization ────── Score, rank, classify (MWP vs. Software)
        │
        ▼
  05 Strategy ──────────── Delivery plan + content alignment
```

**Two output tracks:**

- **MWP Track** — Ideas that can be delivered as folder-based AI workspaces (sequential, human-reviewed, repeatable workflows)
- **Software Track** — Ideas that need custom code, apps, or infrastructure

Each stage produces a plain markdown file you can read, edit, and approve before the next stage runs.

---

## Quick Start

### Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed
- A batch of ideas to process (DMs, notes, bullet lists — any format)

### Setup (one time)

```bash
cd ideation-workflow
# Open Claude Code, then type:
setup
```

You'll answer 7 questions about your channel, audience, content pillars, and how you want ideas prioritized. This configures the workspace permanently — you only do it once.

### Run the Pipeline

```bash
# Paste your ideas and type:
intake
```

Then walk through each stage:

1. **Review the idea cards** — Make sure every idea was captured. Add any that were missed.
2. **Review the pattern map** — Check that clusters make sense. Rename or reorganize if needed.
3. **Review the evaluations** — Add context the agent couldn't know. Flag disagreements.
4. **Review the rankings** — Override any scores that don't match your judgment. Confirm top priorities.
5. **Review the strategy** — Approve the delivery plan and content alignment.

At each stage, the agent pauses and shows you what it produced. You edit, approve, or redirect. The next stage reads whatever you left there.

---

## Folder Structure

```
ideation-workflow/
├── CLAUDE.md                     # Workspace identity (auto-loaded)
├── CONTEXT.md                    # Task routing to stages
├── README.md                     # You are here
│
├── setup/
│   └── questionnaire.md          # One-time onboarding (7 questions)
│
├── _config/                      # Scoring weights and classification criteria
│   ├── evaluation-criteria.md    # How dimensions are weighted
│   └── mwp-fit-checklist.md      # MWP vs. Software decision rules
│
├── shared/                       # Cross-stage resources
│   └── channel-alignment.md      # Content pillars, audience, goals
│
└── stages/
    ├── 01-intake/                # Raw ideas → standardized idea cards
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   ├── extraction-format.md
    │   │   └── dedup-rules.md
    │   └── output/
    │
    ├── 02-pattern-analysis/      # Idea cards → themed clusters
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   └── clustering-guide.md
    │   └── output/
    │
    ├── 03-critical-evaluation/   # Clusters → feasibility/impact briefs
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   └── analysis-framework.md
    │   └── output/
    │
    ├── 04-prioritization/        # Briefs → scored rankings + MWP/Software classification
    │   ├── CONTEXT.md
    │   ├── references/
    │   │   └── scoring-rubric.md
    │   └── output/
    │
    └── 05-strategy/              # Rankings → delivery plan + content calendar
        ├── CONTEXT.md
        ├── references/
        │   └── delivery-templates.md
        └── output/
```

---

## The Five Stages

### Stage 01 — Intake

**Input:** Raw ideas in any format (DMs, bullet lists, voice transcripts, notes)

**What it does:**
- Extracts every distinct idea into a standardized "idea card"
- Merges duplicates, links related ideas
- Tags each with source, domain, and initial complexity/recurrence signals

**Output:** Numbered catalog of idea cards

**Your job:** Confirm all ideas were captured. Add any the agent missed.

---

### Stage 02 — Pattern Analysis

**Input:** Idea card catalog from Stage 01

**What it does:**
- Groups related ideas into clusters by shared need
- Names each cluster with a descriptive theme
- Maps clusters to your content pillars
- Identifies orphan ideas and cross-cluster connections

**Output:** Pattern map with named clusters and membership

**Your job:** Validate groupings. Rename themes. Move ideas between clusters if they're misplaced.

---

### Stage 03 — Critical Evaluation

**Input:** Pattern map from Stage 02 + original idea cards from Stage 01

**What it does:**
- Evaluates each cluster on six dimensions:
  - **Feasibility** — What would it take to build?
  - **Impact** — How many people does this serve? How deeply?
  - **Novelty** — Does this exist already?
  - **Channel Alignment** — Does this generate content and reinforce the brand?
  - **Research Alignment** — Does this demonstrate the MWP/ICM thesis?
  - **Risk** — What could go wrong?

**Output:** Evaluation briefs for every cluster and orphan

**Your job:** Add domain knowledge the agent couldn't have. Flag assessment errors.

---

### Stage 04 — Prioritization

**Input:** Evaluation briefs from Stage 03

**What it does:**
- Scores each idea across all dimensions (1-5 scale)
- Applies your priority weights to produce composite rankings
- Classifies each idea using the MWP fit checklist:
  - **MWP Workspace** — Sequential, reviewable, repeatable, text-based → build as a folder workflow
  - **Software Required** — Needs APIs, databases, UI, or real-time processing → build as code
  - **Hybrid** — MWP core + software component

**Output:** Two ranked lists (MWP track + Software track)

**Your job:** Override rankings where your judgment disagrees. Confirm top 3-5 priorities.

---

### Stage 05 — Strategy

**Input:** Prioritized and classified list from Stage 04

**What it does:**
- For MWP items: outlines the workspace (stages, pipeline, scope estimate)
- For Software items: outlines the technical approach (stack, integrations, key decisions)
- Sequences delivery order (quick wins first, then high-impact, then strategic bets)
- Maps each deliverable to content opportunities (build walkthrough, demo, use-case story)

**Output:** Delivery strategy with workspace specs, software specs, and content plan

**Your job:** Approve the plan. Adjust scope. Start building.

---

## Priority Profiles

During setup, you choose how dimensions are weighted:

| Profile | Impact | Feasibility | Channel | Research | Novelty |
|---------|--------|-------------|---------|----------|---------|
| **Balanced** (default) | 0.30 | 0.20 | 0.20 | 0.20 | 0.10 |
| **Community-first** | 0.40 | 0.25 | 0.15 | 0.10 | 0.10 |
| **Research-driven** | 0.20 | 0.15 | 0.20 | 0.35 | 0.10 |
| **Content-driven** | 0.25 | 0.15 | 0.35 | 0.15 | 0.10 |
| **Ship fast** | 0.25 | 0.35 | 0.20 | 0.10 | 0.10 |

You can also provide custom weights.

---

## MWP Classification

The pipeline automatically classifies each idea as MWP-fit or software-required based on four criteria:

An idea fits MWP when the workflow is:
- **Sequential** — Clear step-by-step order
- **Human-reviewable** — A person should check output at each stage
- **Repeatable** — Same pipeline runs multiple times with different input
- **Text-based I/O** — Inputs and outputs are markdown/JSON

Ideas that need live APIs, concurrent processing, persistent databases, interactive UIs, or real-time data get classified as Software Required.

---

## Editing Between Stages

Every stage writes its output to an `output/` folder as a plain markdown file. Before the next stage runs, you can:

- **Edit the file directly** — Fix anything, add context, remove ideas
- **Leave it as-is** — If the output looks good, just proceed
- **Re-run the stage** — If the output is fundamentally wrong, re-run with different guidance

The next stage reads whatever you left in the output folder. This is the core MWP principle: every intermediate output is an edit surface.

---

## Running Multiple Batches

Each run uses a batch slug (e.g., `march-2026-dms`). Output files are named `[batch-slug]-[artifact].md`. To process a new batch of ideas, just paste new input and say `intake` — previous batch outputs remain in their folders.

---

## Built With

This workspace follows the [Interpretable Context Methodology (ICM)](https://github.com/RinDig/Model-Workspace-Protocol-MWP-) — a method for orchestrating AI agent workflows using folder structure instead of framework code. One agent reads the right files at the right moment. The folder hierarchy is the orchestration logic.

For the full methodology, see the [ICM paper](https://github.com/RinDig/Model-Workspace-Protocol-MWP-).

---

## License

MIT
