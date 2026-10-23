# Security Assessment Report: [System or Lab Name]

> **Classification:** Public portfolio copy — sanitized  
> **Assessment date:** [YYYY-MM-DD]  
> **Author:** [Name / handle]  
> **Status:** [Draft | Reviewed | Complete]

## Executive summary

[Explain the objective, overall posture, principal risks, and most important recommended actions in concise, non-sensitive language.]

## Authorization and scope

- **Authorization reference:** [Description or redacted reference]
- **In-scope assets:** [Lab assets or approved systems; sanitize identifying details]
- **Out of scope:** [Explicit exclusions]
- **Assessment window:** [Start/end, timezone]
- **Constraints:** [Rate limits, prohibited techniques, availability constraints]

## Environment and methodology

- **Environment:** [OS, architecture, deployment type]
- **Tools and versions:** [Tool — version]
- **Methodology:** [Standards or process used]
- **Data handling:** [Synthetic/anonymized; retention and cleanup]

## Results overview

| Severity | Count | Summary |
|---|---:|---|
| Critical | [0] | [Summary] |
| High | [0] | [Summary] |
| Medium | [0] | [Summary] |
| Low / Informational | [0] | [Summary] |

## Findings

### [FINDING-001] [Clear, concise title]

- **Severity:** [Critical / High / Medium / Low / Informational]
- **Affected component:** [Sanitized identifier]
- **Status:** [Open / Accepted / Fixed / Retest pending]
- **Confidence:** [High / Medium / Low]

**Observation**  
[What was observed and how it was validated. Avoid publishing sensitive values.]

**Impact**  
[Realistic business or technical consequence.]

**Evidence**  
[Minimal sanitized evidence. Redact tokens, personal data, internal addresses, and identifying metadata.]

```text
[Paste safe, minimal evidence here. Do not include credentials or raw sensitive output.]
```

**Remediation**  
[Specific, prioritized corrective action and secure configuration guidance.]

**Validation**  
[How to confirm the fix in an authorized environment.]

**References**  
- [Vendor advisory / standard / documentation]

## Screenshots and lab results

<!-- Insert only sanitized images. Confirm no secrets, usernames, hostnames, or private data are visible. -->

![Sanitized assessment evidence](../../assets/screenshots/REPLACE-WITH-SANITIZED-IMAGE.png)

## Limitations

[Time, access, test coverage, and other limitations; state what was not tested.]

## Remediation plan

| Finding | Action | Owner | Target date | Verification |
|---|---|---|---|---|
| [FINDING-001] | [Action] | [Role] | [Date] | [Retest method] |

## Cleanup and lessons learned

[Describe cleanup performed, residual risk, and process improvements.]

## Appendix: safe reproduction notes

[Only provide reproducible steps for an isolated lab or authorized target. Include environment setup and teardown; omit secrets and sensitive payloads.]
