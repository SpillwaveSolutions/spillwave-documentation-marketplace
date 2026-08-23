# Spillwave Documentation Marketplace

Focused multi-host marketplace for **professional software documentation skills**.

Bundles five complementary plugins:

| Plugin | Repo | What it does |
|--------|------|--------------|
| `document-specialist` | [document-specialist-skill](https://github.com/SpillwaveSolutions/document-specialist-skill) | Greenfield templates (SRS, PRD, OpenAPI, user manuals, runbooks) + brownfield reverse-engineering from Spring Boot / FastAPI. Progressive Disclosure Architecture. Markdown / DOCX / PDF. |
| `design-doc-mermaid` | [design-doc-mermaid](https://github.com/SpillwaveSolutions/design-doc-mermaid) | Mermaid diagrams for design docs (C4, sequence, flowchart, ER). Extract, render, embed. |
| `plantuml` | [plantuml](https://github.com/SpillwaveSolutions/plantuml) | PlantUML generation, extraction from Markdown, image export, and updated docs with image links. |
| `google-docs-style` | [google-docs-style](https://github.com/SpillwaveSolutions/google-docs-style) | Google developer documentation style guide + formatter + hooks. |
| `ste100` | [ste100-agent-plugins](https://github.com/SpillwaveSolutions/ste100-agent-plugins) | ASD-STE100 Simplified Technical English gate with local TypeScript orchestrator / editor / adversary loop. No external API calls. |

Supports **Claude Code**, **Grok Build**, **Codex**, **Cursor**, and the universal Agent Plugins 1.0 standard. Tracking via WikiTicket SDD.

This is a specialized catalog. Broader domain skills live in [`skills-marketplace`](https://github.com/SpillwaveSolutions/skills-marketplace). Knowledge packs live in [`second-brain-marketplace`](https://github.com/SpillwaveSolutions/second-brain-marketplace).

## Install

```bash
# Claude Code / Grok Build
/plugin marketplace add SpillwaveSolutions/spillwave-documentation-marketplace
/plugin install document-specialist@spillwave-documentation
/plugin install design-doc-mermaid@spillwave-documentation
/plugin install plantuml@spillwave-documentation
/plugin install google-docs-style@spillwave-documentation
/plugin install ste100@spillwave-documentation
```

Or install individual repos with Skilz:

```bash
skilz install SpillwaveSolutions/document-specialist-skill
skilz install SpillwaveSolutions/design-doc-mermaid
skilz install SpillwaveSolutions/plantuml
skilz install SpillwaveSolutions/google-docs-style
skilz install SpillwaveSolutions/ste100-agent-plugins
```

Codex and Cursor consume the host-specific plugin manifests shipped by each source repo.

## Why this suite

- **document-specialist** owns the full lifecycle of software docs.
- **design-doc-mermaid** + **plantuml** give first-class diagram support (the specialist already invokes them).
- **google-docs-style** enforces clear, consistent developer writing.
- **ste100** adds controlled Simplified Technical English for procedures, runbooks, and regulated content.

Together they form a complete documentation workstation for agents.

## Related

- [skills-marketplace](https://github.com/SpillwaveSolutions/skills-marketplace) — broader skill catalog
- [second-brain-marketplace](https://github.com/SpillwaveSolutions/second-brain-marketplace) — OKF / second-brain packs
- [wiki_ticket_sdd](https://github.com/SpillwaveSolutions/wiki_ticket_sdd) — work tracking

MIT © Rick Hightower / Spillwave Solutions
