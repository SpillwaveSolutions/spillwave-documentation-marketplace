# Spillwave Documentation Marketplace

Focused multi-host marketplace for **professional software documentation skills**.

Claude Code reads [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json). Plugin sources are GitHub objects, not raw URLs.

Bundles five complementary plugins:

| Plugin | Repo | What it does |
|--------|------|--------------|
| `document-specialist` | [document-specialist-skill](https://github.com/SpillwaveSolutions/document-specialist-skill) | Greenfield templates (SRS, PRD, OpenAPI, user manuals, runbooks) + brownfield reverse-engineering from Spring Boot / FastAPI. Progressive Disclosure Architecture. Markdown / DOCX / PDF. Mermaid-first diagrams, PlantUML wireframes. |
| `design-doc-mermaid` | [design-doc-mermaid](https://github.com/SpillwaveSolutions/design-doc-mermaid) | Default diagrams for design docs (C4, sequence, flowchart, class, ER, state). Extract, render, embed. |
| `plantuml` | [plantuml](https://github.com/SpillwaveSolutions/plantuml) | Leftover UML (use case, timing, ArchiMate), Salt wireframes, and image export. GitHub wiki never renders PlantUML source. |
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

- **document-specialist** owns the full lifecycle of software docs, including wireframes.
- **design-doc-mermaid** is the default diagram tool on GitHub wiki.
- **plantuml** covers wireframes and UML types Mermaid cannot do easily, always as images.
- **google-docs-style** enforces clear, consistent developer writing.
- **ste100** adds controlled Simplified Technical English for procedures, runbooks, and regulated content.

Together they form a complete documentation workstation for agents.

## Style default

`document-specialist` writes prose in **STE100** unless the user names Google
style. The two voice packs are exclusive. Do not mix them.

Hard bans in both packs:

- No em dash (`—`) and no `--` used as an em dash.
- Do not start a sentence with **So**, **That**, **Thus**, or **Hence**.

## WikiTicket SDD wiring

When [wiki_ticket_sdd](https://github.com/SpillwaveSolutions/wiki_ticket_sdd)
creates an architecture doc, a code walkthrough, or a requirements doc, it must invoke:

1. `document-specialist` for prose (and wireframes)
2. `design-doc-mermaid` for GitHub-safe diagrams, including class, ER, state, and component views
3. `plantuml` only for leftover types (use case, timing, ArchiMate, Salt wireframes)

**GitHub wiki:** Mermaid stays in a fenced block. PlantUML is a PNG or SVG that
you commit and upload with the wiki page.

**Confluence:** render Mermaid and PlantUML to PNG or SVG and upload both.

## Related

- [skills-marketplace](https://github.com/SpillwaveSolutions/skills-marketplace) — broader skill catalog
- [second-brain-marketplace](https://github.com/SpillwaveSolutions/second-brain-marketplace) — OKF / second-brain packs
- [wiki_ticket_sdd](https://github.com/SpillwaveSolutions/wiki_ticket_sdd) — work tracking

MIT © Rick Hightower / Spillwave Solutions
