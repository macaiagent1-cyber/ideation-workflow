# Onboarding Questionnaire

All questions in a single pass. Answers configure the workspace permanently. These are system-level — they describe who you are and how the pipeline should weigh decisions, not the content of any specific batch of ideas.

---

## Questions

### Q1: Channel/Brand Name
What is the name of your channel or brand?

- **Placeholder:** `{{BRAND_NAME}}`
- **Files:** `shared/channel-alignment.md`
- **Type:** free text

### Q2: What does your channel do? (One sentence)
What is the mission or focus of your channel?

- **Placeholder:** `{{CHANNEL_MISSION}}`
- **Files:** `shared/channel-alignment.md`
- **Type:** free text
- **Example:** "Teaches developers how to build AI agent workflows using folder structure instead of frameworks"

### Q3: Who is your audience?
Describe your primary audience — who they are, what they care about, what they already know, and what makes them engage.

- **Placeholders:** `{{TARGET_AUDIENCE}}`, `{{AUDIENCE_CARES_ABOUT}}`, `{{AUDIENCE_KNOWLEDGE_LEVEL}}`, `{{AUDIENCE_ENGAGEMENT_DRIVERS}}`
- **Files:** `shared/channel-alignment.md`
- **Type:** free text
- **Example:** "AI-curious developers and technical creators who know programming but are new to agent orchestration. They care about practical tools over theory. They engage when they see something they can use immediately."

### Q4: Content Pillars (3-5 recurring themes)
What are the main topics your channel covers? List 3-5 pillars.

- **Placeholders:** `{{CONTENT_PILLAR_1}}` through `{{CONTENT_PILLAR_5}}`, plus per-pillar: `{{PILLAR_N_DESCRIPTION}}`, `{{PILLAR_N_AUDIENCE_FIT}}`
- **Files:** `shared/channel-alignment.md`
- **Type:** free text (comma-separated list)
- **Example:** "MWP workspace builds, Context engineering, AI workflow design, Tool reviews, Community showcases"
- **Agent derives:** Per-pillar description and audience fit from pillar names + Q3 audience
- If fewer than 4 pillars: remove `{{?PILLAR_4}}` conditional block
- If fewer than 5 pillars: remove `{{?PILLAR_5}}` conditional block

### Q5: Priority Profile
How should the pipeline weigh decisions? This determines how ideas are ranked in Stage 04.

- **Placeholders:** `{{WEIGHT_IMPACT}}`, `{{WEIGHT_FEASIBILITY}}`, `{{WEIGHT_CHANNEL}}`, `{{WEIGHT_RESEARCH}}`, `{{WEIGHT_NOVELTY}}`
- **Files:** `_config/evaluation-criteria.md`
- **Type:** selection or custom
- **Options:**
  - **Balanced** (default) — Impact 0.30, Feasibility 0.20, Channel 0.20, Research 0.20, Novelty 0.10
  - **Community-first** — Impact 0.40, Feasibility 0.25, Channel 0.15, Research 0.10, Novelty 0.10
  - **Research-driven** — Impact 0.20, Feasibility 0.15, Channel 0.20, Research 0.35, Novelty 0.10
  - **Content-driven** — Impact 0.25, Feasibility 0.15, Channel 0.35, Research 0.15, Novelty 0.10
  - **Ship fast** — Impact 0.25, Feasibility 0.35, Channel 0.20, Research 0.10, Novelty 0.10
  - **Custom** — Provide five weights summing to 1.0

### Q6: What does your community most need right now?
In one sentence, what is the biggest gap or most common request you're hearing?

- **Placeholder:** `{{COMMUNITY_CURRENT_NEED}}`
- **Files:** (used as context during Stage 03 evaluation, not placed in a file — agent remembers this)
- **Type:** free text
- **Example:** "People want to see MWP applied to their own domains but don't know how to start"

### Q7: What domains does your community work in?
List the main fields your community members come from. This helps the agent recognize domain-specific patterns in Stage 02.

- **Placeholder:** `{{COMMUNITY_DOMAINS}}`
- **Files:** (used as context during pattern analysis — agent remembers this)
- **Type:** free text (comma-separated)
- **Example:** "Software development, content creation, education, consulting, research, marketing"

---

## Post-Onboarding Process

1. **Pass 1:** Replace all direct placeholders in their target files
2. **Pass 2:** Derive per-pillar descriptions and audience fit from pillar names + audience description
3. **Scan:** Check every `.md` file for remaining `{{` patterns — resolve any that remain
4. **Confirm:** Tell the user: "Your ideation workspace is configured for {{BRAND_NAME}}. To process a batch of ideas, paste your DMs/notes and say `intake`."
