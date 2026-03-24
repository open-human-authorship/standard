# Nonconformities

## Status
Informative guidance aligned with `OHAS_STANDARD.md` v0.1.

## Purpose
This document defines a practical classification model for nonconformities observed during an OHAS review or audit.

## Classification Categories

### Minor Nonconformity
A limited issue that does not materially undermine the claimed assurance level by itself.

Examples:
- incomplete metadata field
- missing nonessential reference
- formatting inconsistency in records
- late but recoverable evidence labeling

Typical response:
- correction requested
- certification may proceed with note or observation

### Major Nonconformity
A significant issue that weakens confidence in the claim and usually requires corrective action before a positive conclusion.

Examples:
- incomplete version history for a D1 or higher claim
- uncontrolled import event without sufficient explanation
- mismatch between declared tools and observed workflow
- incomplete session records in a controlled environment claim
- ambiguous certification scope

Typical response:
- corrective action required
- certification normally paused or downgraded until resolved

### Critical Nonconformity
A severe issue that undermines the core reliability of the certification claim.

Examples:
- falsified declaration
- evidence tampering
- undisclosed use of prohibited tools within certified scope
- fabricated logs
- broken chain of custody for a D3 or D4 claim
- major discrepancy suggesting the certified text was produced outside the claimed workflow

Typical response:
- certification denied, suspended, or revoked
- challenge or enforcement procedure triggered where applicable

## Observations
An observation is not a nonconformity but a point worth recording.

Examples:
- process could be documented more clearly
- retention policy could be improved
- scope statement should be simplified for public understanding

## Downgrade vs Failure
In some cases the correct outcome is not rejection but downgrade.

Examples:
- a claim made at D3 may still support D2
- a claim made at D2 may still support D1
- a P1 workflow may be better represented as P2 if AI use occurred outside the certified scope and was properly disclosed

## Repeated Issues
Repeated minor issues across multiple evidence items may together form a major nonconformity.

## Documentation
Every nonconformity record should include:

- identifier
- description
- related requirement or expectation
- severity
- evidence reference
- proposed action
- disposition
- date

## Suggested Record Format
A practical record may be structured as:

- NC-ID
- Title
- Severity
- Description
- Related scope
- Evidence reference
- Proposed corrective action
- Auditor note
- Final status

## Notes
Nonconformity processes should remain evidence-based and proportionate. OHAS should not be used to support speculative accusations without documented review.
