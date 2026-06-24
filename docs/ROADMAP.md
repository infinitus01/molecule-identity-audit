# Roadmap

This roadmap is intentionally public-facing and high level. It establishes direction without publishing full resolver logic, private regression cases, or commercial workflow details.

## Completed / Publicly Represented

### P0 - Fail-closed Public Demo

Status: Done

- Static Netlify demo
- Read-only fixture
- No upload
- No backend
- No API
- No data collection
- Explicit non-goals

### P1 - Structure Identity Audit Foundation

Status: Done in private validation workflow; publicly represented as methodology

- Structure parse / sanitize boundary
- Computed identifier consistency
- Formula / mass consistency concept
- Stage-gate behavior

### P1.1 - Input Scope and Stage Truthfulness

Status: Done in method design

- A stage PASS must be earned by evidence.
- A structure parse PASS is not an identity PASS.
- A demo PASS is not production readiness.
- A database no-match is not a fake-molecule conclusion.

### P1.2 - Stereo / Fragment / Salt / Immutable Artifact Foundation

Status: Public status note available

- Stereochemistry completeness boundary
- Fragment / salt / multicomponent audit boundary
- Immutable artifact concept
- No silent normalization for downstream claims

## Planned

### P2 - Database Identity Resolution

Status: Planned

High-level goal: compare submitted identity metadata against external identity sources without over-claiming from missing data.

Implementation details are not public in this showcase repository.

### P3 - Evidence Ledger Validation

Status: Planned

High-level goal: preserve source, timestamp, transformation, and claim boundary context for audit review.

Implementation details are not public in this showcase repository.

### P4 - Basic Structure Audit Report Export

Status: Planned

High-level goal: produce reviewable audit reports for identity validation outcomes.

### P5 - Batch CSV / SDF Audit

Status: Planned

High-level goal: support batch-level identity audit while preserving per-artifact evidence boundaries.

## Not Planned for This Public Demo

- pharmacology prediction
- ADMET prediction
- toxicity prediction
- docking
- clinical prediction
- molecule recommendation
- production SaaS account system
