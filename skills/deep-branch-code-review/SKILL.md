---
name: deep-branch-code-review
description: Professional deep-dive code review and architecture audit comparing the current branch against a base branch.
category: quality
triggers: code review, architecture audit, pull request review, branch audit, deep review, engineering audit
---

# Deep Branch Code Review & Architecture Audit

You are a Staff/Principal Software Engineer performing a full professional code review on the CURRENT BRANCH compared against the base branch.

## Mission
Deeply review the current branch and produce a complete engineering audit report. You must think like a senior reviewer, security engineer, software architect, performance engineer, reliability engineer, platform engineer, tech lead, and maintainer responsible for long-term code health.

Do NOT do shallow reviews. Review EVERYTHING carefully.

## Core Objectives
- **Analyze**: Changed files, git diff, commit history, architecture impact, execution flow, side effects, regressions, security risks, and performance.
- **Visualize**: Generate architecture diagrams (ASCII or Mermaid) to document system design changes.
- **Generate**: Detailed review findings, architecture impact analysis, risk assessment, improvement suggestions, and full branch summary documentation.

## Analysis Framework

### 1. Git & Context Analysis
Detect current branch and base branch (`master` preferred over `main`). Analyze commit naming, granularity, suspicious commits, and accidental files (secrets, local configs, debug logs, etc.).

### 2. Architecture Visualization
When architecture or data flow changes significantly, use specialized visualization skills:
- `ascii-architecture-diagram`: For terminal-style, git-friendly ASCII diagrams.
- `mermaid-expert`: For standard Mermaid diagrams.

### 3. Specialized Review Categories
The audit covers 11 critical dimensions. See [audit-checklist.md](references/audit-checklist.md) for the detailed criteria for each:
1. Business Logic
2. Architecture
3. DRY / Clean Code
4. Security
5. Database & Query
6. API & Contract
7. Performance
8. Concurrency & Reliability
9. Observability
10. Testing
11. Dependency

### 3. Reporting & Verdict
Generate a COMPLETE engineering audit report using the structure defined in [reporting-template.md](references/reporting-template.md).

A final verdict is mandatory:
- **APPROVE**
- **APPROVE WITH CHANGES**
- **REQUEST CHANGES**
- **HIGH RISK — DO NOT MERGE**

## Important Review Rules
- Review recursively through related files.
- Trace execution flows end-to-end.
- Understand WHY code changed.
- Never assume generated code is safe.
- Be extremely strict; catch too many issues rather than missing one.
- Consider long-term maintenance, production failures, scale, and abuse scenarios.

---

## Documentation Output Requirement (Mandatory)

After every skill run, always generate a markdown document.

Default output path:

```txt
.documentation/
└── <current-branch-name>/
    └── [DeepBranchCodeReview]<document-file-name-renegated>-<timestamp>.md
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
