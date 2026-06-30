# Architecture

## Architectural thesis

CaseBuilder is organized around contracts, not implementation details.

The system has four major stages:

```text
Capture -> Build -> Review -> Generate
```

Each stage produces artifacts consumed by the next stage. Every stage is repeatable. Every output must preserve provenance.

## Layers

### Capture layer

Owned by Rake.

Produces the Capture Bundle: immutable source material, court metadata, files, hashes, and provenance.

### Build layer

Consumes the Capture Bundle.

Produces the Canonical Case Record and equivalent projections for humans and machines.

### Review layer

Consumes the Canonical Case Record.

Produces review packets, issue maps, timelines, contradictions, exhibit maps, and strategy artifacts.

### Generate layer

Consumes approved review artifacts.

Produces motions, discovery, declarations, exhibits, appendices, and filing packets.

## Core artifacts

| Artifact | Owner | Purpose |
|---|---|---|
| Capture Bundle | Capture | Immutable source material and provenance |
| Canonical Case Record | Build | Verified factual record derived from Capture |
| Review Packet | Review | Human-reviewable case understanding |
| Human Decision | Review | Approval, rejection, correction, or instruction |
| Filing Package | Generate | Work product ready for filing |

## Source of truth

The Capture Bundle is the authoritative input.

The Canonical Case Record is the verified derived record.

Filesystem and DuckDB outputs are projections. They must be reproducible and equivalent.

## Invariants

- No derived artifact mutates captured source material.
- No generation happens without approved understanding.
- Every claim traces to evidence.
- Every projection can be regenerated.
- Every stage records the artifact versions it consumed.
