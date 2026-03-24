# Evidence Requirements by Assurance Level

## Status
Informative guidance aligned with `OHAS_STANDARD.md` v0.1.

## Purpose
This document summarizes the typical evidence expected for OHAS assurance levels D0 through D4.

Repository adopters may refine these requirements, but changes should remain consistent with the normative standard.

## Shared Baseline Evidence
The following items are generally expected across all levels:

- work identifier
- scope statement
- assurance level claim
- profile claim
- final content hash
- author declaration
- issuer or applicant identification

## D0 — Self Declaration
Typical evidence:

- signed or otherwise attributable author declaration
- final work hash
- title and scope metadata
- date of submission or issuance

Expected assurance:
Low. D0 primarily documents a claim rather than a controlled process.

## D1 — Logged Human Process
Typical evidence:

- all D0 evidence
- version history or dated draft sequence
- basic toolchain declaration
- session timestamps or equivalent chronology evidence
- simple exception log, if relevant

Expected assurance:
Moderate. D1 should show a plausible and continuous human drafting process.

## D2 — Controlled Workflow
Typical evidence:

- all D1 evidence
- controlled-editor or managed-workstation records
- session logs
- policy-state records
- import or clipboard records where applicable
- device or environment identification
- restricted toolchain evidence
- documented workflow policy

Expected assurance:
Moderate to high. D2 should show that drafting occurred under defined controls.

## D3 — Audited Human Authorship
Typical evidence:

- all D2 evidence
- independent audit record
- evidence review notes
- formal finding or attestation
- stronger chain-of-custody documentation
- supervisory or procedural records where relevant

Expected assurance:
High. D3 should demonstrate both controlled process and independent review.

## D4 — Certified Human-Only Secure Environment
Typical evidence:

- all D3 evidence
- certified writing room or secure environment records
- access logs
- session supervision records where applicable
- room or workstation integrity records
- device-control evidence
- physical-material handling records if handwritten notes are used
- enhanced retention and custody documentation

Expected assurance:
Very high, though not absolute.

## Evidence Qualities
Evidence should be evaluated not only for presence but also for quality.

Key qualities include:

- authenticity
- integrity
- traceability
- legibility
- relevance to scope
- temporal coherence
- policy relevance

## Missing or Weak Evidence
Weak evidence does not always require rejection. The consequence depends on:

- claimed assurance level
- severity of the gap
- compensating controls
- whether the gap affects core scope or only supporting detail

## Suggested Evidence Bundle Structure
A practical evidence bundle may include:

- `manifest.json`
- `author-declaration.pdf`
- `version-log.json`
- `session-logs/`
- `environment/`
- `audit-report.pdf`
- `exceptions.json`

## Notes
Issuers should document any alternative evidence model they accept, especially for accessibility accommodations, educational settings, or prize workflows.
