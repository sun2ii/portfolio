# 90-Day AI Discovery & Architecture Process

## Phase 0 — Kickoff (Week 0)

**Goal:** Align scope and secure system access

**Outputs:**
- Scope confirmation for onboarding, pricing, contractor workflows, and knowledge integration
- Stakeholder list (owner, estimator, field ops, office admin)
- Access to pricing sheets, vendor catalogs, compliance docs, and existing workflows
- Engagement schedule + communication rhythm

```mermaid
flowchart LR
    Start[Phase 0 — Kickoff<br/>Week 0]:::primary
    Goal[Goal: Align scope and secure system access]:::goal

    Start --> Goal
    Goal --> S1[Scope Confirmation]:::primary
    Goal --> S2[Stakeholder List]:::important
    Goal --> S3[System Access]:::important
    Goal --> S4[Engagement Schedule]:::primary

    S1 --> S1A[Onboarding workflow]:::detail
    S1 --> S1B[Pricing logic]:::detail
    S1 --> S1C[Contractor workflows]:::detail
    S1 --> S1D[Knowledge integration]:::detail

    S2 --> S2A[Owner]:::detail
    S2 --> S2B[Estimator]:::detail
    S2 --> S2C[Field ops]:::detail
    S2 --> S2D[Office admin]:::detail

    S3 --> S3A[Pricing sheets]:::detail
    S3 --> S3B[Vendor catalogs]:::detail
    S3 --> S3C[Compliance docs]:::detail
    S3 --> S3D[Existing workflows]:::detail

    S4 --> S4A[Meeting cadence]:::detail
    S4 --> S4B[Communication channels]:::detail
    S4 --> S4C[Week-by-week plan]:::detail

    classDef primary fill:#4A90E2,stroke:#357ABD,stroke-width:2px,color:#fff
    classDef important fill:#50E3C2,stroke:#3BBFA3,stroke-width:2px,color:#000
    classDef goal fill:#2ECC71,stroke:#27AE60,stroke-width:3px,color:#000,font-weight:bold
    classDef secondary fill:#7F8C8D,stroke:#5D6D7E,stroke-width:2px,color:#fff
    classDef detail fill:#D1D8E0,stroke:#AAB7C4,stroke-width:1px,color:#000
```

---

## Phase 1 — Current-State Discovery (Weeks 1–4)

**Goal:** Understand how the fencing business actually operates end-to-end

### Stakeholder Interviews
- **Owner** — strategic workflow
- **Office staff** — quoting + admin
- **Estimators** — field operations
- **Install crew lead** — job flow + material usage

### Workflow Mapping
Customer intake → qualification → pricing → quote → approval → job scheduling → material ordering → installation → payment

### Analysis
- Pricing worksheets
- Vendor lists
- Historical invoices
- Conversation transcripts

### Manual-Work Discovery
- Quote creation steps
- Material estimation
- Commission calculation
- Data entry + hand-offs

### Tool & System Inventory
- Pricing spreadsheets
- Job folders
- Messaging tools
- Website forms
- CRM (if any)

### Deliverables
- **Current-state workflow diagrams** — intake, pricing, job costing, contractor workflow
- **Pain-point summary**
- **System + document inventory** — pricing sheets, catalogs, compliance PDFs, conversation logs

```mermaid
flowchart LR
    Start[Phase 1 — Current-State Discovery<br/>Weeks 1-4]:::primary
    Goal[Goal: Understand how the fencing business<br/>actually operates end-to-end]:::goal

    Start --> Goal
    Goal --> S1[Stakeholder Interviews]:::primary
    Goal --> S2[Workflow Mapping]:::important
    Goal --> S3[Manual-Work Discovery]:::important
    Goal --> S4[Tool & System Inventory]:::primary

    S1 --> S1A[Owner - strategic workflow]:::detail
    S1 --> S1B[Office staff - quoting + admin]:::detail
    S1 --> S1C[Estimators - field operations]:::detail
    S1 --> S1D[Install crew lead - material usage]:::detail

    S2 --> S2A[Customer intake → qualification]:::detail
    S2 --> S2B[Pricing → quote → approval]:::detail
    S2 --> S2C[Job scheduling → material ordering]:::detail
    S2 --> S2D[Installation → payment]:::detail

    S3 --> S3A[Quote creation steps]:::detail
    S3 --> S3B[Material estimation]:::detail
    S3 --> S3C[Commission calculation]:::detail
    S3 --> S3D[Data entry + hand-offs]:::detail

    S4 --> S4A[Pricing spreadsheets]:::detail
    S4 --> S4B[Job folders + messaging tools]:::detail
    S4 --> S4C[Website forms + CRM]:::detail

    S1 -.-> D1[Deliverable:<br/>Current-state workflow diagrams]:::secondary
    S2 -.-> D1
    S3 -.-> D2[Deliverable:<br/>Pain-point summary]:::secondary
    S4 -.-> D3[Deliverable:<br/>System + document inventory]:::secondary

    classDef primary fill:#4A90E2,stroke:#357ABD,stroke-width:2px,color:#fff
    classDef important fill:#50E3C2,stroke:#3BBFA3,stroke-width:2px,color:#000
    classDef goal fill:#2ECC71,stroke:#27AE60,stroke-width:3px,color:#000,font-weight:bold
    classDef secondary fill:#7F8C8D,stroke:#5D6D7E,stroke-width:2px,color:#fff
    classDef detail fill:#D1D8E0,stroke:#AAB7C4,stroke-width:1px,color:#000
```

---

## Phase 2 — Architecture Mapping (Weeks 4–8)

**Goal:** Convert MyFencer's real operations into a scalable technical architecture

### Audit & Reverse-Engineer
- Audit all pricing sheets, cost tables, and vendor documents
- Reverse-engineer existing quoting logic into a clean rules engine structure
- Identify inconsistencies in material descriptions, SKUs, and vendor pricing

### Data Flow Mapping
**Current flow:**
website → DMs → manual quoting → spreadsheet → approval → field ops

### Bottleneck Identification
- Manual classification
- Pricing inconsistencies
- Missing data structure

### Data Model Design
Unified models for:
- Materials
- Pricing rules
- Job costing
- Customer attributes
- Contractor workflows

### Deliverables
- **Current-state architecture diagram**
- **Entity-relationship model** — materials, pricing, job costing, conversations
- **Data lineage & integration map** — how data moves through the business today

```mermaid
flowchart LR
    Start[Phase 2 — Architecture Mapping<br/>Weeks 4-8]:::primary
    Goal[Goal: Convert MyFencer's real operations<br/>into a scalable technical architecture]:::goal

    Start --> Goal
    Goal --> S1[Audit & Reverse-Engineer]:::primary
    Goal --> S2[Identify Issues & Bottlenecks]:::important
    Goal --> S3[Design Unified Data Models]:::important

    S1 --> S1A[Audit pricing sheets + cost tables]:::detail
    S1 --> S1B[Reverse-engineer quoting logic]:::detail
    S1 --> S1C[Analyze vendor documents]:::detail

    S2 --> S2A[Material description inconsistencies]:::detail
    S2 --> S2B[Map current data flow:<br/>website → DMs → spreadsheet → field ops]:::detail
    S2 --> S2C[Identify manual classification bottlenecks]:::detail
    S2 --> S2D[Find pricing inconsistencies]:::detail

    S3 --> S3A[Materials model]:::detail
    S3 --> S3B[Pricing rules model]:::detail
    S3 --> S3C[Job costing model]:::detail
    S3 --> S3D[Customer attributes model]:::detail
    S3 --> S3E[Contractor workflows model]:::detail

    S1 -.-> D1[Deliverable:<br/>Current-state architecture diagram]:::secondary
    S2 -.-> D1
    S3 -.-> D2[Deliverable:<br/>Entity-relationship model]:::secondary
    S2 -.-> D3[Deliverable:<br/>Data lineage + integration map]:::secondary

    classDef primary fill:#4A90E2,stroke:#357ABD,stroke-width:2px,color:#fff
    classDef important fill:#50E3C2,stroke:#3BBFA3,stroke-width:2px,color:#000
    classDef goal fill:#2ECC71,stroke:#27AE60,stroke-width:3px,color:#000,font-weight:bold
    classDef secondary fill:#7F8C8D,stroke:#5D6D7E,stroke-width:2px,color:#fff
    classDef detail fill:#D1D8E0,stroke:#AAB7C4,stroke-width:1px,color:#000
```

---

## Phase 3 — AI Feasibility & Solution Design (Weeks 8–10)

**Goal:** Determine where AI can reliably automate and enhance MyFencer operations

### RAG Feasibility Evaluation
Knowledge base components:
- Materials
- Pricing sheets
- Compliance docs
- Historical conversations

### Rules vs. LLM Logic
- **Pricing** = rules-based
- **Classification** = LLM-based
- **Material lookup** = hybrid approach

### AI Architecture Design
Core capabilities:
- User-type detection
- Intake + classification
- Quoting guidance
- Contractor/DIY suggestion paths

### Embedding Strategy
Build embeddings across pricing tables and material catalogs

### Feasibility Stress-Testing
Validate across:
- Accuracy
- Cost
- Reliability
- Scalability
- Auditability

### Deliverables
- **AI opportunity map** — intake, pricing validation, job costing, material lookup, contractor workflows
- **Future-state architecture diagram**
- **Proposed data model redesign** — materials, pricing, jobs, user types

```mermaid
flowchart LR
    Start[Phase 3 — AI Feasibility & Solution Design<br/>Weeks 8-10]:::primary
    Goal[Goal: Determine where AI can reliably<br/>automate and enhance MyFencer operations]:::goal

    Start --> Goal
    Goal --> S1[Evaluate RAG Feasibility]:::primary
    Goal --> S2[Define Rules vs. LLM Logic]:::important
    Goal --> S3[Design AI Architecture]:::important
    Goal --> S4[Stress-Test Feasibility]:::primary

    S1 --> S1A[Materials knowledge base]:::detail
    S1 --> S1B[Pricing sheets]:::detail
    S1 --> S1C[Compliance docs]:::detail
    S1 --> S1D[Historical conversations]:::detail
    S1 --> S1E[Build embedding strategy]:::detail

    S2 --> S2A[Pricing = rules-based]:::detail
    S2 --> S2B[Classification = LLM-based]:::detail
    S2 --> S2C[Material lookup = hybrid]:::detail

    S3 --> S3A[User-type detection]:::detail
    S3 --> S3B[Intake + classification]:::detail
    S3 --> S3C[Quoting guidance]:::detail
    S3 --> S3D[Contractor/DIY suggestion paths]:::detail

    S4 --> S4A[Accuracy validation]:::detail
    S4 --> S4B[Cost analysis]:::detail
    S4 --> S4C[Reliability + scalability]:::detail
    S4 --> S4D[Auditability requirements]:::detail

    S1 -.-> D1[Deliverable:<br/>AI opportunity map]:::secondary
    S3 -.-> D1
    S2 -.-> D2[Deliverable:<br/>Future-state architecture diagram]:::secondary
    S3 -.-> D2
    S1 -.-> D3[Deliverable:<br/>Proposed data model redesign]:::secondary
    S2 -.-> D3

    classDef primary fill:#4A90E2,stroke:#357ABD,stroke-width:2px,color:#fff
    classDef important fill:#50E3C2,stroke:#3BBFA3,stroke-width:2px,color:#000
    classDef goal fill:#2ECC71,stroke:#27AE60,stroke-width:3px,color:#000,font-weight:bold
    classDef secondary fill:#7F8C8D,stroke:#5D6D7E,stroke-width:2px,color:#fff
    classDef detail fill:#D1D8E0,stroke:#AAB7C4,stroke-width:1px,color:#000
```

---

## Phase 4 — Executive Recommendations (Weeks 10–12)

**Goal:** Present a clear roadmap for turning MyFencer into a scalable AI-powered operations system

### Consolidate Findings
Create founder-facing packet with:
- Cost/benefit analysis
- Risk mitigation plan
- Build now vs. later priorities

### Present Future-State
- Architecture redesign
- Workflow optimization
- Executive presentation

### Implementation Roadmap
**3-Phase approach:**
1. **Phase 1** — Knowledge system + onboarding logic
2. **Phase 2** — Pricing engine + job-costing automation
3. **Phase 3** — Full contractor back-office platform + analytics

### Deliverables
- **90-day summary report**
- **Implementation roadmap**
- **Executive-style architecture presentation**

```mermaid
flowchart LR
    Start[Phase 4 — Executive Recommendations<br/>Weeks 10-12]:::primary
    Goal[Goal: Present a clear roadmap for turning MyFencer<br/>into a scalable AI-powered operations system]:::goal

    Start --> Goal
    Goal --> S1[Consolidate Findings]:::primary
    Goal --> S2[Present Future-State]:::important
    Goal --> S3[Create Implementation Roadmap]:::important
    Goal --> S4[Alignment Session]:::primary

    S1 --> S1A[Founder-facing packet]:::detail
    S1 --> S1B[Cost/benefit analysis]:::detail
    S1 --> S1C[Risk mitigation plan]:::detail

    S2 --> S2A[Future-state architecture]:::detail
    S2 --> S2B[Workflow redesign]:::detail
    S2 --> S2C[Executive presentation]:::detail

    S3 --> S3A[Phase 1:<br/>Knowledge system + onboarding logic]:::detail
    S3 --> S3B[Phase 2:<br/>Pricing engine + job-costing automation]:::detail
    S3 --> S3C[Phase 3:<br/>Full contractor back-office platform + analytics]:::detail

    S4 --> S4A[Build now vs. later priorities]:::detail
    S4 --> S4B[Resource requirements]:::detail
    S4 --> S4C[Timeline validation]:::detail

    S1 -.-> D1[Deliverable:<br/>90-day summary report]:::secondary
    S3 -.-> D2[Deliverable:<br/>Implementation roadmap]:::secondary
    S2 -.-> D3[Deliverable:<br/>Executive presentation]:::secondary

    classDef primary fill:#4A90E2,stroke:#357ABD,stroke-width:2px,color:#fff
    classDef important fill:#50E3C2,stroke:#3BBFA3,stroke-width:2px,color:#000
    classDef goal fill:#2ECC71,stroke:#27AE60,stroke-width:3px,color:#000,font-weight:bold
    classDef secondary fill:#7F8C8D,stroke:#5D6D7E,stroke-width:2px,color:#fff
    classDef detail fill:#D1D8E0,stroke:#AAB7C4,stroke-width:1px,color:#000
```

---

## Outcome

**By Day 90, MyFencer achieved:**

- A complete map of all operational workflows
- A unified knowledge schema and data model for pricing, materials, and jobs
- A future-state AI architecture for intake → pricing → job costing
- A clear implementation plan that guided the actual build

This process became the backbone for the MyFencer production system now running in real-world contractor operations.

---

## About MyFencer

**MyFencer** is an AI-driven knowledge and workflow automation system built for fencing contractors.

The platform combines structured business logic, clean data models, and AI-powered reasoning to streamline the entire lifecycle of a fencing project — from initial customer intake to job costing.

### Core Components
- Materials catalog
- Pricing sheets
- Vendor catalogs
- Compliance documents
- Historical conversations
- Approval workflows
- Job costs + margins

### Technology Approach
Centralized knowledge system using:
- Embeddings
- RAG (retrieval-augmented generation)
- Structured rules logic
