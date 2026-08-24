# CLAUDE.md

This is the Spillwave Documentation Marketplace.

It bundles five documentation-related agent skills/plugins:

1. **document-specialist** — Professional software documentation (SRS, PRD, OpenAPI, manuals, runbooks) with Progressive Disclosure Architecture.
2. **design-doc-mermaid** — Mermaid diagrams + design document generation from code or templates.
3. **plantuml** — PlantUML diagram generation, extraction, and image conversion.
4. **google-docs-style** — Google developer documentation style guide + formatters/hooks.
5. **ste100** — ASD-STE100 Simplified Technical English gate (local, offline).

Multi-host support: Claude Code, Grok Build, Codex, Cursor, Agent Plugins 1.0.

See README.md and marketplace.json for install and plugin details.

## Style and wiring

- Default voice for document-specialist: STE100.
- Alternate voice: google-docs-style, only when the user names it.
- Never mix the two packs.
- No em dash. No sentence starting with So, That, Thus, or Hence.
- WikiTicket architecture docs and code walkthroughs must call
  document-specialist + design-doc-mermaid + plantuml.
