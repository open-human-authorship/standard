# Threat Model

## Purpose
This document summarizes important threat scenarios and limitations relevant to OHAS.

## Core Principle
OHAS is designed to reduce uncertainty through process evidence. It is not designed to eliminate all possible deception.

## Representative Threats

### 1. Off-Workflow Generation
An author generates text outside the controlled environment and later inserts it into the workflow.

Mitigations may include:
- controlled import
- clipboard logging
- version continuity review
- higher-assurance environments

### 2. Misleading Declarations
A claimant falsely states that no prohibited AI use occurred.

Mitigations may include:
- stronger evidence requirements
- audit
- sanctions or revocation process

### 3. Evidence Tampering
Logs or manifests are altered after the fact.

Mitigations may include:
- signatures
- append-only records
- retention policies
- independent review

### 4. Ambiguous Scope
A claimant uses AI outside scope but presents the certification as if it covered everything.

Mitigations may include:
- precise scope statements
- explicit profile language
- public manifest clarity

### 5. Overreliance on Detection Tools
A reviewer uses detector scores as though they were proof.

Mitigations may include:
- policy prohibition on detector-only conclusions
- evidence-based review

### 6. Accessibility Conflicts
Strict controls unintentionally block legitimate assistive technologies.

Mitigations may include:
- explicit accommodation policy
- alternative evidence models
- institution-defined exceptions

## Residual Risk
Even strong controls leave residual risk. OHAS should communicate assurance honestly and avoid false certainty.
