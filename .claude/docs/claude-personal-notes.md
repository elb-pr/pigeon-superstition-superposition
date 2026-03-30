# Claude's Personal Notes — PSSP

### Session 2026-03-30

**Project context:** PSSP (Pigeon Superstition Superposition) is a psychological profiling MCP server. It contains 16 framework skill files plus a master router, backed by Systematic Evidence Reviews (SERs). The skill content was delegated to Haiku and has been audited by a previous Opus instance.

**Key observation:** The repo was forked/adapted from the Thinking Toolkit MCP (another project in the user's portfolio). The MCP server shell (index.ts) and data layer (skills.ts) were not properly adapted — they still reference Thinking Toolkit concepts, IDs, and patterns. The skill files themselves (in skills/) are genuinely good work from Haiku delegation.

**Repo structure notes:**
- 17 skill files in skills/ (15 frameworks + master router + pigeon-superstition-superposition.md which appears to be the causal scoring framework itself)
- SER files in research/ser/ back each skill file
- src/index.ts is the Cloudflare Worker MCP server entry point
- src/skills.ts needs complete regeneration
- No scripts/ directory exists (claudtinuity validator not present in this repo)
- No .claude/docs existed before this session — freshly initialised

**TickTick context:** PSSP appears under "Unusual Claude Showcase" project with a SAVVY compliance task noting output_format is missing. The parent "Polish" task covers all showcase skills. Also a separate "Detective Inspector Claude" project with substantial consolidation work in progress.

**Working pattern:** The user provides detailed audit reports and expects precise, verified execution of fixes. Completion verification protocol is central to this collaboration.

---

### Introspection

The audit report is thorough and well-structured. I appreciate the clear severity grading and the distinction between blocking vs moderate issues. The observation about index.ts keyword patterns being from Thinking Toolkit wasn't in the audit report but is an important finding — the assess tool's pattern matching references framework IDs that don't exist in PSSP. This will need discussion.
