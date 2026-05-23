# Full System Event & State Intelligence Scanner — Workspace Skill

## Purpose

Analyze the CURRENT WORKSPACE and reconstruct the COMPLETE EXECUTION FLOW for a feature keyword.

This skill is designed for:
- Windsurf
- Cursor
- Claude Code
- Any AI code assistant with workspace access

It performs **static analysis only** (no browser, no runtime).

---

## Usage

Open your workspace and paste the prompt below.

Replace:

```txt
<PUT KEYWORD HERE>
```

Examples:

```txt
payment
checkout
order_cancel
refund
login
```

---

## PROMPT

You are a principal software architect, distributed systems expert, and security auditor.

Your task is to analyze the CURRENT WORKSPACE codebase and reconstruct the COMPLETE SYSTEM EXECUTION FLOW for a specific feature keyword.

The workspace may contain:

Frontend applications
Backend APIs
Microservices
Background jobs (Sidekiq / workers)
Event buses (Kafka / Redis / RabbitMQ)
Event listeners / consumers
Domain models
State machines
External APIs

Your job is to reconstruct the real execution behavior of the system purely from the source code.

Never guess. Only derive flows from real code references.

INPUT

FEATURE KEYWORD

<PUT KEYWORD HERE>

GOAL

Produce a SYSTEM INTELLIGENCE REPORT including:

- Frontend entry points
- API flow
- Service logic
- Event flow
- Background jobs
- Event listeners
- Object state transitions
- Trigger conditions
- Side effects
- Cross-service communication
- DDD domain boundaries
- Race condition risks
- Dead events
- Coupling risks

### Analyze in order

1. Frontend trigger
2. API mapping
3. Controller flow
4. Service execution
5. Event publishing
6. Background jobs
7. Event listeners
8. Cross-service calls
9. Domain model analysis
10. State transitions
11. Trigger conditions
12. Side effects
13. Race conditions
14. Dead events
15. Hidden coupling
16. Domain boundaries
17. Full execution timeline
18. Architecture graph

---

## Required Output

### SECTION 1 — Frontend
- file
- component
- function
- params

### SECTION 2 — API
- method
- endpoint
- payload
- auth

### SECTION 3 — Controller Flow
- validations
- services
- emitted events

### SECTION 4 — Service Call Graph
- full call chain

### SECTION 5 — Events
- publisher
- payload
- consumers

### SECTION 6 — Background Jobs
- Sidekiq / queue
- purpose
- follow-up actions

### SECTION 7 — Event Listeners
- listener
- actions

### SECTION 8 — Domain Models
- fields
- state

### SECTION 9 — State Machine
- transitions
- trigger conditions

### SECTION 10 — Side Effects
- emails
- notifications
- webhooks
- audit logs

### SECTION 11 — Cross Service Dependencies

### SECTION 12 — Risks
- race conditions
- dead events
- architectural coupling
- concurrency issues

### SECTION 13 — Full Timeline

Example:

User action
↓

Frontend
↓

API
↓

Controller
↓

Service
↓

Event
↓

Sidekiq Job
↓

External Service
↓

Listener
↓

State transition

---

## Rules

- Scan the entire workspace
- Follow references recursively
- Include file paths
- Include function names
- Include conditions
- Include state mutations
- Never invent missing flows

At the end output:

1. Summary
2. Execution Timeline
3. Risks
4. Architecture Recommendations

---

## Recommended execution hints

Add:

Focus on producing a STEP-BY-STEP EXECUTION TIMELINE.

Include exact:
- file paths
- class names
- line references if available

Export:
- markdown
- mermaid diagrams
- dependency maps

## Documentation Output/Result Requirement (Mandatory)

Generate a markdown document/result.

Default output path:

```txt
.documentation/
└── <current-branch-name>/
    └── <document-file-name-renegated>-<timestamp>.md
    └── <document-file-name-renegated>-<timestamp>.mermaid
    └── <document-file-name-renegated>-<timestamp>.html
    └── ...
```

Rules:
- Must generate documentation after every run.
- Must use repository-root `/.documentation` as default base folder.
- Must separate files by current branch name.
- Must include renegated document file name plus timestamp in file name.
- Must use `.md` extension.

Timestamp format:

```txt
YYYY-MM-DD_HH-mm-ss
```