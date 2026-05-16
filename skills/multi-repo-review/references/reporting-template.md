# [Feature Name] — Multi-Repository System Review

**Generated at:** <timestamp>
**Review Mode:** FULL MULTI-REPOSITORY SYSTEM REVIEW

---

## 1. Executive Summary
- **Feature Purpose:** [Brief description]
- **Repositories Involved:**
  - [Repo Name] ([Branch])
- **Overall Impact:** [High-level summary]
- **High-Level Risks:** [Critical items to note]
- **Deployment Complexity:** [Low/Medium/High]

---

## 2. Repository Overview
[Repeat for each repository]
### [Repository Name]
- **Purpose:** [Service responsibility]
- **Architecture Style:** [e.g., Clean Architecture, Hexagonal, Monolithic]
- **Branch/Base:** `[Branch]` vs `[Base Branch]`
- **Changes:** [Number] files changed.
- **Key Components:** [List affected services, models, controllers, etc.]

---

## 3. Feature Flow Analysis
### End-to-End Flow
[Describe how the request/data moves through the system]

### Diagrams
```mermaid
[Insert Sequence, Architecture, or Data Flow Diagram]
```

---

## 4. Detailed Change Analysis
[Grouped by repository]

### [Repository Name]
- **Models/Migrations:** [Impact] (Tests: [Yes/No/Missing])
- **Services/Logic:** [Impact] (Tests: [Yes/No/Missing])
- **APIs/Contracts:** [Impact] (Tests: [Yes/No/Missing])
- **Workers/Jobs:** [Impact] (Tests: [Yes/No/Missing])

---

## 5. Cross-Repository Impact Analysis
- **Integration Points:** [Where services talk]
- **Shared Contracts:** [API/Event schemas shared]
- **Deployment Dependencies:** [e.g., Service A must deploy before Service B]
- **Compatibility Risks:** [Rollback or version mismatch issues]

---

## 6. Security Review
| Severity | File | Issue | Exploit Scenario | Remediation |
| :--- | :--- | :--- | :--- | :--- |
| [Level] | [Path] | [Description] | [How it could be abused] | [Fix] |

---

## 7. Performance & Scalability
- **Query Impact:** [N+1, missing indexes, etc.]
- **Sync Bottlenecks:** [Slow external calls, etc.]
- **Scalability Risks:** [Fan-out, queue overload, etc.]

---

## 8. Reliability & Distributed Systems
- **Failure Scenarios:** [What happens when Service X is down?]
- **Retry & Idempotency:** [Safety of background jobs]
- **Rollback Safety:** [DB/Code compatibility during rollback]
- **Eventual Consistency:** [Data lag concerns]

---

## 9. Code Quality & Maintainability
- **Abstraction Quality:** [Leaky abstractions, etc.]
- **DRY Violations:** [Duplicated logic across repos]
- **Naming & Readability:** [Concerns]

---

## 10. Suggested Improvements
- [Refactor suggestion]
- [Architecture improvement]
- [Observability addition]

---

## 11. Deployment Strategy
1. [Step 1: e.g., Run migration]
2. [Step 2: Deploy Service A]
3. [Step 3: Deploy Service B]
**Rollback Plan:** [Specific considerations]

---

## 12. Final Verdict

### Scores (0-100)
- **Code Quality:** [Score]
- **Architecture:** [Score]
- **Security:** [Score]
- **Reliability:** [Score]
- **Scalability:** [Score]
- **Maintainability:** [Score]
- **Testing & Coverage:** [Score]
- **Production Readiness:** [Score]

### Conclusion
**[APPROVE / APPROVE WITH CHANGES / REQUEST CHANGES / HIGH RISK — DO NOT MERGE]**

**Reasoning:** [Brief justification for the verdict]

---

### Final Metadata
**Reviewed repositories:**
- [Repo Name] -> [Branch] (vs [Base])
