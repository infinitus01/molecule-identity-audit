# Basic Structure Audit Template

This template is a public-facing example of how a molecule identity audit can be reported without making pharmacology claims.

## Audit Summary

| Field | Value |
|---|---|
| Artifact ID | `<artifact-id>` |
| Submitted structure | `<SMILES / Molfile / SDF reference>` |
| Asserted identifier | `<InChIKey / registry ID / external record ID>` |
| Audit status | `PASS / PARTIAL / FAIL / STOP` |
| Downstream stage gate | `OPEN / BLOCKED` |
| Reason code | `<reason-code>` |

## Identity Checks

| Check | Status | Notes |
|---|---|---|
| Structure parse | `PASS / FAIL` | Can the submitted structure be parsed? |
| Sanitization | `PASS / FAIL` | Does the structure pass basic chemical sanitization? |
| InChIKey consistency | `PASS / FAIL / PARTIAL` | Does computed identity match the asserted record? |
| Formula / mass consistency | `PASS / FAIL / PARTIAL` | Are computed descriptors consistent with submitted metadata? |
| Stereochemistry completeness | `PASS / PARTIAL / FAIL` | Are required stereocenters specified? |
| Salt / fragment / mixture audit | `PASS / PARTIAL / FAIL` | Is the submitted material a single intended entity? |
| Immutable artifact hash | `PASS / FAIL` | Can the audit artifact be reproduced without timestamp drift? |

## Evidence Boundary

```text
If identity fails:
  downstream pharmacology generation must stop.

If identity is partial:
  downstream claims remain blocked until reviewed.

If database lookup has no match:
  do not infer that the molecule is fake.
```

## Output Contract

| Output | Meaning |
|---|---|
| `STRUCTURE_PARSE_FAIL` | The structure cannot be parsed. |
| `STRUCTURE_IDENTITY_FAIL` | Parsed structure does not match asserted identity metadata. |
| `IDENTITY_PARTIAL` | Identity evidence is incomplete or ambiguous. |
| `DOWNSTREAM_STAGE_BLOCKED` | Claims and predictions remain closed until identity is resolved. |
| `AUDIT_PASS` | Identity and boundary checks are sufficient for the configured stage. |

## Non-goals

This audit does not generate:

- activity prediction
- ADMET prediction
- toxicity prediction
- docking score
- clinical conclusion
- molecule recommendation
