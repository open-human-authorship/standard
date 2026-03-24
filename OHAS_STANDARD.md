# Open Human Authorship Standard (OHAS)

**Version:** 0.1-draft  
**Status:** Public Draft for Open Review  
**License:** CC BY 4.0 for the specification text; Apache-2.0 or MIT for reference implementations  
**Repository Scope:** Open standard for certifying human-authored text creation workflows without generative AI in the certified writing process

---

## 1. Purpose

The **Open Human Authorship Standard (OHAS)** defines an open, reviewable, and implementable framework for certifying that a text was produced through a documented human writing process **without the use of generative AI within the certified scope**, according to declared policies, collected evidence, and an auditable chain of custody.

OHAS is designed for public discussion and iterative improvement in open repositories such as GitHub. It is intended for use by publishers, authors, schools, universities, literary prizes, archives, cultural institutions, and independent certification bodies.

OHAS does **not** claim to prove an absolute metaphysical truth that no AI was used anywhere under any circumstance. Instead, it defines how to certify:

1. a declared policy,
2. a documented writing workflow,
3. the evidence collected during that workflow,
4. the level of assurance achieved, and
5. the public verifiability of the resulting certification.

---

## 2. Design Principles

### 2.1 Verifiability
All certified claims must be supported by inspectable evidence.

### 2.2 Openness
The standard, profiles, schemas, and certification requirements must be publicly reviewable and implementable by multiple parties.

### 2.3 Technology Neutrality
OHAS does not mandate a single vendor, software stack, hosting model, or hardware platform.

### 2.4 Layered Assurance
The standard defines multiple assurance levels rather than a single binary label.

### 2.5 Process over Guesswork
OHAS prioritizes provenance, workflow controls, auditability, and evidence over stylistic “AI detectors” or probabilistic guesses.

### 2.6 Transparency
Any issued certification must disclose the applicable profile, assurance level, scope, exceptions, and issuer.

### 2.7 Accessibility
Equivalent compliance paths should exist for writers using assistive technologies, provided the profile rules remain enforceable and auditable.

---

## 3. Scope

OHAS applies to text-based works, including but not limited to:

- novels
- short stories
- essays
- poems
- scripts and plays
- scholarly manuscripts
- educational submissions
- speeches
- articles
- selected chapters or sections of larger works

Certification may apply to:

- a complete work,
- a named edition,
- a versioned manuscript,
- a section or chapter,
- a submission package,
- a defined writing session or set of sessions.

The certified scope **must** be explicitly identified in the certification manifest.

---

## 4. Terms and Definitions

### 4.1 Human Author
A natural person who creates the intellectual content of the text.

### 4.2 Generative AI
A computational system capable of producing original or pseudo-original text in response to prompts, examples, instructions, transformations, or probabilistic continuation.

### 4.3 Certified Scope
The exact textual content, version, and workflow boundaries covered by an OHAS certification.

### 4.4 Policy Profile
A defined rule set specifying what tools and actions are forbidden, allowed, or allowed only with disclosure.

### 4.5 Assurance Level
The degree of confidence provided by the certification process, based on controls, evidence, and audit depth.

### 4.6 Primary Evidence
Evidence directly documenting the writing process, such as signed version history, writing logs, handwritten drafts, controlled session records, or recorded workstation events.

### 4.7 Secondary Evidence
Corroborating evidence such as editorial testimony, stylometric consistency reports, room access logs, or timeline analysis.

### 4.8 Certification Issuer
The entity that issues an OHAS certificate after evaluating conformance.

### 4.9 Auditor
An independent evaluator who verifies workflow conformity, evidence integrity, and compliance with the selected OHAS profile.

### 4.10 Certified Writing Environment
A digital and optionally physical environment configured to enforce or support OHAS requirements for a given assurance level.

---

## 5. Normative Statement Keywords

The key words **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** in this document are to be interpreted as described in RFC 2119 and RFC 8174 when, and only when, they appear in all capitals.

---

## 6. Core Claim Model

An OHAS certification SHALL express the following claim structure:

> This text, within the certified scope, was produced according to OHAS profile `X` at assurance level `Y`, under the declared workflow and evidence requirements, with the following permitted and prohibited tool classes.

OHAS certifications MUST NOT claim absolute impossibility of concealed or out-of-band violations. They MAY claim that no nonconformities were identified within the certified process and evidence set.

---

## 7. Policy Profiles

OHAS uses policy profiles to define what “without AI” means in a concrete and testable way.

### [7.1 Profile P1 — No Generative AI for Text Creation](profiles/P1-no-generative-ai.md)
The certified text MUST NOT include text generated, rewritten, expanded, or substantially transformed by generative AI.

Allowed examples MAY include:
- file saving
- non-generative spell checking
- formatting
- local backup
- non-semantic text editor features

Forbidden examples MUST include:
- prompt-based paragraph generation
- LLM-based rewriting
- AI summarization incorporated into the work
- predictive co-writing beyond a defined minimal autocomplete threshold
- paraphrasing tools using generative models

### [7.2 Profile P2 — No Generative AI in Core Text; AI Allowed Outside Text Body](profiles/P2-no-ai-in-text-creation.md)
Same as P1 for the text body, but AI MAY be used outside the certified text for activities such as cover ideation, layout support, or marketing copy, provided these are excluded from scope or explicitly disclosed.

### [7.3 Profile P3 — Human Authored with Declared AI Assistance Outside Certified Segments](profiles/P3-human-authored-with-declared-ai-support.md)
The certified content MUST identify which sections are fully human-authored and which surrounding processes used AI assistance.

### [7.4 Profile P4 — Educational Strict Mode](profiles/P4-educational-strict-mode.md)
A stricter profile for schools, universities, examinations, or coursework. It SHOULD include tighter restrictions on networks, device access, copy/paste, and external imports.

### [7.5 Profile P5 — Prize / Competition Mode](profiles/P5-prize-competition-mode.md)
A profile intended for literary prizes, contests, and public awards requiring stronger assurance and chain-of-custody controls.

Future profiles MAY be added through versioned public governance.

---

## 8. Assurance Levels

### 8.1 Level D0 — Self Declaration
The author declares compliance with a selected profile.

#### Minimum Requirements
- author identity or pseudonymous identity under issuer rules
- signed declaration
- final work hash
- profile selection
- certified scope definition

#### Characteristics
- minimal assurance
- no strong audit requirement
- mainly reputational value

### 8.2 Level D1 — Logged Human Process
The writing process is documented through version history and basic evidence capture.

#### Minimum Requirements
- all D0 requirements
- version snapshots or revision history
- timestamps
- tool disclosure
- basic consistency check

#### Characteristics
- low to medium assurance
- suitable for independent authors and lightweight publishing workflows

### 8.3 Level D2 — Controlled Workflow
The writing process takes place in a controlled digital environment with enforceable rules.

#### Minimum Requirements
- all D1 requirements
- certified writing tool or controlled workstation
- event logs
- import/paste controls
- declared allowed software list
- workflow dossier

#### Characteristics
- medium to high assurance
- suitable for publishers, institutions, and formal submissions

### 8.4 Level D3 — Audited Human Authorship
The D2 workflow is independently audited.

#### Minimum Requirements
- all D2 requirements
- independent audit report
- chain-of-custody review
- anomaly review
- evidence sampling or complete evidence review

#### Characteristics
- high assurance
- suitable for awards, institutional archives, and high-value manuscripts

### 8.5 Level D4 — Secure Certified Human-Only Environment
The text is created in a controlled digital and physical environment with the strongest OHAS controls.

#### Minimum Requirements
- all D3 requirements
- certified physical writing room or equivalent
- controlled device entry rules
- hardened workstation or verified boot environment
- monitored session controls under applicable law
- formal operator procedures

#### Characteristics
- very high assurance
- still not absolute proof
- suitable for premium or highly sensitive certification scenarios

---

## 9. Allowed, Forbidden, and Disclosable Actions

Each OHAS profile MUST define action classes.

### 9.1 Forbidden Actions
Examples include:
- generating text with an LLM for insertion into the certified scope
- rewriting text with a generative assistant
- expanding notes into prose using AI
- grammar/style rewrites driven by generative models where the rewrite affects certified text content
- bulk import of externally generated text without declared exclusion from scope

### 9.2 Allowed Actions
Examples may include:
- manual typing
- non-generative spellcheck
- page formatting
- saving, exporting, printing
- manual citation insertion
- offline dictionary lookup
- assistive text entry tools, where profile-compatible

### 9.3 Disclosable Actions
Examples may include:
- speech-to-text
- OCR of handwritten notes
- grammar tools requiring review by the author
- bibliographic search tools
- translation support outside the certified text body

Any action marked as “disclosable” MUST be recorded in the certification manifest when used.

---

## 10. Evidence Model

### 10.1 Evidence Categories
OHAS evidence MAY include:
- version history
- content hashes
- signed checkpoints
- editor session logs
- handwritten draft scans
- room access records
- workstation configuration attestations
- operator checklists
- audit reports
- export manifests
- screen or event logs where lawful and declared

### 10.2 Evidence Requirements
Evidence MUST be:
- attributable,
- timestamped,
- tamper-evident where feasible,
- linked to the certified scope,
- retained according to issuer policy.

### 10.3 Evidence Integrity
For D1 and above, significant versions SHOULD be hashed.  
For D2 and above, logs and checkpoints SHOULD be digitally signed.  
For D3 and D4, audit artifacts MUST be retained in a tamper-evident evidence package.

---

## 11. Work Identifier and Version Chain

Each certified work SHOULD receive a unique identifier in a format such as:

`ohas:work:<issuer>:<year>:<serial>`

Example:

`ohas:work:openhumanauth:2026:000001`

Each meaningful version SHOULD record:

- work ID
- version ID
- parent version ID
- timestamp
- author ID
- device or environment ID
- toolchain ID
- content hash
- active profile
- signature or attestation
- evidence references

---

## 12. Certification Manifest

Every OHAS certification MUST include a machine-readable and human-readable manifest.

### 12.1 Required Manifest Fields
- specification version
- certificate ID
- issuer
- issue date
- status
- work ID
- title
- author or author identity policy reference
- certified scope
- profile
- assurance level
- final content hash
- evidence summary
- exceptions or disclosures
- auditor reference, if applicable
- verification method

### 12.2 Suggested Serialization
The manifest MAY be serialized as:
- JSON
- YAML
- signed JSON-LD
- C2PA-compatible or adjacent provenance payloads
- W3C Verifiable Credential compatible structures

The current repository includes draft schemas and examples:

### Schemas
- [schemas/manifest.schema.json](schemas/manifest.schema.json)
- [schemas/version-record.schema.json](schemas/version-record.schema.json)

### Examples
- [examples/manifest.example.json](examples/manifest.example.json)
- [examples/version-record.example.json](examples/version-record.example.json)

---

## 13. Public Verification

An OHAS-compliant implementation SHOULD support public verification through one or more of the following:

- a public verification page
- a signed manifest file included with the work
- a QR code in the publication
- an API endpoint
- downloadable evidence summary

Public verification MUST allow a verifier to confirm at least:
- certificate validity
- profile
- assurance level
- issuer
- certified scope
- final content hash
- revocation or suspension status

---

## 14. Certified Writing Environment Requirements

### 14.1 General
A certified writing environment MUST support the applicable controls for its assurance level.

### 14.2 Software Requirements
For D2 and above, the writing environment SHOULD support:
- automatic versioning
- timestamping
- content hashing
- logging of session events
- import and paste tracking
- export of evidence dossier
- offline operation or controlled network mode

### 14.3 Paste and Import Control
For D2 and above, external paste or import SHOULD be restricted, disabled, or explicitly classified.

Suggested import classes:
- I1: brief personal notes
- I2: quotations and citations
- I3: authorized external reference text
- I4: noncompliant or prohibited import

For D4, unrestricted external paste MUST NOT be allowed.

### 14.4 Network Control
Profiles P4 and P5 SHOULD define network restrictions.  
For D4, the writing environment SHOULD be offline or on a tightly restricted allowlist-only network.

### 14.5 Software Allowlisting
For D2 and above, issuers SHOULD define an allowlist of permitted software categories and a denylist of prohibited generative tools.

---

## 15. Physical Certified Writing Space

OHAS defines an optional but recommended physical component for higher assurance levels.

### 15.1 Term
A physical writing space conforming to OHAS MAY be called a **Certified Human Writing Room (CHWR)**.

### 15.2 Purpose
A CHWR provides a controlled physical setting designed to reduce or prevent undisclosed use of generative AI and strengthen chain of custody.

### 15.3 Applicability
A CHWR is OPTIONAL for D0-D2, RECOMMENDED for D3, and NORMALLY REQUIRED for D4 unless an equivalent control framework is documented.

### 15.4 Minimum Physical Requirements
A CHWR SHOULD include:
- controlled entry and exit logging
- temporary storage for phones, smartwatches, tablets, and unauthorized devices
- a dedicated workstation
- clear session identification
- operator procedure or self-service procedure with logging
- controlled paper handling, if paper drafts are permitted
- documented room policy

### 15.5 Suggested Physical Size
A practical single-seat CHWR MAY be implemented in approximately **6-10 square meters**.  
A higher-comfort or supervised room MAY require **10-16 square meters**.  
Multi-seat installations SHOULD provide separate visual and acoustic privacy measures.

### 15.6 Functional Zones
A CHWR SHOULD define, where feasible:
- entry/check-in area
- personal device deposit area
- writing station area
- controlled paper handling area
- technical cabinet or secure support area

### 15.7 Physical Controls for D4
For D4, the room SHOULD include:
- logged check-in/check-out
- restricted device policy
- hardened workstation
- tamper-evident system state verification
- formal session start/end procedure
- retained operator or automated environment log

### 15.8 Privacy and Compliance
Any room monitoring, camera use, keystroke logging, or behavioral recording MUST comply with applicable privacy, labor, education, and data protection law.

See also:
- [docs/certified-writing-room.md](docs/certified-writing-room.md)

---

## 16. Audit Requirements

### 16.1 Audit Types
OHAS audits MAY include:
- documentary audit
- technical audit
- procedural audit
- physical environment audit
- sample-based audit
- full audit

### 16.2 Audit Objectives
The auditor MUST determine whether the evidence and workflow support the issued OHAS claim.

### 16.3 Audit Checks
The audit SHOULD review:
- scope definition
- profile compatibility
- evidence completeness
- timeline consistency
- imports and exceptions
- environment configuration
- operator adherence, where applicable
- nonconformities

### 16.4 Audit Outcome Categories
- conformant
- conformant with observations
- suspended pending remediation
- nonconformant
- revoked

### 16.5 Nonconformities
Nonconformities SHOULD be classified as:
- minor
- major
- critical

A critical nonconformity SHOULD block issuance or trigger revocation.

The repository currently includes informative audit guidance:

- [audit/audit-process.md](audit/audit-process.md)
- [audit/evidence-requirements.md](audit/evidence-requirements.md)
- [audit/nonconformities.md](audit/nonconformities.md)
- [audit/checklist-D1.md](audit/checklist-D1.md)
- [audit/checklist-D2.md](audit/checklist-D2.md)
- [audit/checklist-D3.md](audit/checklist-D3.md)
- [audit/checklist-D4.md](audit/checklist-D4.md)
- [audit/sample-audit-report.md](audit/sample-audit-report.md)
- [audit/revocation-process.md](audit/revocation-process.md)

Unless explicitly incorporated by governance or a future release, these audit documents are informative rather than normative.

---

## 17. Certificate Lifecycle

### 17.1 Issuance
A certificate MAY be issued only after required evidence and reviews are complete.

### 17.2 Suspension
A certificate MAY be suspended where unresolved concerns exist.

### 17.3 Revocation
A certificate MUST be revocable if fraud, material misrepresentation, or critical nonconformity is discovered.

### 17.4 Reissuance
A revised edition or corrected work SHOULD receive a new certificate ID and, where appropriate, a new final content hash.

---

## 18. Reference Data Structures

### 18.1 Minimal Manifest Example

```json
{
  "spec_version": "OHAS-0.1-draft",
  "certificate_id": "ohas:cert:openhumanauth:2026:000001",
  "status": "valid",
  "issuer": "Open Human Authorship Initiative",
  "issue_date": "2026-03-23",
  "work": {
    "work_id": "ohas:work:openhumanauth:2026:000001",
    "title": "Example Manuscript",
    "author": "Example Author"
  },
  "scope": "full text, version 1.0",
  "profile": "P1",
  "assurance_level": "D2",
  "final_content_hash": "sha256:REPLACE_ME",
  "evidence_summary": {
    "version_count": 48,
    "session_count": 12,
    "external_imports": 2
  },
  "disclosures": [
    "OCR used for handwritten notes import",
    "Non-generative spellcheck enabled"
  ],
  "verification": {
    "manifest_signature": "REPLACE_ME",
    "public_status_url": "REPLACE_ME"
  }
}
```

### 18.2 Version Record Example

```json
{
  "work_id": "ohas:work:openhumanauth:2026:000001",
  "version_id": "v00048",
  "parent_version_id": "v00047",
  "timestamp": "2026-03-23T10:12:00Z",
  "author_id": "author:example",
  "environment_id": "env:chwr-room-01:wks-01",
  "toolchain_id": "ohas-editor-0.1",
  "content_hash": "sha256:REPLACE_ME",
  "profile": "P1",
  "attestation": "REPLACE_ME"
}
```

---

## 19. Interoperability

OHAS SHOULD remain compatible, where practical, with:
- content provenance standards such as C2PA
- verifiable credential frameworks
- digital signatures and timestamping systems
- archival preservation workflows
- publishing metadata systems

OHAS does not require any single interoperability layer in version 0.1, but future versions SHOULD define formal mappings.

---

## 20. Accessibility Considerations

OHAS implementations MUST consider equivalent paths for writers who use assistive technologies.

Examples include:
- speech-to-text workflows
- screen readers
- alternative input devices
- dictated drafts later corrected by the same author

Profiles and issuers SHOULD clearly state how equivalent compliance is demonstrated in such cases.

---

## 21. Known Limits

OHAS explicitly recognizes the following limits:

1. It cannot prove with absolute certainty that no out-of-band AI use occurred.
2. It is stronger as a process certification than as a forensic detection system.
3. Higher assurance levels require greater operational cost and discipline.
4. Privacy, labor law, and data protection constraints may limit monitoring methods.
5. Different sectors may require different policy profiles.

These limits MUST be disclosed as part of honest implementation guidance.

---

## 22. Related Repository Documents

The repository also includes supporting documents:

### Project Entry and Contribution
- [README.md](README.md)
- [CONTRIBUTING.md](CONTRIBUTING.md)
- [CHANGELOG.md](CHANGELOG.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [LICENSE](LICENSE)

### Governance
- [governance/maintainers.md](governance/maintainers.md)

### Informative Documentation
- [docs/introduction.md](docs/introduction.md)
- [docs/use-cases.md](docs/use-cases.md)
- [docs/faq.md](docs/faq.md)
- [docs/architecture.md](docs/architecture.md)
- [docs/certified-writing-room.md](docs/certified-writing-room.md)
- [docs/threat-model.md](docs/threat-model.md)
- [docs/roadmap.md](docs/roadmap.md)

### Reference Implementations
- `/reference-implementations` (not yet defined)

### 22.1 Change Management
Changes SHOULD be proposed through pull requests, with issues used for:
- profile changes
- assurance level adjustments
- schema evolution
- control clarifications
- governance proposals

### 22.2 Versioning
The specification SHOULD use semantic or date-based versioning.  
Draft versions SHOULD clearly indicate that they are under public review.

### 22.3 Decision Process
The project SHOULD define a transparent maintainership and review process, including:
- who can approve changes,
- what counts as a breaking change,
- how profiles are added,
- how deprecations are announced.

---

## 23. Draft Status Statement

This document is a draft intended for open collaborative development. It SHOULD NOT yet be treated as a mature certification standard without further technical review, legal review, and pilot implementations.

---

## 24. Final Summary

OHAS v0.1 defines:

- a public claim model,
- policy profiles,
- assurance levels D0-D4,
- evidence requirements,
- manifest structure,
- public verification requirements,
- digital writing environment controls,
- an optional physical **Certified Human Writing Room** concept,
- open governance expectations for a public repository.
