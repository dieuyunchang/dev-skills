# Engineering Audit Report: [Branch Name]

## 1. Executive Summary
- **Context**: What does this branch do and why?
- **High-Level Impact**: Summary of the changes and their significance.

## 2. Technical Summary
- **Major Changes**: Key modifications to the codebase.
- **Architecture & Flow**: Impact on system design and data flow.
- **Architecture Visualization**:
  > [!TIP]
  > Use the `ascii-architecture-diagram` or `mermaid-expert` skills to visualize the new architecture or flow changes.
  
  [Insert ASCII or Mermaid diagram here]

## 3. Files & Components Affected
| Component | Impacted Files | Description of Impact |
|-----------|----------------|-----------------------|
| Models    | ...            | ...                   |
| Services  | ...            | ...                   |
| APIs      | ...            | ...                   |
| ...       | ...            | ...                   |

## 4. Risk Assessment
- **Critical/High Risks**: Immediate threats to production, security, or data.
- **Medium/Low Risks**: Potential technical debt or minor regressions.
- **Rollback/Deployment Risks**: Considerations for the release process.

## 5. Behavior Changes
- **Before vs After**: Functional changes from the user/system perspective.
- **API/Contract Changes**: Impact on external consumers.

## 6. Performance & Scalability
- **Query/Memory Impact**: Specific findings related to efficiency.
- **Bottlenecks**: Potential issues under load.

## 7. Suggested Improvements
- **Refactors**: Ideas for cleaner code and abstractions.
- **Optimizations**: Specific logic or query improvements.

## 8. Deployment Considerations
- **Migrations**: Ordering and downtime risks.
- **Feature Flags**: Recommendations for safe rollout.
- **Compatibility**: Ensuring backward compatibility.

## 9. Final Verdict
- **Overall Code Quality Score**: 0-100
- **Maintainability Score**: 0-100
- **Security Score**: 0-100
- **Scalability Score**: 0-100
- **Production Readiness**: [READY / NOT READY]

### Verdict: [APPROVE / APPROVE WITH CHANGES / REQUEST CHANGES / HIGH RISK — DO NOT MERGE]

**Rationale**: [Detailed explanation for the verdict]
