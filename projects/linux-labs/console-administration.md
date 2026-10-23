# Lab: Linux Console Administration and Baseline Hardening

- **Date:** [YYYY-MM-DD]
- **Distribution/version:** [Distribution and release]
- **Environment:** [Isolated VM; snapshot available]
- **Objective:** Inspect services, updates, logs, and basic host security posture.

## Checks performed

```bash
# Read-only inspection examples
uname -a
systemctl --failed
ss -tulpen
journalctl --since "24 hours ago" --no-pager | tail -n 100
```

[Document package update status, service exposure, log review, time synchronization, firewall posture, and SSH configuration review as relevant. Redact sensitive output.]

## Changes made

| Change | Rationale | Risk / rollback | Verification |
|---|---|---|---|
| [Change] | [Why] | [Rollback] | [How verified] |

## Results

- **Baseline:** [Summary]
- **Changes:** [Summary]
- **Verification:** [Commands and expected outcome]

```text
[Sanitized output only]
```

## Screenshots

![Sanitized console lab result](../../assets/screenshots/REPLACE-WITH-SANITIZED-IMAGE.png)

## Lessons learned and cleanup

[Document service impact, reboot/recovery considerations, and lab reset.]
