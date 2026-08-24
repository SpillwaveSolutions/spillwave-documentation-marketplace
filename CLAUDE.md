# CLAUDE.md

This is the Spillwave Documentation Marketplace.

It bundles five documentation-related agent skills/plugins:

1. **document-specialist** — Professional software documentation (SRS, PRD, OpenAPI, manuals, runbooks) with Progressive Disclosure Architecture. Mermaid-first diagrams. PlantUML for wireframes and leftover UML.
2. **design-doc-mermaid** — Default Mermaid diagrams for design docs, walkthroughs, and requirements (C4, sequence, class, ER, state, flowchart).
3. **plantuml** — Wireframes, use case, timing, ArchiMate, plus image export. GitHub wiki does not render PlantUML source.
4. **google-docs-style** — Google developer documentation style guide + formatters/hooks.
5. **ste100** — ASD-STE100 Simplified Technical English gate (local, offline).

Multi-host support: Claude Code, Grok Build, Codex, Cursor, Agent Plugins 1.0.

See README.md and marketplace.json for install and plugin details.

## Style and wiring

- Default voice for document-specialist: STE100.
- Alternate voice: google-docs-style, only when the user names it.
- Never mix the two packs.
- No em dash. No sentence starting with So, That, Thus, or Hence.
- WikiTicket architecture docs, code walkthroughs, and requirements docs call
  document-specialist + design-doc-mermaid. PlantUML is opt-in for wireframes
  and leftover UML.
- GitHub wiki: Mermaid inline. PlantUML as uploaded images.
- Confluence: images for both Mermaid and PlantUML.
