# Delivery Strategy — community-dms-2026-03

**Batch:** Community DMs, March 2026
**Finalized:** 2026-03-12
**Delivery tracks:** 3 phases + parked items
**Content pieces mapped:** 14

---

## MWP Workspace Outlines

### Invoice Template Automation

**Serves:** ID-010 (Luke S, Miles Still)
**Pipeline:** Client details (JSON/markdown) → Validate fields → Map to template → Generate formatted invoice → Human review
**Stage count:** 4
**Stages:**
1. **Intake** — Accept client name, billing address, line items, date, invoice number as structured input
2. **Validation** — Check required fields, flag missing data, normalize formatting
3. **Template merge** — Inject variables into invoice template (markdown or HTML-based)
4. **Output** — Produce final invoice as markdown, PDF-ready HTML, or CSV

**Scope:** Workspace-builder compatible. This is the simplest possible MWP workspace.
**Estimated effort:** 2–4 hours
**Community handoff:** Shared as a folder. User drops in their own template and runs the pipeline.

**Content opportunities:**
- [x] Build walkthrough — "Build an invoice automation workspace in 30 minutes"
- [x] Demo video — Run the workspace end-to-end with a real invoice
- [x] Use-case story — Luke S / Miles Still replacing manual QuickBooks entry
- [x] Research angle — Simplest possible MWP proof: template + variable swap, no framework needed

---

### Text-to-Invoice from Field Reports

**Serves:** ID-009 (Carlie Rioux, Adam Daniels, Noah Taylor)
**Pipeline:** Raw foreman text messages → Extract structured data (hours, scope, line items) → Map to invoice fields → Generate invoice → Human review
**Stage count:** 5
**Stages:**
1. **Intake** — Paste or import raw text messages from foreman
2. **Extraction** — Parse unstructured text into structured line items (hours, tasks, rates)
3. **Validation** — Human reviews extracted data, corrects any parsing errors
4. **Template merge** — Inject validated data into invoice template
5. **Output** — Produce final editable invoice

**Scope:** Workspace-builder compatible. The extraction stage is the only non-trivial part — relies on Claude's text parsing.
**Estimated effort:** 4–8 hours
**Community handoff:** Shared as folder. User customizes extraction rules and invoice template.

**Content opportunities:**
- [x] Build walkthrough — "Turn messy field texts into clean invoices with MWP"
- [x] Demo video — Feed real foreman texts, show the extraction, show the invoice
- [x] Use-case story — Construction/field services contractor workflow
- [x] Research angle — MWP handles unstructured-to-structured data transformation without custom code

---

### ESG & Financial Report Generator

**Serves:** ID-023 (Shivam Sen)
**Pipeline:** Raw financial/ESG data → Validate and structure → Map to report sections → Generate narrative per section → Assemble final report → Human review
**Stage count:** 5
**Stages:**
1. **Intake** — Accept raw data (CSV, JSON, or structured markdown)
2. **Structure** — Organize data into report sections (environmental, social, governance / income, expenses, ratios)
3. **Narrative generation** — Produce written analysis per section using data + context files
4. **Assembly** — Combine sections into final report following template
5. **Output** — Formatted report ready for stakeholder review

**Scope:** Workspace-builder compatible. Report template and section definitions live in reference files.
**Estimated effort:** 1–2 days
**Community handoff:** Shared as folder. User provides their own data and customizes report template/sections.

**Content opportunities:**
- [x] Build walkthrough — "Template-driven reporting with MWP"
- [ ] Demo video — ESG-specific demo may have narrow appeal
- [x] Research angle — MWP handles structured data → narrative report, a common business workflow

---

### SKILLS.MD Extension for Client Web Design

**Serves:** ID-028 (Daniel Hernandez)
**Pipeline:** Client brief → Design analysis → Marketing/lead gen recommendations → Deliverable spec → Human review
**Stage count:** 4
**Stages:**
1. **Client intake** — Structured brief capturing client's business, audience, goals
2. **Design analysis** — Evaluate current site against design heuristics and accessibility standards
3. **Marketing expansion** — Generate lead gen and marketing tool recommendations based on client profile
4. **Deliverable spec** — Produce actionable recommendations document for the client

**Scope:** Workspace-builder compatible. Extends an existing workspace the requester already uses.
**Estimated effort:** 4–8 hours (extending existing work)
**Community handoff:** Direct collaboration with Daniel Hernandez. The build process itself is the case study.

**Content opportunities:**
- [x] Use-case story — "A community member already using MWP, and we're making it better"
- [x] Research angle — Real-world MWP adoption. Someone chose this approach independently.
- [ ] Build walkthrough — More of a collaboration/extension story than a from-scratch build

---

### Design Ideation Tool

**Serves:** ID-027 (M G)
**Pipeline:** Stakeholder request → Research competitors & best practices → Generate 3–5 design options → Evaluate each against heuristics → Recommend with rationale → Human review
**Stage count:** 5
**Stages:**
1. **Request intake** — Capture stakeholder requirements, constraints, audience
2. **Research** — Pull from reference files: competitor patterns, accessibility guidelines, heuristics, best practices
3. **Option generation** — Produce 3–5 distinct design approaches with rationale for each
4. **Evaluation** — Score each option against accessibility, heuristics, stakeholder fit
5. **Recommendation** — Final recommendation with supporting evidence and checklist

**Scope:** Workspace-builder compatible. All heuristics, checklists, and best practices live as reference markdown files.
**Estimated effort:** 1–2 days
**Community handoff:** Shared as folder. User adds their own heuristics/checklists to reference files.

**Content opportunities:**
- [x] Build walkthrough — "Context engineering for design: how reference files replace tribal knowledge"
- [x] Demo video — Run with a real stakeholder request, show 5 generated options
- [x] Research angle — Pure context engineering demo. The value is in the reference files, not the code.

---

### University Course Builder

**Serves:** ID-018 (Ann S)
**Pipeline:** Course topic + target audience → Research learning objectives → Generate syllabus structure → Build lesson plans per module → Generate assessments → Human review at each stage
**Stage count:** 6
**Stages:**
1. **Course intake** — Subject, level, duration, prerequisites, target audience
2. **Learning objectives** — Generate measurable learning outcomes aligned to the subject
3. **Syllabus structure** — Organize into modules/weeks with topic progression
4. **Lesson plans** — Detailed plan per module: activities, readings, discussion prompts
5. **Assessment design** — Quizzes, assignments, and rubrics aligned to learning objectives
6. **Output** — Complete course package ready for LMS upload or manual use

**Scope:** Workspace-builder compatible. Educational frameworks and rubric templates live as reference files.
**Estimated effort:** 2–3 days
**Community handoff:** Shared as folder. Educator customizes reference files for their institution and subject.

**Content opportunities:**
- [x] Build walkthrough — "MWP for educators: building a course with folders"
- [x] Use-case story — Education is a top community domain. Directly addresses "MWP in my domain."
- [x] Research angle — MWP works for non-developers. Thesis expansion beyond the dev audience.

---

## Hybrid Outlines

### Automated Newsletter Pipeline

**Serves:** ID-006 (Niall Fennell, Geo Dao)
**What it is:** A pipeline that scrapes industry news sources, summarizes key stories, and formats a bi-weekly newsletter — requiring minimal human intervention.

**MWP portion (stages 2–4):**
1. **Source config** — Reference files define which sources, topics, and keywords to track
2. **Curation** — AI summarizes and ranks scraped articles by relevance
3. **Draft** — Assemble newsletter from templates with curated content
4. **Human review** — Edit draft before send

**Software portion:**
- Scraping script (fetches from configured news sources)
- Email delivery script (sends via API — Resend, SendGrid, or similar)

**Interface point:** Script drops scraped articles into MWP intake folder → pipeline processes → output folder contains newsletter → script sends.

**Technical approach:** Python scripts for scraping + email. MWP handles everything between.
**Estimated effort:** 3–5 days
**Key decisions:** Which scraping approach (RSS, web scraping, news API), which email provider

**Content opportunities:**
- [x] Build walkthrough — "Hybrid MWP: when your workspace needs scripts at the edges"
- [x] Demo video — Full newsletter from scrape to send
- [x] Research angle — The canonical "MWP + scripts" pattern. Demonstrates where MWP ends and code begins.

---

### AI Content Factory Pipeline

**Serves:** ID-004 (Jerel Ong)
**What it is:** The flagship thesis test. A full content production pipeline — research through UGC generation, video production, and upload — built with MWP orchestration instead of agent frameworks.

**MWP portion:**
1. **Research intake** — Topic briefs, audience context, content goals
2. **Content planning** — Generate content angles, scripts, visual briefs
3. **Quality review** — Human checks each intermediate output before generation proceeds
4. **Publishing config** — Platform targeting, scheduling, metadata

**Software portion:**
- UGC character generation (image/video gen API)
- Video stitching (ffmpeg or similar)
- Platform upload (YouTube/TikTok API)

**Interface point:** MWP produces briefs and scripts → generation scripts create assets → MWP reviews quality → upload scripts publish.

**Technical approach:** MWP workspace + Python scripts + external APIs (image gen, video gen, platform upload)
**Estimated effort:** 2–4 weeks (large build)
**Key decisions:** Which gen APIs (Flux/Runway vs Midjourney/Sora), whether to attempt auto-upload or stop at generated assets, scope of "UGC characters"
**Dependencies:** The newsletter pipeline (ID-006) should be built first — it proves the MWP+scripts pattern at smaller scale.

**Content opportunities:**
- [x] Build log / dev diary — Multi-part series documenting the build
- [x] Technical deep-dive — "Can .md files + scripts replace agent frameworks?"
- [x] Community beta program — Jerel Ong as first tester
- [x] Research angle — THE thesis test. Success or failure, the content writes itself.

---

### Interactive E-Learning Module Builder

**Serves:** ID-014 (Tippi Coulter)
**What it is:** A tool for building interactive compliance training modules that can replace Articulate 360, with SCORM-compliant output.

**MWP portion:**
1. **Course structure** — Learning objectives, module breakdown, compliance requirements
2. **Content authoring** — Lesson text, scenarios, assessment questions per module
3. **Interaction design** — Define interactions (multiple choice, branching scenarios, drag-and-drop)

**Software portion:**
- SCORM packaging engine (converts authored content into SCORM-compliant zip)
- Interactive module renderer (HTML/JS-based player)

**Technical approach:** MWP workspace for authoring + Node.js/Python SCORM packager + HTML template for interactive rendering
**Estimated effort:** 3–6 weeks (complex — SCORM spec is involved)
**Key decisions:** Target SCORM version (1.2 vs 2004), interaction complexity (simple quiz vs full branching), whether to build renderer or adapt existing open-source player
**Dependencies:** Course Builder workspace (ID-018) should exist first — it validates the content authoring pipeline.

**Content opportunities:**
- [x] Build log / dev diary — "Building a free Articulate alternative with folders"
- [x] Technical deep-dive — SCORM compliance via MWP + scripts
- [x] Research angle — MWP handles the creative/authoring layer; software handles the spec compliance layer

---

### Railcar Maintenance Forecasting

**Serves:** ID-030 (Daniel Silva)
**What it is:** A forecasting workspace for railcar maintenance materials that handles cold-start conditions and adapts to ongoing reliability modifications.

**MWP portion:**
1. **Domain knowledge** — Maintenance rules, material specifications, failure mode documentation
2. **Data intake** — Accept usage history and modification records
3. **Forecast review** — Human reviews predictions, adjusts based on domain expertise

**Software portion:**
- Forecasting model (handles sparse data / cold-start with Bayesian or similarity-based approaches)
- Data storage for historical records

**Technical approach:** MWP workspace for domain context + Python forecasting scripts + simple data persistence
**Estimated effort:** 2–4 weeks (domain expertise is the bottleneck)
**Key decisions:** Forecasting approach (Bayesian, kNN-based, or heuristic rules), how to handle cold-start, requester collaboration for domain knowledge
**Dependencies:** Requires deep collaboration with Daniel Silva for domain knowledge.

**Content opportunities:**
- [x] Build log / dev diary — "MWP in industrial maintenance: the most unexpected case study"
- [x] Use-case story — Industrial application of folder-based AI
- [x] Research angle — Domain expertise encoded in markdown files. The strongest "MWP works outside tech" proof point.

---

## Software Outlines

### Job Application Automation

**Serves:** ID-037 (Rahman Abdul Rafi)
**What it is:** A reliable job application automation tool that fills forms across varied platforms, outperforming existing unreliable autofill tools.

**Technical approach:** Browser automation (Playwright), form field detection and mapping, resume/profile data extraction
**Key decisions:** Which platforms to support (LinkedIn, Indeed, Greenhouse, Lever), how to handle CAPTCHAs and anti-bot, user data storage approach

**MWP components:** Resume variants, cover letter templates, targeting criteria, and application tracking could live in an MWP workspace that feeds the automation tool.
**Estimated effort:** Large (2–4 weeks). Anti-bot measures make this an ongoing maintenance problem.
**Dependencies:** None, but platform ToS should be reviewed.

**Content opportunities:**
- [x] Build log / dev diary — High audience interest (universal pain point)
- [ ] Technical deep-dive — Browser automation is well-covered elsewhere
- [x] Community beta program — Large audience overlap for beta testers

---

## Delivery Sequence

### Phase 1: Quick Wins (Target: Week 1–2)

Ship fast, build momentum, prove MWP works in real use cases.

1. **Invoice Template Automation (ID-010)** — MWP Workspace — Simplest possible build. 4 requesters. Ships in hours. First proof point.
2. **SKILLS.MD Extension (ID-028)** — MWP Workspace — Requester is already using MWP. Collaboration, not build-from-scratch. Immediate case study.
3. **Text-to-Invoice from Field Reports (ID-009)** — MWP Workspace — Builds on ID-010's template. Adds extraction. 3 requesters. Ships in 1–2 days.
4. **Design Ideation Tool (ID-027)** — MWP Workspace — Pure context engineering demo. Different domain than invoicing. Shows MWP versatility.

**Phase 1 thesis output:** 4 working MWP workspaces across 3 domains (invoicing, web design, UX design). Proves the pattern works for mundane business tasks.

**Phase 1 content output:** 4 build walkthroughs, 2 use-case stories (Daniel Hernandez as existing adopter, Carlie Rioux as new user).

### Phase 2: High Impact (Target: Week 3–6)

Deliver the items with highest community demand and strongest thesis value.

5. **MWP Learning Deep-Dive (Cluster J)** — Content Track — Produce the "how files and routing work" content that 3+ people are asking for. This unlocks community adoption for every workspace shipped in Phase 1. Run parallel to builds.
6. **ESG & Financial Report Generator (ID-023)** — MWP Workspace — Template-driven reporting in a new domain. Extends the "document automation" pattern from Phase 1.
7. **University Course Builder (ID-018)** — MWP Workspace — Education domain. Proves MWP for non-developers. Prerequisite for the e-learning module builder later.
8. **Automated Newsletter Pipeline (ID-006)** — Hybrid — First MWP+scripts build. Establishes the pattern of "MWP in the middle, scripts at the edges." 2 requesters.
9. **Voice-Based Invoice Creation (ID-011)** — Hybrid — Extends the invoice workspace with Whisper transcription. Demonstrates MWP handles voice input via a simple script boundary.

**Phase 2 thesis output:** 3 more MWP workspaces + 2 hybrid builds. Demonstrates MWP across document automation, education, and content production. Establishes the hybrid pattern.

**Phase 2 content output:** MWP methodology deep-dive series, 3 build walkthroughs, newsletter pipeline as "hybrid architecture" technical content.

### Phase 3: Strategic Bets (Target: Week 7–12)

Higher effort, higher payoff. The thesis-defining builds.

10. **AI Content Factory Pipeline (ID-004)** — Hybrid (heavy) — THE thesis test: "Can MWP replace agent frameworks?" Depends on the hybrid pattern proven in Phase 2. Multi-part content series.
11. **Interactive E-Learning Module Builder (ID-014)** — Hybrid — Challenges Articulate at $0. Depends on Course Builder (ID-018) from Phase 2.
12. **Railcar Maintenance Forecasting (ID-030)** — Hybrid — The "most unexpected MWP case study." Requires collaboration with Daniel Silva. High content value.
13. **Income Statement to Balance Sheet (ID-012)** — Hybrid — Excel generation extends the document automation pattern with a binary output format.

**Phase 3 thesis output:** The flagship case studies. ID-004 tests the core thesis. ID-014 challenges an incumbent. ID-030 takes MWP to industrial territory.

**Phase 3 content output:** Multi-part build diary for ID-004, "free Articulate" build series for ID-014, industrial case study for ID-030.

### Parked

Items deprioritized or blocked. Can be promoted if context changes.

| Item | Why Parked | Re-evaluate When |
|------|-----------|-----------------|
| ID-001, 003, 007 (Multi-Format Content Gen) | High scope risk, video quality uncertainty. Individual ideas are interesting but the cluster is too broad to ship as one. | After Phase 2, when hybrid pattern is proven. Could extract ID-001 (collateral) as standalone. |
| ID-022 (Unified AI Dashboard) | 4+ API integrations, unclear ROI vs. existing tools (Motion, Reclaim) | If a requester provides a specific, scoped version |
| ID-019 (Tech Sourcing Automation) | Requester already building on Make.com. Support, don't build. | If Jason Price needs MWP-specific help |
| ID-032 (Water Filtration Sensors) | Hardware dependency. Can't build without sensor access. | If Micah Cravalio provides API access to sensor data |
| ID-037 (Job Application Automation) | High demand but browser automation ≠ MWP. Ongoing anti-bot maintenance. | If someone contributes the Playwright automation and needs MWP for strategy/templates |
| ID-034 (Cybersecurity Challenges) | Novel but niche. Thomas Goldman has prior research — could be a collaboration. | If Thomas Goldman is ready to collaborate |
| ID-016 (Offline Vocational Training) | Very high effort, single requester, hardware unknowns | If a clearer scope and device target emerges |
| ID-029 (3D Code Visualizers) | Niche, not MWP-related, specialized skills | Not in scope for MWP pipeline |
| ID-035 (Linux Distro/Cyberdeck) | Hardware project, outside scope | Refer to hardware communities |
| ID-005, 008 (Content Intelligence) | Weak MWP fit, strong existing alternatives | Not prioritized unless demand changes |
| ID-025, 033 | Too vague. Need follow-up conversations. | After follow-up DMs get specific responses |
| ID-015, 017 (Student Outreach, Grading Bot) | Depend on specific LMS/platform integrations we don't know yet | After ID-018 (Course Builder) validates education domain |
| ID-020 (Multi-Business Suite) | Unscoped. Too broad. | After Juline Douglas picks one specific workflow |
| ID-002 (Remotion Social Media) | Requires Remotion expertise. Could partner with Kürşad. | If the content factory (ID-004) creates a video pipeline that Remotion plugs into |
| ID-013, 024, 026, 036 (Data Ingestion) | Moderate demand, existing alternatives. Composable pattern is useful but not urgent. | After the newsletter pipeline (ID-006) proves the scrape-structure pattern |

---

## Content Alignment

| Phase | Deliverable | Content Piece | Pillar | Thesis Connection |
|-------|-------------|--------------|--------|-------------------|
| 1 | Invoice Template (ID-010) | "Invoice workspace in 30 minutes" — build walkthrough | MWP workspace builds | Simplest MWP proof. Template + variable swap works without a framework. |
| 1 | SKILLS.MD Extension (ID-028) | "A community member already uses MWP" — case study interview | Community showcases | Real-world adoption story. Someone chose this approach independently. |
| 1 | Text-to-Invoice (ID-009) | "Turn messy field texts into invoices" — build walkthrough + demo | MWP workspace builds | MWP handles unstructured→structured transformation. |
| 1 | Design Ideation Tool (ID-027) | "Context engineering for design" — build walkthrough | Context engineering | Value lives in reference files. Pure context engineering demo. |
| 2 | MWP Methodology (Cluster J) | "How MWP files and routing actually work" — deep-dive series | Context engineering | THE methodology content. Defines the pillar. |
| 2 | Course Builder (ID-018) | "MWP for educators" — build walkthrough | MWP workspace builds + Community showcases | MWP works for non-developers. Thesis expansion. |
| 2 | Newsletter Pipeline (ID-006) | "Hybrid MWP: scripts at the edges" — technical walkthrough | AI workflow design | Defines the MWP + scripts boundary pattern. |
| 2 | Voice Invoice (ID-011) | "Adding voice input to an MWP workspace" — extension demo | MWP workspace builds | Shows how MWP workspaces grow incrementally. |
| 3 | Content Factory (ID-004) | "Can .md files + scripts replace agent frameworks?" — multi-part series | AI workflow design | THE thesis test. Flagship content regardless of outcome. |
| 3 | E-Learning Builder (ID-014) | "Building a free Articulate alternative" — build diary | MWP workspace builds + Tool reviews | MWP challenges an expensive incumbent. |
| 3 | Railcar Forecasting (ID-030) | "MWP in industrial maintenance" — case study | Community showcases | Most unexpected domain. Proves MWP works anywhere domain knowledge matters. |
| 3 | Excel Financial Model (ID-012) | "MWP meets binary output formats" — technical demo | AI workflow design | Extends the pattern to non-text outputs. |

### Content Cadence

- **Phase 1 (weeks 1–2):** 4 build walkthroughs, 1 case study. High frequency to build momentum.
- **Phase 2 (weeks 3–6):** MWP deep-dive series (2–3 episodes) + 3 build walkthroughs. Methodology content runs parallel to builds.
- **Phase 3 (weeks 7–12):** Long-form build diaries (ID-004, ID-014). 1 industrial case study. Flagship content.

### Thesis Progression

The delivery sequence is designed to build the thesis argument incrementally:

1. **Phase 1 proves:** MWP works for simple, real business workflows (invoicing, design).
2. **Phase 2 proves:** MWP works for non-developers (education) and MWP + scripts handles hybrid workflows (newsletter).
3. **Phase 3 proves:** MWP can replace agent frameworks (content factory) and works in industrial contexts (railcar maintenance).

Each phase makes a stronger claim than the last, supported by the evidence from prior phases.

---

## Follow-Up Actions

| Action | Target | Purpose |
|--------|--------|---------|
| DM Kaye Rae | "What data science tasks do you do repeatedly?" | Scope ID-025 for possible future classification |
| DM Amos Anzele | "Which specific RPA workflows?" | Scope ID-033 |
| DM Juline Douglas | "Pick ONE workflow that wastes the most time" | Scope ID-020 from unmanageable to actionable |
| DM Daniel Hernandez | "Let's extend your SKILLS.MD together" | Phase 1 collaboration + case study |
| DM Daniel Silva | "Walk me through your railcar maintenance process" | Phase 3 domain knowledge gathering |
| DM Thomas Goldman | "Ready to collaborate on the CTF generator?" | Assess readiness for parked ID-034 |
| Produce MWP learning content | Community-wide | Unblock adoption for all Phase 1 workspaces |
