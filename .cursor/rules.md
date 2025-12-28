# AI-First Collaborative Framework – Permanent Rules for All Agents

You are an AI agent in a repository designed for human-AI collaboration across ideation, development, iteration, integration, and simulations. Follow these rules strictly in every chat or action. This framework supports tools like Cursor, GitHub Copilot, and multi-agent systems from Google/OpenAI.

## Core Project Goals

- Enable initial idea discussions with LLMs, then formalize into persistent files for context retention.
- Handle novel approaches: Discuss implementations, disagree with existing architecture based on new research (e.g., PDFs, text formats).
- Process heterogeneous inputs (images, PDFs, XLS, etc.) into adaptable outputs for simulations (e.g., design/engineering/finance projects) using protocols like Model Context Protocol (MCP).
- Maintain non-technical accessibility: Explain choices assuming zero technical knowledge, using plain English.
- Integrate systems thinking: Use utility functions (e.g., Cobb-Douglas U(x1,x2) = x1^α * x2^(1-α)) for trade-offs, smoothing paths via PDE integrals (e.g., ∫ ∇U · dx).

## Key Files You MUST Reference (Read When Relevant)

- spec.md: High-level requirements and goals.
- architecture.md: Living design decisions.
- CONTEXT.md: 1-page executive summary of current state, open questions, links (update weekly).
- proposals/*.md: New ideas/papers; include sections: Summary, Link/Citation, Pros/Cons vs Current, Migration Plan, Open Questions.
- docs/adr/*.md: Architecture Decision Records with "Superseded by" and "Objections" sections.
- DECISIONS.md: Dashboard with tables (Core Choices, Rejected Ideas, Open Questions); keep ultra-short, non-technical.
- CHANGELOG.md: Version history in Keep a Changelog format; link to roots (proposals/ADRs).
- incoming/: Trigger processing for any dropped files.
- assets/: Store usable outputs (data, models, figures); include mini-READMEs.
- processing/: Notebooks/scripts for computations.

## Workflow Rules You Must Enforce

1. **Ideation and Iteration**: Start discussions with high-level prompts; formalize outputs into MD files. Break tasks into phases (planning, coding, testing) to manage context limits.
2. **Novel Approaches/Disagreement**: For new ideas (e.g., from PDFs), create dated proposal file immediately. Compare to architecture.md/DECISIONS.md; feel free to disagree with past choices if evidence provided. When implementing, generate code, update architecture.md, supersede ADRs.
3. **Data Processing Pipeline (Ingest & Compute)**: On file in incoming/ (e.g., PDF/XLS/image), offer: "New file detected. Shall I extract to assets/?" Create: clean data (.parquet/CSV), notebooks/scripts, figures, summary (append to CONTEXT.md), next-steps (TODO.md/DECISIONS.md if architectural). Outputs must be MCP-compliant: executable, adaptable (e.g., for PDE simulations), with instructions for further modeling.
4. **MCP Integration**: Use MCP SDKs (e.g., Python) for multi-environment adaptability. Expose resources/tools for heterogeneous data; ensure outputs support simulations (e.g., PDE path-smoothing with Cobb-Douglas utilities).
5. **Decision and Version Updates**: After accepting/rejecting ideas, MUST update DECISIONS.md (limit Core Choices to 10 rows; plain English). Draft CHANGELOG.md entries post-merge (link roots); use SemVer.
6. **GitHub Utilization**: Suggest feature branches for experiments. Automate via Actions (e.g., ingest.yml for incoming/ processing). Use Releases for version snapshots.
7. **Systems Thinking & Simulations**: For projects involving variance, apply Cobb-Douglas for resource optimization. Integrate PDEs (e.g., finite differences) for path integrals; output interactive assets (e.g., Streamlit apps).
8. **Session Start**: Always suggest: "Shall I load CONTEXT.md + architecture.md + latest proposal/DECISIONS.md?"
9. **Automation Permissions**: Install packages (uv/pip) if needed for extraction. Enforce folder template; create missing files.

## Folder Template Enforcement

Ensure this exists; create if missing: src/, tests/, docs/references/, docs/adr/, proposals/, incoming/, assets/data/models/figures/prompts/exports/, processing/notebooks/scripts/logs/, research/, spec.md, architecture.md, CONTEXT.md, DECISIONS.md, CHANGELOG.md, TODO.md, README.md.

## Example DECISIONS.md Template

# Current Architectural Decisions – Human & AI readable (updated automatically)

Last updated: [Date] – edit freely, AI tidies.

## 1. Big Picture

[One-sentence summary].

## 2. Core Choices (max 10 rows)

| Area | Chosen | Instead Of | Because (Plain English) | Status |
|------|--------|------------|-------------------------|--------|
[Table rows]

## 3. Rejected Ideas

| Date | Idea/Paper | Why Rejected | Link |
|------|------------|--------------|------|
[Table rows]

## 4. Open Questions

- [Questions with links]

## Example CHANGELOG.md Template

# Changelog

[Keep a Changelog format with Unreleased, version sections, rationale linking roots].

This set ensures productivity while acknowledging AI inconsistencies.

Adopt this root-level hierarchy for all projects to optimize AI collaboration and data handling:
project-name/
├── src/                  # Core code, modular by feature/module
├── tests/                # Unit/integration tests
├── docs/                 # All documentation
│   ├── references/       # PDFs, papers, external sources for long-term citation
│   ├── adr/              # Architecture Decision Records (ADRs) for formal decisions
│   └── diagrams/         # Generated visuals (e.g., architecture diagrams)
├── proposals/            # Novel ideas, disagreements, and research integrations
│   ├── 2025-12-example-proposal.md  # Dated files with summaries, pros/cons, migration plans
├── incoming/             # Drop heterogeneous files here (PDFs, XLS, images, etc.) for auto-processing
│   ├── example-paper.pdf
│   └── dataset.xlsx
├── assets/               # Reusable outputs from processing
│   ├── data/             # Cleaned datasets (e.g., .parquet, .csv)
│   ├── models/           # Trained models (e.g., ONNX, pickled)
│   ├── figures/          # Charts, diagrams (PNG, interactive HTML)
│   ├── prompts/          # Reusable LLM prompt templates
│   └── exports/          # Packages, APIs, dashboards for further development
├── processing/           # Scripts and notebooks for transformations
│   ├── notebooks/        # .ipynb for simulations, computations
│   ├── scripts/          # Auto-generated .py for extractions
│   └── logs/             # Processing history, errors, decisions
├── research/             # Optional archive for variance-representing files
├── spec.md               # High-level requirements (evolves slowly)
├── architecture.md       # Current design decisions
├── CONTEXT.md            # 1-page summary of state, questions, links
├── DECISIONS.md          # Decision dashboard (tables for choices, rejections)
├── CHANGELOG.md          # Versioned history with roots
├── TODO.md               # Open experiments, next steps
├── README.md             # Setup, usage, contributions
└── .cursor/rules.md      # AI enforcement rules (detailed below)

