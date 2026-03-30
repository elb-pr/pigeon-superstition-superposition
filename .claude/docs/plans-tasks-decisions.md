# Plans, Tasks & Decisions — PSSP

## Active Plans

### plan-2026-03-30-pssp-audit-fixes
**Status:** active
**Created:** 2026-03-30
**Goal:** Resolve all issues identified in the PSSP Skill File Audit Report

---

## Active Tasks

### T1 — BLOCKING: Regenerate src/skills.ts
**Priority:** high
**Plan:** plan-2026-03-30-pssp-audit-fixes
**Status:** pending
**Detail:** skills.ts contains Thinking Toolkit MCP content, not PSSP. Must regenerate from 16+1 skill files in skills/, using exports index.ts expects: FRAMEWORKS, FRAMEWORK_MAP, FRAMEWORK_TABLE. Interface must include FrameworkEntry (id, name, description, content) and FRAMEWORK_TABLE entries (frameworkId, framework, profile_signal).

### T2 — index.ts audit: assess tool keyword patterns
**Priority:** high
**Plan:** plan-2026-03-30-pssp-audit-fixes
**Status:** pending
**Detail:** The assess tool in index.ts has keyword patterns from the Thinking Toolkit (cause-effect-confusion, temporal-blindness, etc). These need replacing with PSSP-appropriate patterns. Tool descriptions are partially adapted but still reference "stuck-type" language. get_thinking_toolkit tool name also needs renaming.

### T3 — Add Tier 1 PROVISIONAL example to attachment-architecture.md
**Priority:** medium
**Plan:** plan-2026-03-30-pssp-audit-fixes
**Status:** pending
**Detail:** Neither existing example demonstrates a Tier 1 observation being correctly held as PROVISIONAL. Add third example showing single-source attachment signal blocked at Tier 1.

### T4 — Add S9 cross-validation reference to predictive-risk-map.md
**Priority:** medium
**Plan:** plan-2026-03-30-pssp-audit-fixes
**Status:** pending
**Detail:** Master router specifies S10 cross-validates with S9 (Contradiction Map). predictive-risk-map.md has zero references to S9. Add S9 reference noting unresolved contradictions as risk factors.

---

## Done

(none yet)

---

## Decisions

(none yet)
