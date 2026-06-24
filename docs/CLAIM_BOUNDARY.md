# Claim Boundary

The public demo and methodology use a strict claim boundary.

## Core Rule

Molecular identity validation is not pharmacology validation.

A valid structure does not imply:

- biological activity
- drug-likeness
- ADMET suitability
- toxicity profile
- clinical potential
- commercial value

## Approved Public Language

Use:

```text
Molecule Identity Audit
Scientific Identity Audit
Evidence-boundary validation
Fail-closed validation contract
Structure identity and metadata consistency
Downstream claim blocked
```

Use with context:

```text
Basic Structure Audit
Immutable structure artifact
Identity consistency check
Stage-gate validation
```

## Avoid

Do not describe this demo as:

```text
AI drug discovery
drug prediction platform
ADMET predictor
toxicity predictor
docking engine
target-fit engine
clinical prediction tool
molecule recommendation engine
```

## Fail-closed Wording

Preferred:

```text
The identity evidence is inconsistent, so downstream claims remain blocked.
```

Avoid:

```text
The molecule is fake.
```

Preferred:

```text
The submitted structure can parse, but identity metadata does not match the asserted record.
```

Avoid:

```text
The molecule failed chemistry.
```

Preferred:

```text
No database match is not evidence of invalidity.
```

Avoid:

```text
The database says this molecule does not exist.
```

## Public Disclaimer

Use this statement on public pages:

```text
This demo does not predict activity, ADMET, toxicity, clinical success, drug-likeness, or investment value. It only illustrates molecular identity and evidence-boundary validation.
```
