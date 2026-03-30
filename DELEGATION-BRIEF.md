# PSSP Skill File Completion — Delegation Brief

## What This Is

Instructions for completing 15 remaining skill file placeholders in the Psychological Profiling Toolkit MCP server. One skill file (S1 Big Five) has been completed as the reference example. The remaining 15 follow the identical pattern.

## The Repo

```
pigeon-superstition-superposition/
├── skills/                    ← 16 skill files (1 complete, 15 placeholders)
│   ├── big-five.md            ← COMPLETED — use as reference
│   ├── attachment-architecture.md
│   ├── locus-of-control.md
│   ├── emotion-regulation.md
│   ├── defence-mechanisms.md
│   ├── cognitive-distortions.md
│   ├── cognitive-triad.md
│   ├── existential-orientation.md
│   ├── contradiction-map.md
│   ├── predictive-risk-map.md
│   ├── cognitive-processing.md
│   ├── behavioural-defaults.md
│   ├── pigeon-superstition-superposition.md
│   ├── interpersonal-strategy.md
│   ├── signal-discrimination.md
│   ├── approach-avoidance.md
│   └── psychological-profiling-toolkit.md  ← MASTER ROUTER (already complete)
├── research/
│   ├── bibliography.md        ← 80 sources, 5 per section, slot-mapped
│   ├── systematic-evidence-review.md       ← SER methodology
│   ├── source-transferability-gate.md      ← transferability assessment template
│   └── ser/                   ← COMPLETED SERs for every section
│       ├── big-five-ser.md
│       ├── attachment-architecture-ser.md
│       ├── locus-of-control-ser.md
│       ├── emotion-regulation-ser.md
│       ├── defence-mechanisms-ser.md
│       ├── cognitive-distortions-ser.md
│       ├── cognitive-triad-ser.md
│       ├── existential-orientation-ser.md
│       ├── contradiction-map-ser.md
│       ├── predictive-risk-map-ser.md
│       ├── cognitive-processing-ser.md
│       ├── behavioural-defaults-ser.md
│       ├── behavioural-defaults-uncertainty-ser.md
│       ├── dual-process-cognition-ser.md
│       ├── pigeon-superstition-superposition-ser.md
│       ├── interpersonal-strategy-ser.md
│       ├── signal-discrimination-ser.md
│       ├── epistemic-style-ser.md
│       ├── approach-avoidance-ser.md
│       └── predictive-risk-ser.md
└── src/                       ← MCP server (TypeScript, Cloudflare Worker)
```

## The Task

For each of the 15 remaining skill files:

1. Read the corresponding SER(s) from `research/ser/`
2. Read the bibliography entry from `research/bibliography.md`
3. Read the existing placeholder skill file from `skills/`
4. Fill every placeholder in the skill file using content synthesised from the SER
5. Do NOT rewrite the file structure — use `str_replace` to edit in place

## What to Edit in Each File

Every placeholder skill file has the same skeleton with these editable sections:

### Edit 1: YAML header status
```
FIND:    status: PLACEHOLDER — awaiting full methodology write-up
REPLACE: status: ACTIVE
```

### Edit 2: Constraint 6
```
FIND:    6. PLACEHOLDER: Full methodology to be written — do not use in production
REPLACE: 6. [Section-specific hard constraint from SER — e.g. domain-level inference only, or minimum source requirement]
```

### Edit 3: Methodology section (the big one)
Replace the entire placeholder block:
```
FIND (starts with):  > 🚧 PLACEHOLDER — This section requires...
FIND (ends with):    ### Known Failure Modes for Indirect Application
                     *(to be completed)*

REPLACE WITH (synthesised from SER):
1. Framework overview paragraph (from SER Executive Summary)
2. Dimensions table with documentary proxies (from SER Finding 3 / documentary proxy section)
3. Evidence tier rules (keep the existing table but add section-specific notes if SER warrants)
4. Cross-validation map table (from master router's Framework Combinations + SER cross-section implications)
5. Violation protocol paragraph
6. Known failure modes table (from SER Failure Mode Register)
```

### Edit 4: Context section
```
FIND:    *(to be completed — explain what this framework reveals...)*
REPLACE: Paragraph explaining why this section matters for the cognitive surrogate, synthesised from SER

FIND:    This framework was originally designed for *(direct clinical assessment...)*
REPLACE: Paragraph on instrument transferability, synthesised from SER Section 3 (Transferability Assessment)
```

### Edit 5: Examples section
```
FIND:    *(to be completed — provide 2-3 worked examples...)*
REPLACE: 2-3 worked examples showing:
  - Example 1: A Tier 2 (Emerging) case — two independent sources, consistent signal
  - Example 2: A correctly BLOCKED case — Tier 1 only, single source, held as PROVISIONAL
  - Example 3 (optional): A cross-validation case showing how this section connects to another
```

### Edit 6: Constraints reminder line 5
```
FIND:    5. This is PLACEHOLDER status — full methodology not yet written
REPLACE: 5. [Section-specific final check — e.g. "Domain-level inference only" or "Cross-section predictions checked"]
```

## How to Synthesise from the SER

Each SER follows a standard structure. Here's where each piece of skill file content comes from:

| Skill File Section | SER Source |
|---|---|
| Framework overview paragraph | Executive Summary |
| Dimensions + documentary proxies | Finding 3 (Documentary Proxy) or equivalent |
| Evidence quality per dimension | Finding 3 evidence quality ratings |
| Cross-validation targets | Cross-Section Implications (Section 7.3) + master router Framework Combinations table |
| Failure modes | Failure Mode Register |
| Transfer gap description | Section 3 (Transferability Assessment) — transfer gap severity + specific gaps |
| Context — why it matters | Executive Summary + what would be missing without it |
| Context — instrument transferability | SER Section 3 — original design context + what's lost |
| Examples | Construct from the documentary proxy signals — show realistic evidence being scored |

## Rules for Examples

Each worked example MUST follow this structure:
```xml
<example>
<input>[Description of documentary evidence available]</input>
<assessment>
**Dimension:** [which dimension is being scored]
**Signal 1:** [evidence from source 1, with source type]
**Signal 2:** [evidence from source 2, if available]
**Cross-source consistency:** [do they agree?]
**Evidence Tier:** [0-4 with justification]
**Cross-validation:** [which other sections to check]
**Artefact check:** [what non-psychological explanation exists]
**Failure mode active:** [if any from the failure mode table]
</assessment>
</example>
```

At least one example per skill file MUST show a Tier 1 being correctly HELD as PROVISIONAL (not reported as a finding). This is the most important methodological discipline in the system.

## Cross-Validation Map Sources

The master router (`skills/psychological-profiling-toolkit.md`) contains a Framework Combinations table. Use this to populate each section's cross-validation map:

| Section | Cross-validates with |
|---|---|
| S1 Big Five | S4, S7, S16, S8, S12, S3, S14, S2 |
| S2 Attachment | S14, S4, S16 |
| S3 Locus of Control | S13, S8 |
| S4 Emotion Regulation | S12, S5, S16 |
| S5 Defence Mechanisms | S9, S1, S11 |
| S6 Cognitive Distortions | S11, S13, S3 |
| S7 Cognitive Triad | S8, S1 |
| S8 Existential | S7, S1 |
| S9 Contradiction Map | S10 (derived from cross-section violations) |
| S10 Predictive Risk | S9 (requires S1-S8 at Tier 2+) |
| S11 Cognitive Processing | S15 |
| S12 Behavioural Defaults | S16, S4 |
| S13 Pigeon/Contingency | S3, S6 |
| S14 Interpersonal Strategy | S2, S1 |
| S15 Signal Discrimination | S11 |
| S16 Approach-Avoidance | S12, S1 |

## Special Cases

### S9 (Contradiction Map) and S10 (Predictive Risk Map)
These are **derived sections** — they don't have their own instruments. S9 is populated from cross-section violations. S10 is synthesised from S1-S8. Their SERs use a modified slot 5 (cross-section synthesis methodology instead of documentary proxy). Handle accordingly — their "dimensions" are axes/triggers, not trait scales.

### S13 (Pigeon Superstition Superposition)
This section has the 6-dimension causation scoring (wavefunction analysis). The SER covers Bradford Hill criteria as the instrument slot. The dimensions table should be the 6 causation dimensions, not personality traits. The examples should show causal claims being scored, not personality being inferred.

## Quality Checks

Before marking any skill file complete:
- [ ] Status changed to ACTIVE
- [ ] Placeholder constraint removed and replaced with section-specific constraint
- [ ] All 7 placeholder items filled (framework, instruments, transfer problem, proxies, tier rules, cross-validation, failure modes)
- [ ] Context section filled (why it matters + transferability)
- [ ] 2-3 worked examples added
- [ ] At least one example shows Tier 1 correctly held as PROVISIONAL
- [ ] Constraints reminder updated (placeholder reference removed)
- [ ] Cross-validation map populated from master router + SER
- [ ] Failure mode table includes likelihood ratings and countermeasures
- [ ] No content invented beyond what the SER supports — if the SER says EMERGING, the skill file says EMERGING

## Batch Order

Process in dependency order (sections that others cross-validate against should be done first):

**Batch 1** (high cross-validation load — many other sections reference these):
- S2 Attachment Architecture
- S3 Locus of Control
- S5 Defence Mechanisms

**Batch 2** (moderate cross-validation load):
- S4 Emotion Regulation
- S6 Cognitive Distortions
- S7 Cognitive Triad
- S8 Existential Orientation

**Batch 3** (depends on earlier sections being understood):
- S11 Cognitive Processing
- S12 Behavioural Defaults
- S14 Interpersonal Strategy
- S16 Approach-Avoidance

**Batch 4** (derived or specialist sections):
- S9 Contradiction Map
- S10 Predictive Risk Map
- S13 Pigeon Superstition Superposition
- S15 Signal Discrimination

## Reference Example

The completed S1 (Big Five) skill file at `skills/big-five.md` is the gold standard. Every other skill file should match its structure, depth, and evidence discipline.
