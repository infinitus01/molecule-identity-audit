# P1.2 Status Note

P1.2 focuses on preserving molecular identity boundaries around stereochemistry, fragments, salts, mixtures, and immutable artifacts.

## Public Status

Status: Done or under validation, depending on the deployment context.

This public showcase does not include the full private edge-case corpus or regression harness.

## Scope

P1.2 addresses cases where a structure can parse but should not automatically pass downstream claim gates.

Examples:

- unspecified stereochemistry
- salt forms
- fragments
- multicomponent structures
- metadata mismatch
- InChIKey mismatch
- immutable artifact drift
- fake stage PASS

## Boundary Rules

### Stereochemistry

Incomplete stereochemistry is not necessarily a parse failure.

It can be:

```text
parse: PASS
identity: PARTIAL
downstream: BLOCKED
```

### Salt / Fragment / Mixture

A salt, fragment, or multicomponent record must not be silently stripped or normalized into a different asserted entity for downstream claims.

### Immutable Artifact

An audit artifact should be reproducible. Volatile fields such as generation timestamps should not alter identity hashes unless they are intentionally part of the audit envelope.

### Stage Truthfulness

A displayed PASS must match evidence. If a prior stage is incomplete, downstream stage gates remain blocked.

## Private Work Not Included Here

- full failure map
- full negative test corpus
- resolver edge-case rules
- client review checklist
- commercial report templates
- production workflow details
