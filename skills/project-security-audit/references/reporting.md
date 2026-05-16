# Security Audit Reporting

Format for documenting identified risks.

## Issue Structure
For every issue identified, provide:

### [Severity] - [Issue Title]
- **File**: Exact file path (e.g., `src/utils/telemetry.js`)
- **Code**: Relevant code snippet
- **Why Dangerous**: Clear explanation of the threat.
- **Exploitation Risk**: What an attacker gains if this is executed.
- **Recommendation**: How to fix or isolate the risk safely.

## Severity Definitions
- **Critical**: Remote Code Execution (RCE), Active Credential Theft, or confirmed Malware.
- **High**: Exfiltration logic, Dangerous Shell scripts, or suspicious obfuscation.
- **Medium**: Telemetry with high risk of secret leakage, non-privileged system modifications.
- **Low**: Best practice violations, suspicious but unconfirmed patterns.

## Final Security Verdict
At the conclusion of the audit, provide the following table and summary:

| Metric | Score / Status |
|--------|----------------|
| **Overall Risk Score** | 0-100 (Higher is riskier) |
| **Safe to Run?** | YES / NO / CAUTION |
| **Safe to Install Deps?** | YES / NO / CAUTION |
| **Safe to Use API Keys?** | YES / NO |
| **Safe to Run Docker?** | YES / NO |
| **Sandbox Recommended?** | YES / NO |

### Recommended Next Actions
1. [Action 1]
2. [Action 2]
...
