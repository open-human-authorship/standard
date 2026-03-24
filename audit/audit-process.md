# Audit Process

## Status
Informative guidance aligned with `OHAS_STANDARD.md` v0.1.

## Purpose
This document describes a practical audit flow for evaluating whether a work, workflow, or certified writing environment conforms to an OHAS assurance level and policy profile.

This document is informative unless explicitly adopted by an issuer or repository governance process.

## Audit Objectives
An OHAS audit should determine:

- whether the claimed scope of certification is clearly defined
- whether the declared assurance level is supported by the available evidence
- whether the selected profile has been applied consistently
- whether the chain of custody is coherent and materially trustworthy
- whether any exceptions, deviations, or nonconformities affect certification status

## Audit Types
The following audit types may be used alone or in combination:

### Document Review
Review of manifests, declarations, logs, version records, and supporting files.

### Technical Review
Inspection of toolchain settings, workstation controls, logging behavior, network policy, and integrity protections.

### Procedural Review
Evaluation of how sessions, evidence collection, supervision, and approval decisions are carried out.

### Physical Review
Inspection of a certified writing room or controlled writing environment where relevant.

### Sampling Audit
Review of selected sessions, versions, or evidence items rather than the full corpus.

### Full Audit
Review of the complete evidence bundle and related controls.

## Baseline Audit Flow

### 1. Intake
The auditor receives:

- the certification claim
- the requested assurance level
- the selected profile
- the scope definition
- the evidence bundle
- any prior findings or relevant declarations

### 2. Completeness Check
The auditor confirms that the submission is sufficiently complete to begin review.

Typical intake checks include:

- manifest present
- final content hash present
- author declaration present
- assurance level stated
- profile stated
- evidence references resolvable
- issuer or applicant contact information present

### 3. Scope Validation
The auditor confirms what exactly is being certified.

This may include:

- full work
- certified chapters only
- a specific edition
- a competition submission
- a supervised educational artifact

If scope is ambiguous, the audit should not proceed to a positive conclusion.

### 4. Evidence Review
The auditor reviews the evidence required by the declared assurance level.

Examples include:

- version history
- session logs
- workstation records
- environment records
- supervision records
- exception logs
- declarations and acknowledgments

### 5. Consistency Analysis
The auditor evaluates whether the evidence is internally consistent.

Consistency checks may include:

- chronology of versions
- relationship between parent and child versions
- plausibility of session timing
- presence of abrupt unexplained text insertion
- consistency between declared tools and observed logs
- alignment between claimed restrictions and actual environment configuration

### 6. Exception Review
Any declared exceptions must be reviewed for:

- legitimacy
- policy compatibility
- correct scope treatment
- correct logging and disclosure

### 7. Nonconformity Classification
Observed issues should be classified according to `audit/nonconformities.md`.

### 8. Draft Finding
The auditor prepares a draft conclusion such as:

- conforming
- conforming with observations
- pending corrective action
- nonconforming
- insufficient evidence

### 9. Applicant Response
Where the process allows it, the applicant or issuer may respond to findings, provide missing evidence, or contest factual inaccuracies.

### 10. Final Decision
A final decision is issued and recorded.

## Minimum Review Focus by Assurance Level

### D0
Focus on declaration integrity and final work identification.

### D1
Focus on version history, timeline coherence, and basic toolchain declarations.

### D2
Focus on controlled workflow evidence, restrictions, and session integrity.

### D3
Focus on all D2 requirements plus independent review quality and chain-of-custody robustness.

### D4
Focus on all D3 requirements plus certified physical environment controls and strong operational assurance.

## Audit Outputs
An audit output should normally contain:

- work identifier
- scope reviewed
- assurance level evaluated
- profile evaluated
- summary of evidence reviewed
- findings
- nonconformities, if any
- conclusion
- date
- auditor identity or role
- review limitations

## Independence and Conflicts
Where OHAS is used for formal certification, auditors should disclose conflicts of interest and apply a documented independence policy.

## Record Retention
Issuers should define retention periods for:

- manifests
- reports
- evidence indexes
- declarations
- challenge records
- revocation decisions

## Notes
OHAS audits should avoid overreliance on AI detection tools. Such tools may be used, if at all, only as secondary signals and not as primary proof of authorship or non-authorship.
