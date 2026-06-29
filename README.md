# CaseBuilder

**Capture. Build. Review. Generate.**

CaseBuilder transforms a legal matter from disconnected documents into a complete, verified, and continually evolving case knowledge base.

It is not a legal research chatbot.
It is not a one-shot document generator.
It is not branded around AI.

CaseBuilder is a legal workflow system for collecting the record, building the case, reviewing understanding, and generating work product only after human approval.

> Capture reality once. Build understanding continuously. Generate work product only after understanding has been validated.

---

## The Problem

Every legal matter begins with scattered facts.

The record may be spread across:

- Court portals
- Filed PDFs
- Docket metadata
- Emails
- Discovery
- Exhibits
- Photos
- Contracts
- Case law
- Attorney notes
- Prior research

Some documents contain searchable text.
Many are scanned images.
Important facts are buried across hundreds or thousands of pages.

Before meaningful legal work can happen, someone must reconstruct the case.

That reconstruction is repetitive, expensive, difficult to verify, and repeated every time the case changes.

---

## The Solution

CaseBuilder creates a complete, structured, provenance-backed representation of a case.

Rather than treating filings as isolated documents, CaseBuilder treats them as part of a living case knowledge base.

The system captures source material, builds a verified case model, supports review and analysis, and generates filings only after the human agrees with the system's understanding of the case.

---

## Product Loop

CaseBuilder is not a linear pipeline.

It is a repeating workflow.

```text
Capture
  ↓
Build
  ↓
Review
  ↓
Generate
  ↓
File
  ↓
Capture
```

Every new filing becomes new source material.
Every stage can be revisited.
Every iteration improves the case.

---

## Workspaces

CaseBuilder is organized around four major workspaces.

Each workspace has its own internal loop.

```text
CaseBuilder
├── Capture
├── Build
├── Review
└── Generate
```

---

## Capture Workspace

Purpose: collect and preserve source material.

Capture is powered by Rake.

Responsibilities:

- Connect to court portals
- Collect filed documents
- Pull docket metadata
- Gather related content
- Link references
- Preserve provenance
- Produce the Capture Bundle

Capture does not analyze.
Capture preserves reality.

### Capture Loop

```text
Collect
  ↓
Link
  ↓
Validate
  ↓
Repeat
```

---

## Build Workspace

Purpose: transform the Capture Bundle into a verified case knowledge base.

Responsibilities:

- Explode filed PDFs
- Detect filing, document, and page boundaries
- Render every page image
- Extract searchable PDF text where available
- Add page-level transcription for scanned/image-only pages
- Preserve the provenance chain
- Compute quality and review metadata
- Build equivalent filesystem and database projections
- Seal and verify the case record

Build does not argue.
Build makes the case readable, traceable, and complete.

### Build Loop

```text
Explode
  ↓
Transcribe
  ↓
Verify
  ↓
Repeat
```

---

## Review Workspace

Purpose: develop and validate understanding of the case.

The Review workspace is where discovery, issue spotting, evidence organization, and strategy development happen.

Responsibilities:

- Timeline reconstruction
- Financial reconstruction
- Evidence mapping
- Filing chronology
- Contradiction detection
- Missing information discovery
- Authority organization
- Exhibit organization
- Strategy development
- Questions requiring human judgment

Review does not generate filings.
Review produces an evidence-backed understanding of the case.

### Review Loop

```text
Discover
  ↓
Analyze
  ↓
Question
  ↓
Refine
  ↓
Repeat
```

---

## Human Review Gate

The human does not merely review a generated filing.

The human reviews the system's understanding of the case before filing generation begins.

The human may:

- Approve the understanding
- Reject it
- Correct it
- Add context
- Request more evidence
- Request regeneration

Only after the human agrees that the case has been accurately understood does the system generate work product.

This is the core safety and quality principle of CaseBuilder.

---

## Generate Workspace

Purpose: turn approved understanding into legal work product.

Examples:

- Motions
- Responses
- Declarations
- Affidavits
- Discovery
- Appendices
- Exhibits
- E-filing packets

Generation never invents evidence.
Every factual statement must trace back to the verified case knowledge base.

### Generate Loop

```text
Draft
  ↓
Validate
  ↓
Review
  ↓
Repeat
```

---

## Case Knowledge Base

The output of CaseBuilder is not just a document folder.

It is a structured case knowledge base.

It contains:

- Court record
- Filings
- Documents
- Pages
- Page images
- Transcriptions
- Metadata
- Provenance
- References
- Authorities
- Exhibits
- Discovery
- Analysis
- Strategy
- Work product

Each domain can evolve while remaining tied to the underlying evidence.

---

## Canonical Case Record

At the foundation of the knowledge base is the Canonical Case Record.

The Record is a deterministic, verifiable representation of the factual record derived from the Capture Bundle.

It contains:

- Court metadata
- Filing hierarchy
- Document hierarchy
- Page hierarchy
- Page images
- Page transcriptions
- Provenance
- Quality metadata
- Relationships

The filesystem projection and database projection are equivalent renderings of the same Record.

Neither projection is the source of truth.
Both are reproducible from the Capture.

---

## Ecosystem Components

CaseBuilder pulls together capabilities that currently exist across several projects.

```text
Rake
  capture / collect / pull / link / actions

CaseForge
  explode / transcribe / canonical record / projections / verify

Lawnlord
  HOA case review / evidence analysis / timeline / strategy

Today
  filing generation / work product assembly
```

The dream state is a single comprehensive workflow:

```text
Capture the record
  ↓
Build the case
  ↓
Review the understanding
  ↓
Generate the filing
  ↓
File
  ↓
Capture the new record
```

---

## Design Principles

### Evidence First

Every conclusion must trace back to evidence.

### Provenance Always

Nothing enters the system without a source chain.

### Human Judgment

The system supports attorneys. It does not replace legal judgment.

### Review Before Generation

Work product is generated only after the human approves the system's understanding.

### Iterative by Design

Every stage loops. Every stage can improve. Every filing can become new source material.

### No Black Boxes

The system must be inspectable, reproducible, and verifiable.

---

## Product Philosophy

CaseBuilder is designed to eliminate repetitive reconstruction of the factual record so attorneys can focus on judgment, strategy, and advocacy.

The system does not ask attorneys to trust generated text.

It asks them to validate the case understanding before generating work product.

Understanding comes first.
Generation comes second.

---

## Long-Term Vision

CaseBuilder becomes the trusted legal workspace where every matter is continuously collected, organized, understood, reviewed, and improved.

Every filing strengthens the knowledge base.
Every review improves understanding.
Every decision remains traceable back to evidence.

The goal is not automated lawyering.

The goal is better lawyering.
