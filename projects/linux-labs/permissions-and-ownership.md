# Lab: Linux File Permissions and Ownership

- **Date:** [YYYY-MM-DD]
- **Distribution/version:** [e.g., Ubuntu 24.04 LTS]
- **Environment:** [Disposable VM/container; no production systems]
- **Objective:** Understand ownership, mode bits, least privilege, and verification.

## Concepts

[Explain user/group/other permissions, symbolic and octal notation, directory traversal, and why least privilege matters.]

## Procedure

Use a disposable lab. Review every command before execution; privileged commands can alter system access.

```bash
# Inspect identity and a lab file (replace placeholders)
id
ls -l -- ./sample.txt
stat -- ./sample.txt

# Example only: set owner/group and restrictive permissions on a lab file
# sudo chown <lab-user>:<lab-group> ./sample.txt
# chmod 640 ./sample.txt
```

## Verification and results

- **Expected:** [Describe intended owner and access]
- **Observed:** [Record sanitized output]
- **Verification command:** `stat -- ./sample.txt`

```text
[Paste sanitized output; do not include usernames or paths that identify a real system.]
```

## Screenshots

![Sanitized permissions lab result](../../assets/screenshots/REPLACE-WITH-SANITIZED-IMAGE.png)

## Lessons learned and cleanup

[What changed, what could go wrong, safe rollback, and cleanup performed.]
