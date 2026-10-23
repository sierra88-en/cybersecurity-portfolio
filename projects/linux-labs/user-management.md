# Lab: Linux User and Group Management

- **Date:** [YYYY-MM-DD]
- **Distribution/version:** [Distribution and release]
- **Environment:** [Disposable VM/container]
- **Objective:** Practice account lifecycle, group membership, and access review.

## Safety notes

Perform only in a disposable lab with console recovery. Never change or delete production accounts based on this template. Do not publish real usernames or account databases.

## Procedure

```bash
# Inspect the current identity and groups
id
getent group <lab-group>

# Example lifecycle commands — review before use; privileged actions are commented
# sudo useradd --create-home <lab-user>
# sudo usermod --append --groups <lab-group> <lab-user>
# id <lab-user>
# sudo userdel --remove <lab-user>   # only for a disposable lab account
```

## Results

- **Expected:** [Expected account/group state]
- **Observed:** [Sanitized result]
- **Access review:** [Explain how least privilege was assessed]

```text
[Sanitized command output]
```

## Screenshots

![Sanitized user-management result](../../assets/screenshots/REPLACE-WITH-SANITIZED-IMAGE.png)

## Lessons learned and cleanup

[Account lifecycle considerations, verification, and cleanup confirmation.]
