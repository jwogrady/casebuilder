# ADR 0001: Product boundaries

## Status

Accepted

## Context

CaseBuilder sits between source capture, legal understanding, and filing generation. Without explicit boundaries, the project can collapse into a single vague tool that collects, analyzes, and drafts without verifiable contracts.

## Decision

CaseBuilder is organized around four stages:

1. Capture
2. Build
3. Review
4. Generate

Each stage has clear artifacts and responsibilities.

## Consequences

- Capture preserves source material and provenance.
- Build produces the Canonical Case Record.
- Review produces human-reviewable understanding.
- Generate produces work product from approved understanding.

No stage may silently bypass the human review gate.
