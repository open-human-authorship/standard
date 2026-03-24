# OHAS Architecture Overview

## Purpose
This document gives a non-normative overview of the main components of OHAS.

## Main Layers

### 1. Policy Layer
This layer defines what is being claimed.

Examples:
- no generative AI in certified scope
- no AI in text creation but AI allowed outside scope
- educational strict mode
- prize or competition mode

These claims are represented by profiles such as `P1` through `P5`.

### 2. Assurance Layer
This layer defines how strong the supporting evidence and controls are.

Assurance levels run from `D0` to `D4`.

### 3. Evidence Layer
This layer contains concrete records such as:

- author declaration
- manifest
- version records
- session logs
- environment records
- audit reports

### 4. Verification Layer
This layer allows an issuer, auditor, or third party to review whether the evidence supports the claim.

### 5. Publication Layer
This layer makes the certification understandable and visible, for example through a public record, signed credential, or QR-linked status page.

## Typical Flow
1. a work is registered
2. scope and profile are chosen
3. the work is drafted under a workflow
4. evidence is collected
5. a manifest is issued
6. audit may be performed
7. a public claim is published

## Design Principle
OHAS separates:
- what is claimed
- how it is evidenced
- how it is reviewed
- how it is communicated
