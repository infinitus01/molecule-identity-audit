Molecule Identity Audit - Static Public Demo

Purpose
This folder is a Netlify Drop-ready static demo. It is intentionally read-only and does not connect to any API, backend, upload flow, analytics, or data collection service.

Public Positioning
Scientific Identity Audit
Molecular identity and evidence-boundary validation system

Primary Message
Before asking what a molecule does, verify what molecule it is.

Demo Boundary
This is not an AI drug discovery platform.
This demo only illustrates molecular identity and evidence-boundary validation.

Explicit Non-goals
- No pharmacology claim
- No ADMET prediction
- No clinical claim
- No investment advice
- No molecule recommendation
- No arbitrary molecule upload
- No backend execution

Static Fixture Logic
SMILES != InChIKey
-> STRUCTURE_IDENTITY_FAIL
-> pharmacology generation stopped
-> data room closed

Deploy
Drag the entire site/ folder into Netlify Drop.

Expected Netlify Drop Structure
site/
  index.html
  README.txt

Expected GitHub Showcase Repo Structure
README.md
docs/
  BASIC_STRUCTURE_AUDIT_TEMPLATE.md
  CLAIM_BOUNDARY.md
  ROADMAP.md
  P1_2_STATUS_NOTE.md
site/
  index.html
  README.txt
assets/
  screenshot.png

Notes
The screenshot.png file is stored at the repository root under assets/ for README display. It is not required for the Netlify static demo page.
