# Contributing

CaseBuilder is currently in product-architecture formation.

The most valuable contributions are clear contracts, testable invariants, and implementation work that strengthens the Capture -> Build -> Review -> Generate loop.

## Principles

- Ground decisions in evidence and code.
- Treat documentation as an architectural contract, not marketing copy.
- Preserve provenance in every artifact.
- Prefer small, reversible changes.
- Do not collapse product stages without an explicit ADR.

## Review standard

A change should answer:

- Which product stage does this belong to?
- What artifact does it consume?
- What artifact does it produce?
- How is provenance preserved?
- How can the output be verified?
- What should happen if the stage fails?

## Branching

Use short-lived branches and pull requests.

Do not merge large architectural changes without an ADR.
