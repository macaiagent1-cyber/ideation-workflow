# Evaluation Report — community-dms-2026-03

**Batch:** Community DMs, March 2026
**Evaluated:** 2026-03-12
**Clusters evaluated:** 10
**Orphans evaluated:** 7

---

## Cluster A: Multi-Format Content Generation (IDs: 001, 003, 007)

### Feasibility
- **Effort estimate:** High
- **Key requirements:** Image generation API (DALL-E / Midjourney / Flux), video generation API, PowerPoint/PPTX programmatic injection (python-pptx or similar), prompt engineering for consistent brand voice across formats
- **Bottleneck:** PowerPoint injection with real layout fidelity (ID-001) and video generation that "doesn't look like slop" (ID-003). Current video gen tools still produce noticeable artifacts at scale.
- **Existing solutions:** Canva's Magic Studio, Jasper, Copy.ai, and AdCreative.ai cover parts of this space. None do all 12 output types from one brief. Canva is closest but lacks deep persona targeting.

### Impact
- **Audience reach:** Medium-High. Content creators and marketers are a core community segment.
- **Value depth:** High if quality bar is met. Replaces hours of per-asset manual work. Low if output looks generic.
- **Urgency:** Medium. People are doing this manually now — painful but functional.
- **Reusability:** High. The "brief → multi-format assets" pattern applies across industries.

### Novelty
- **What exists:** AdCreative.ai (ad-specific), Canva Magic Studio (design-first), Jasper (copy-first). None combine all formats from a persona brief.
- **Differentiation:** The persona-targeting angle + breadth of output types is the gap. MWP approach would mean the persona definitions and output templates live in editable markdown.
- **Innovation angle:** Moderate. The individual capabilities exist; the integration and MWP-based orchestration is the new part.

### Channel Alignment
- **Content pillar:** MWP workspace builds (if delivered as a workspace), Tool reviews (evaluating gen tools along the way)
- **Content generation:** Very high. Building a multi-format content generator on camera is compelling content. Each output type is a mini-demo.
- **Audience reinforcement:** Strong. Developers who create content are the core audience.
- **Brand demonstration:** Moderate. Demonstrates MWP can orchestrate multi-tool pipelines, but the heavy lifting is in the APIs, not the folder structure.

### Research Alignment
- **MWP fit signal:** Partial. The orchestration layer (which format, which persona, which template) is MWP-fit. The generation layer (calling image/video APIs) pushes toward software-required.
- **Paper relevance:** Demonstrates MWP as orchestration for multi-tool workflows — useful but not the strongest thesis proof.
- **Case study potential:** High. The build process itself is rich content.

### Risks
- **Delivery risk:** Video and image quality may not meet the "no slop" bar (ID-003). PowerPoint injection with real formatting fidelity is harder than it sounds.
- **Scope risk:** High. 12 output types is a massive surface area. Scope creep is explicitly called out in the raw notes.
- **Reputation risk:** Medium. Delivering low-quality generated content could undermine the "practical tools" brand.
- **Opportunity cost:** This is a large build. Time spent here doesn't go to the high-demand template automation cluster.

---

## Cluster B: Content Production Pipelines (IDs: 002, 004, 006)

### Feasibility
- **Effort estimate:** Medium–High (varies by idea)
- **Key requirements:** ID-002 needs Remotion expertise. ID-004 needs UGC generation, video stitching, and platform upload APIs. ID-006 needs web scraping, summarization, and email/newsletter formatting.
- **Bottleneck:** ID-004 is the most complex — end-to-end from research to auto-upload involves 5+ distinct steps with different tool requirements. ID-006 is the most straightforward (scrape → summarize → format).
- **Existing solutions:** Buffer/Hootsuite (scheduling), Descript (video), Beehiiv/Substack (newsletters). None provide the full pipeline. n8n/Make.com handle orchestration but aren't MWP-native.

### Impact
- **Audience reach:** High. Content production is the #1 community domain.
- **Value depth:** High. These replace entire workflows, not just individual tasks.
- **Urgency:** Medium-High. ID-006 (newsletter) has multiple requesters and a clear pain point ("pulls me away from my real job"). ID-004 is aspirational.
- **Reusability:** High for ID-006 (any industry newsletter). Medium for ID-002 and ID-004 (more specialized).

### Novelty
- **What exists:** n8n, Make.com, and Zapier handle multi-step automation. YouTube automation tools exist (Opus Clip, Vidyo.ai). Newsletter tools like Beehiiv have AI features.
- **Differentiation:** ID-004 explicitly asks whether MWP (.md files + scripts) can replace agent frameworks. This is the thesis test. The differentiation is proving that folder structure works where people assume they need a framework.
- **Innovation angle:** High for thesis. The individual steps aren't novel — the claim that you don't need a framework to orchestrate them is.

### Channel Alignment
- **Content pillar:** AI workflow design (primary), MWP workspace builds
- **Content generation:** Exceptional. ID-004 is literally "can your approach replace frameworks?" — this is a video that writes itself.
- **Audience reinforcement:** Very strong. Developers who produce content are watching to see if MWP works for their workflows.
- **Brand demonstration:** ID-004 is the strongest brand demonstration opportunity in the entire batch.

### Research Alignment
- **MWP fit signal:** ID-006 (newsletter) is strong MWP fit — sequential stages, text-based, clear handoffs. ID-004 is the ultimate MWP stress test. ID-002 is more tool-specific (Remotion).
- **Paper relevance:** ID-004 directly tests the thesis. ID-006 demonstrates it in a common use case. High relevance.
- **Case study potential:** Exceptional. ID-004 could be the flagship case study for the research paper.

### Risks
- **Delivery risk:** ID-004 is ambitious. If it fails or requires a framework anyway, it undermines the thesis publicly.
- **Scope risk:** ID-004 has open-ended scope (research, UGC gen, video, upload). Needs aggressive scoping.
- **Reputation risk:** Low for ID-006 (well-understood pipeline). High for ID-004 (public thesis test).
- **Opportunity cost:** ID-004 is a large investment. But the thesis payoff is proportionally large if it succeeds.

---

## Cluster C: Content Intelligence & Organization (IDs: 005, 008)

### Feasibility
- **Effort estimate:** Medium–High
- **Key requirements:** ID-005 needs social media platform APIs (rate-limited, often restricted). ID-008 needs document parsing (PowerPoint, images, meeting notes), embedding-based search, and tagging.
- **Bottleneck:** ID-005's bottleneck is API access — platforms restrict analytics access, especially for personal accounts. ID-008's bottleneck is parsing diverse file formats reliably.
- **Existing solutions:** ID-005: Sprout Social, Metricool, Hootsuite analytics. ID-008: Notion AI, Mem, various RAG-based search tools.

### Impact
- **Audience reach:** Medium. Useful but not a burning pain point for most community members.
- **Value depth:** Medium. Convenience improvement, not a fundamental workflow change.
- **Urgency:** Low. People can check analytics manually. Content search is annoying but not blocking.
- **Reusability:** Medium. Analytics coaching is platform-specific. Content search is more general.

### Novelty
- **What exists:** Strong existing solutions in both spaces. Sprout Social for analytics, Notion AI for content search.
- **Differentiation:** Low. Hard to beat purpose-built analytics tools. Content search via embeddings is increasingly commoditized.
- **Innovation angle:** Low. Neither pushes the MWP thesis forward significantly.

### Channel Alignment
- **Content pillar:** Tool reviews (evaluating analytics/search tools)
- **Content generation:** Low. Building an analytics bot isn't compelling video content compared to other options.
- **Audience reinforcement:** Weak. Developers care more about building than analyzing.
- **Brand demonstration:** Weak. Platform API limitations aren't an MWP problem — they're an access problem.

### Research Alignment
- **MWP fit signal:** Weak. ID-005 is platform-API-dependent (software-required). ID-008 needs embedding infrastructure (software-required).
- **Paper relevance:** Low. Neither demonstrates MWP's strengths.
- **Case study potential:** Low.

### Risks
- **Delivery risk:** High for ID-005 (API access may be blocked). Medium for ID-008.
- **Scope risk:** Low. Both are contained.
- **Reputation risk:** Low.
- **Opportunity cost:** Small build, small reward. Fine if nothing else is competing for time.

---

## Cluster D: Template-Driven Document Automation (IDs: 009, 010, 011, 012, 023)

### Feasibility
- **Effort estimate:** Low–Medium
- **Key requirements:** Template design, variable extraction from input data, output formatting (PDF, Excel, markdown). ID-009 adds text parsing from SMS. ID-011 adds voice-to-text input.
- **Bottleneck:** ID-009's bottleneck is reliably parsing unstructured field worker texts into structured line items. ID-010 is trivially simple. ID-011 needs voice transcription (Whisper API). ID-012 needs Excel formula architecture. ID-023 needs ESG report structure knowledge.
- **Existing solutions:** QuickBooks (ID-010 requester already uses it), FreshBooks, Wave for invoicing. Excel templates exist for financial modeling. ESG reporting tools exist but are enterprise-priced.

### Impact
- **Audience reach:** High. Invoice automation alone has 6+ requesters across 3 ideas. Financial reporting extends to consultants and nonprofits.
- **Value depth:** High. These replace daily manual work. ID-009 specifically saves a contractor from daily data entry.
- **Urgency:** High. People are doing this by hand today, every day. This is active pain, not aspirational improvement.
- **Reusability:** Very high. Every freelancer, contractor, and small business invoices. Templates are inherently reusable.

### Novelty
- **What exists:** Invoicing software is a crowded space. QuickBooks, FreshBooks, Wave, Zoho Invoice. Excel financial models are widely available.
- **Differentiation:** The MWP angle — your invoice templates, your extraction rules, your formatting, all in editable markdown files you own and understand. No SaaS lock-in. ID-011's pitch is explicit: "simpler than n8n."
- **Innovation angle:** Moderate. The novelty isn't in invoicing — it's in showing that MWP can handle a "boring" workflow better than a framework/SaaS. This is a strong thesis proof precisely because the problem is well-understood.

### Channel Alignment
- **Content pillar:** MWP workspace builds (primary). This is the textbook MWP demo.
- **Content generation:** Excellent. "Build an invoice automation workspace in 30 minutes" is high-value, high-searchability content. Multiple angles: text parsing, voice input, Excel generation.
- **Audience reinforcement:** Very strong. This hits the community's biggest need: "see MWP applied to their own domains." Everyone invoices.
- **Brand demonstration:** Strong. Proving MWP works for mundane, universal business tasks is more convincing than a flashy demo.

### Research Alignment
- **MWP fit signal:** Very strong. Sequential stages, text-based input/output, clear templates, human-reviewable output. This is what MWP was designed for.
- **Paper relevance:** High. "MWP handles real business workflows" is a key claim to demonstrate.
- **Case study potential:** Excellent. Three variations of the same pattern (text, template, voice) make a compelling comparison case study.

### Risks
- **Delivery risk:** Low. The simplest ideas (ID-010) are almost trivial to deliver. Even the harder ones (ID-009, ID-011) have well-understood solutions.
- **Scope risk:** Low. Invoice = clear boundaries. Financial models (ID-012) are somewhat scope-creepy but containable.
- **Reputation risk:** Low. Under-delivering a simple invoice tool is unlikely. Over-delivering builds trust.
- **Opportunity cost:** Low effort, high signal. Delivering this doesn't block other work significantly.

---

## Cluster E: External Data Ingestion & Structuring (IDs: 013, 024, 026, 036)

### Feasibility
- **Effort estimate:** Medium
- **Key requirements:** API integration (EDGAR, FRED, Yahoo Finance, ProPublica, news APIs), data parsing/extraction, structured storage (spreadsheet/database), scheduling for recurring pulls.
- **Bottleneck:** Data source reliability and format consistency. EDGAR and ProPublica have usable APIs; other sources may require scraping. Rate limits apply.
- **Existing solutions:** Bloomberg Terminal (expensive), various financial data APIs (Alpha Vantage, Polygon.io), ProPublica's nonprofit API. ID-026: worldmonitor.app was explicitly mentioned as an existing alternative.

### Impact
- **Audience reach:** Medium. Financial data users are a subset. ID-026 (news dashboard) has broader appeal but an existing alternative was cited.
- **Value depth:** Medium-High. For people who need this data regularly, automation saves significant time.
- **Urgency:** Medium. These are "would be nice" rather than "can't function without."
- **Reusability:** High. The fetch → parse → structure pattern is the same regardless of data source. A composable template could serve all four.

### Novelty
- **What exists:** Financial data aggregators are plentiful. ID-026 has a direct competitor (worldmonitor.app).
- **Differentiation:** Ownership and customizability. You own the pipeline, you choose the sources, you control the format. No SaaS dependency.
- **Innovation angle:** Low for the data part. Moderate for demonstrating MWP as a data pipeline orchestrator.

### Channel Alignment
- **Content pillar:** AI workflow design (pipeline architecture content)
- **Content generation:** Good. "Build a financial data pipeline with folders and scripts" is solid tutorial content. The composable/swappable source pattern is an architectural lesson.
- **Audience reinforcement:** Moderate. Developers will appreciate the pattern even if they don't need financial data specifically.
- **Brand demonstration:** Moderate. Shows MWP handles data workflows, but the pipeline is script-heavy, not just markdown.

### Research Alignment
- **MWP fit signal:** Moderate. The orchestration layer (which sources, what schedule, how to structure) is MWP-fit. The actual fetching/parsing is script work.
- **Paper relevance:** Useful as a "MWP + scripts" pattern demonstration.
- **Case study potential:** Good for showing the composable adapter pattern.

### Risks
- **Delivery risk:** Medium. API changes, rate limits, and data format inconsistency are ongoing maintenance concerns.
- **Scope risk:** Low per idea. The "composable pipeline" meta-idea could expand if not scoped.
- **Reputation risk:** Low.
- **Opportunity cost:** Medium effort. Not the highest-impact cluster but builds reusable patterns.

---

## Cluster F: AI-Powered Education & Assessment (IDs: 014, 015, 017, 018)

### Feasibility
- **Effort estimate:** Medium–High (varies significantly by idea)
- **Key requirements:** ID-014 needs SCORM-compliant output generation (a specific, complex standard). ID-015 needs student performance data access + messaging integration. ID-017 needs LMS/grading system API integration. ID-018 needs curriculum structure knowledge.
- **Bottleneck:** ID-014's SCORM compliance is the hardest requirement — it's a specific packaging format that e-learning platforms require. ID-017 depends entirely on which grading system the lecturer uses. ID-015 and ID-018 are more tractable.
- **Existing solutions:** ID-014: Articulate 360 ($1,299/yr), Rise, Storyline, iSpring. ID-015: Various LMS engagement tools. ID-017: Gradescope, Turnitin. ID-018: Course design templates exist but aren't AI-assisted at this level.

### Impact
- **Audience reach:** Medium. Education is a key community domain but not the largest segment.
- **Value depth:** High. These replace significant manual effort (grading, course design, student outreach). ID-014 competes with expensive incumbents.
- **Urgency:** Medium-High for ID-014 (Articulate is expensive and disliked). Medium for others.
- **Reusability:** High. Every educator needs some combination of these tools. Course templates and grading rubrics are universally applicable.

### Novelty
- **What exists:** Articulate dominates corporate e-learning. Gradescope handles AI grading. LMS platforms have built-in messaging. No MWP-based alternative exists for any of these.
- **Differentiation:** Ownership and cost. Articulate is $1,299/yr and locked to their platform. An MWP-based course builder is free, open, and customizable.
- **Innovation angle:** High for ID-014 (challenging an incumbent with a radically different approach). Moderate for others.

### Channel Alignment
- **Content pillar:** MWP workspace builds + Community showcases
- **Content generation:** Strong. Building a "free Articulate alternative with folders" is a high-hook video concept. Education demos are relatable.
- **Audience reinforcement:** Strong. Education is one of the top community domains. Directly addresses "see MWP in my domain."
- **Brand demonstration:** Strong. Proving MWP works for non-developers (educators) widens the thesis significantly.

### Research Alignment
- **MWP fit signal:** Mixed. ID-018 (course builder) and ID-015 (outreach) are strong MWP candidates. ID-014 (SCORM modules) likely needs software. ID-017 depends on integration complexity.
- **Paper relevance:** High. "MWP works for educators, not just developers" is a powerful thesis expansion.
- **Case study potential:** Excellent. Education is a non-obvious domain that makes the case study surprising and compelling.

### Risks
- **Delivery risk:** High for ID-014 (SCORM is complex). Medium for ID-017 (grading system integration uncertainty). Low for ID-015, ID-018.
- **Scope risk:** Medium. Each education idea could expand into a full LMS if not scoped carefully.
- **Reputation risk:** Medium. Educators depend on these tools for real students. A flaky grading bot or broken compliance module has real consequences.
- **Opportunity cost:** The simpler ideas (ID-015, ID-018) are worth delivering. ID-014 is a larger bet.

---

## Cluster G: Business Operations Automation (IDs: 019, 020, 021, 022)

### Feasibility
- **Effort estimate:** Medium–Very High (wide range)
- **Key requirements:** ID-019 needs Make.com/Claude integration (already in progress). ID-020 is too broad to scope. ID-021 needs calendar API integration. ID-022 needs Asana API + email API + calendar API + web scraping.
- **Bottleneck:** Integration density. ID-022 requires 4+ API integrations in a single dashboard. ID-020 has no clear deliverable. ID-019 is the most tractable because the requester is already building.
- **Existing solutions:** Asana, Monday.com, ClickUp (project management). Zapier/Make.com (automation). Motion (AI calendar scheduling). Various "AI executive assistant" startups.

### Impact
- **Audience reach:** Medium. Business ops tools appeal to a subset of the community (consultants, agency owners, ops people).
- **Value depth:** Potentially very high — replacing employee-level work (ID-019). But highly dependent on individual business context.
- **Urgency:** High for ID-019 (lost two employees, immediately felt the gap). Low for ID-020 (needs scoping first).
- **Reusability:** Mixed. ID-021 (task decomposition) is universal. ID-019 and ID-022 are situation-specific.

### Novelty
- **What exists:** The "AI executive assistant" space is crowded and well-funded. Lindy, Relevance AI, and dozens of startups. Calendar scheduling: Motion, Reclaim.ai.
- **Differentiation:** MWP angle means the business logic is transparent and editable. No black-box AI decisions. You see the rules in your folders.
- **Innovation angle:** Low. Business ops automation is well-trodden ground. The MWP angle is the only differentiator.

### Channel Alignment
- **Content pillar:** AI workflow design
- **Content generation:** Moderate. "Replace two employees with an AI workflow" (ID-019) is clickable content. The others are less compelling.
- **Audience reinforcement:** Moderate. Business ops isn't the primary audience interest.
- **Brand demonstration:** Moderate. Shows MWP in business context but doesn't push the thesis boundary.

### Research Alignment
- **MWP fit signal:** ID-021 (task decomposition) is MWP-fit — it's a structured process that lives in markdown. ID-019 is already on Make.com (not MWP-native). ID-022 is software-required (multi-API dashboard). ID-020 is unscoped.
- **Paper relevance:** Low. Business ops is a common AI application area without strong thesis novelty.
- **Case study potential:** ID-019 is interesting as a "person already building, needs orchestration help" story. Others are weaker.

### Risks
- **Delivery risk:** High for ID-022 (integration complexity). ID-020 can't be delivered without scoping. ID-019 is low risk (already in progress).
- **Scope risk:** Very high for ID-020 (the request is everything). Medium for ID-022.
- **Reputation risk:** Low. These are personal productivity tools.
- **Opportunity cost:** ID-019 is worth supporting (low effort, person already building). ID-022 is a large investment with uncertain return.

---

## Cluster H: Domain-Specific Industrial AI (IDs: 030, 031, 032)

### Feasibility
- **Effort estimate:** High–Very High
- **Key requirements:** ID-030 needs forecasting models for sparse data (cold-start problem), railcar domain knowledge. ID-031 needs real estate compliance rules and document processing. ID-032 needs IoT sensor data ingestion, time-series analysis, and customer notification systems.
- **Bottleneck:** Domain knowledge acquisition. None of these can be built without deep understanding of the specific industry. ID-032 also has a hardware dependency (sensor integration).
- **Existing solutions:** ID-030: SAP PM, IBM Maximo (enterprise maintenance). ID-031: Dotloop, SkySlope (real estate transaction management). ID-032: Industrial IoT platforms (ThingSpeak, Losant).

### Impact
- **Audience reach:** Low individually (niche industries). Medium collectively (demonstrates MWP versatility).
- **Value depth:** Very high per recipient. These solve real operational problems in the requester's daily work.
- **Urgency:** High for each individual requester. These are active pain points in their businesses.
- **Reusability:** Low. Railcar forecasting doesn't transfer to water filtration. Each is bespoke.

### Novelty
- **What exists:** Enterprise solutions exist for each domain but are expensive and rigid. No MWP-based alternatives.
- **Differentiation:** Accessibility and cost. Enterprise tools are $10K+/year. An MWP workspace is free and transparent.
- **Innovation angle:** High. Showing MWP works in industrial domains (rail, real estate, water treatment) is surprising and expands the thesis significantly.

### Channel Alignment
- **Content pillar:** Community showcases (primary). This is the textbook "MWP in the wild" content.
- **Content generation:** Very high. "I built a railcar maintenance predictor with folders" is genuinely compelling content. The surprise factor drives views.
- **Audience reinforcement:** Strong if framed as "here's what MWP looks like in YOUR domain." Directly addresses the community's biggest need.
- **Brand demonstration:** Very strong. Proving MWP works in industrial contexts is the most convincing thesis proof possible — it's the furthest from a developer-centric comfort zone.

### Research Alignment
- **MWP fit signal:** Mixed. The domain knowledge layer (compliance rules, maintenance schedules, sensor thresholds) is perfect MWP material — it's all structured text. The computation layer (forecasting models, IoT ingestion) is software-required.
- **Paper relevance:** Very high. "MWP in industrial contexts" is a powerful chapter.
- **Case study potential:** Exceptional. Each of these is a standout case study.

### Risks
- **Delivery risk:** High. Domain expertise is the bottleneck, and getting it wrong has real operational consequences. ID-032's hardware dependency adds another failure mode.
- **Scope risk:** Medium. Each is naturally bounded by the specific industry process.
- **Reputation risk:** Medium-High. A bad maintenance forecast or a missed compliance check has real-world consequences beyond the digital space.
- **Opportunity cost:** These are large builds. One at a time is realistic. All three is a multi-month commitment.

---

## Cluster I: Structured Design & Dev Workflows (IDs: 027, 028)

### Feasibility
- **Effort estimate:** Low–Medium
- **Key requirements:** ID-027 needs a structured ideation process encoded in context files (heuristics, accessibility rules, competitor analysis prompts). ID-028 needs extending an existing SKILLS.MD file with marketing/lead gen modules.
- **Bottleneck:** ID-027 requires curating high-quality design heuristics and accessibility checklists. ID-028 is the simplest idea in the batch — the requester is already using the approach and just wants to extend it.
- **Existing solutions:** ID-027: Design thinking frameworks, Figma's built-in brainstorming tools, various UX checklists. ID-028: Nothing — this person already has a custom solution.

### Impact
- **Audience reach:** Medium. Designers and web devs are a community segment.
- **Value depth:** Medium for ID-027 (process improvement). High for ID-028 (extending a tool they already depend on).
- **Urgency:** Medium. Neither is a burning need.
- **Reusability:** High for ID-027 (any designer could use structured ideation). Limited for ID-028 (specific to one person's workflow, though the pattern is reusable).

### Novelty
- **What exists:** Design thinking frameworks are well-established. UX checklists are free online. No one has packaged this as an MWP workspace.
- **Differentiation:** The packaging. Turning scattered design knowledge into a structured, repeatable workspace is the value.
- **Innovation angle:** Moderate. The innovation is in the format (MWP), not the content (design heuristics).

### Channel Alignment
- **Content pillar:** MWP workspace builds + Context engineering
- **Content generation:** Good for ID-027 (showing context engineering for design). Excellent for ID-028 (a community member already using MWP — perfect case study interview).
- **Audience reinforcement:** Moderate. Developers doing design work will find this relevant.
- **Brand demonstration:** ID-028 is a proof point — someone already uses the approach and wants more. That's the strongest possible endorsement.

### Research Alignment
- **MWP fit signal:** Very strong for both. These are pure context-in-folders problems. No software required.
- **Paper relevance:** ID-028 is a real-world MWP adoption story. High relevance.
- **Case study potential:** ID-028 is a ready-made case study. ID-027 demonstrates context engineering.

### Risks
- **Delivery risk:** Very low. Both are markdown/folder builds with no API dependencies.
- **Scope risk:** Low for ID-028. Medium for ID-027 (design heuristics could expand endlessly).
- **Reputation risk:** Very low.
- **Opportunity cost:** Minimal. These are small builds with disproportionate thesis value.

---

## Cluster J: MWP Learning & Methodology Demand (IDs: 038, 039, 040)

### Feasibility
- **Effort estimate:** Low (content creation, not software builds)
- **Key requirements:** Clear documentation, tutorial content, example workspaces. No technical infrastructure needed.
- **Bottleneck:** Pedagogical design — explaining MWP clearly to people at different skill levels.
- **Existing solutions:** Existing Eduba video content covers MWP, but the specific "how files and routing work" deep-dive doesn't exist yet.

### Impact
- **Audience reach:** Very high. This is the foundational content that every other workspace build depends on. If people don't understand MWP, they can't use the workspaces you build for them.
- **Value depth:** High. Understanding the methodology is the prerequisite for everything else.
- **Urgency:** High. Multiple people are asking for this. Without it, every workspace delivery requires hand-holding.
- **Reusability:** Maximum. This content serves every current and future community member.

### Novelty
- **What exists:** Existing Eduba videos introduce MWP. No structured deep-dive on files, routing, and how to adapt it to your own domain exists.
- **Differentiation:** This IS the differentiated content. No one else teaches this methodology.
- **Innovation angle:** High. This is original intellectual property — the methodology itself.

### Channel Alignment
- **Content pillar:** Context engineering (primary). This defines the pillar.
- **Content generation:** This IS the content. No build required — the content is the deliverable.
- **Audience reinforcement:** Maximum. This is exactly what the audience is asking for.
- **Brand demonstration:** Maximum. Teaching the methodology IS the brand.

### Research Alignment
- **MWP fit signal:** N/A — this is content, not a build.
- **Paper relevance:** Foundational. The educational content is how the research reaches practitioners.
- **Case study potential:** N/A — but enables all future case studies by creating informed community members.

### Risks
- **Delivery risk:** Very low. This is writing and filming, not engineering.
- **Scope risk:** Low. Can be chunked into episodes/modules.
- **Reputation risk:** Very low. Worst case is content doesn't land, which is easily iterated.
- **Opportunity cost:** Minimal. This should be produced alongside workspace builds, not instead of them.

---

## Orphan Evaluations

### ID-016: Offline Vocational Training AI

**Feasibility:** Very High effort. Offline-first architecture is a fundamental constraint that changes everything — no API calls, local models only, limited device capability. Requires research into edge deployment (Ollama, llama.cpp) and low-resource devices.
**Impact:** Potentially transformative in its context (developing country vocational training) but extremely niche within the Eduba community.
**Novelty:** High. Very few people are building offline-first AI training tools. The constraint is the innovation.
**Channel Alignment:** Moderate. Compelling content ("AI with no internet") but far from the core audience's context.
**Research Alignment:** Interesting edge case for MWP — does the methodology work when the AI layer is local-only? Novel thesis question.
**Risks:** Very high delivery risk (hardware unknowns, offline constraints). The request is also vague — which vocation? What devices? Needs significant scoping. High opportunity cost for a single requester.

### ID-025: Data Science Workflows

**Feasibility:** Unknown. Request is too vague to assess.
**Impact:** Unknown. Could be high if scoped to a specific workflow. Currently unassessable.
**Novelty:** Unknown.
**Channel Alignment:** Low in current form. "Data science workflows" is generic.
**Research Alignment:** Unknown.
**Risks:** Cannot be evaluated until scoped. Recommend follow-up with requester before allocating any effort.

### ID-029: 3D Code Visualizers for Web

**Feasibility:** High effort. Three.js/WebGL development is specialized. Car configurators require 3D asset management, material systems, camera controls, and UI overlays.
**Impact:** High for the right audience (e-commerce, automotive, real estate). Niche within the Eduba community.
**Novelty:** High. AI-assisted 3D configuration is emerging but not mainstream. Cool demos but limited to specific industries.
**Channel Alignment:** Moderate. Visually impressive content but doesn't reinforce MWP thesis. This is a software engineering project, not a workflow orchestration problem.
**Research Alignment:** Weak. 3D visualization is not an MWP problem.
**Risks:** Scope risk is high (3D development expands fast). Requires specialized skills. Reputation risk is low. Opportunity cost is high for a niche outcome.

### ID-033: RPA Process Improvement

**Feasibility:** Unknown. Request is too vague to assess.
**Impact:** Unknown. RPA is a large market but "improve processes" could mean anything.
**Novelty:** Unknown.
**Channel Alignment:** Low. RPA is adjacent to AI workflows but not the same audience.
**Research Alignment:** Potentially interesting — "MWP as a replacement for RPA" is a thesis-relevant angle, but only if scoped.
**Risks:** Cannot be evaluated until the requester specifies which RPA processes. Recommend follow-up.

### ID-034: Cybersecurity Challenge Generator

**Feasibility:** Medium-High. Requires generating code with specific, controlled vulnerabilities while ensuring it's otherwise safe. Validation is the hard part — how do you confirm the vulnerability exists and nothing else is broken?
**Impact:** Medium. Cybersecurity education is growing. CTF challenge creation is a real pain point for educators and trainers.
**Novelty:** High. AI-generated security challenges with validated, controlled vulnerabilities is genuinely novel. The requester has prior research.
**Channel Alignment:** Moderate. Security is adjacent to the core audience. The build process would make good content, but it's a specialized domain.
**Research Alignment:** Moderate. The challenge templates and vulnerability specifications could be MWP-structured (markdown files defining vulnerability types and constraints). Interesting MWP application.
**Risks:** High validation risk — a cybersecurity tool with bugs is worse than no tool. Medium reputation risk for the same reason. Moderate opportunity cost.

### ID-035: Custom Linux Distro & Cyberdeck

**Feasibility:** Very High effort. This is a hardware + OS project requiring physical builds, driver configuration, and distro customization. Completely outside the software/workflow space.
**Impact:** Very low for the Eduba community. Single-person hardware hobby project.
**Novelty:** Cool but irrelevant to MWP or AI workflows.
**Channel Alignment:** None. This doesn't map to any content pillar.
**Research Alignment:** None.
**Risks:** Not worth evaluating further. This is outside scope. The requester is better served by hardware communities (r/cyberdeck, Pine64 forums).

### ID-037: Job Application Automation

**Feasibility:** Medium. Browser automation (Playwright/Puppeteer) for form-filling across varied job application platforms. Each platform has different forms, CAPTCHAs, and anti-bot measures.
**Impact:** High. Job searching is a universal pain point. "Lots of audience overlap" per the original notes.
**Novelty:** Medium. LinkedIn Easy Apply, Simplify, LazyApply exist but are reportedly unreliable (which is the complaint driving this request).
**Channel Alignment:** Moderate. The build is interesting content but it's a browser automation project, not a workflow orchestration one.
**Research Alignment:** Weak. Browser automation isn't MWP territory. The job search strategy could be MWP-structured (targeting criteria, resume variants, cover letter templates in folders) but the automation layer is software.
**Risks:** Medium delivery risk (anti-bot measures). Medium reputation risk (automated applications can backfire). Platform ToS violations are a concern.
