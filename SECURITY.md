# Security and privacy checklist

Before every commit or upload, verify all of the following:

- [ ] No passwords, API keys, access tokens, private keys, cookies, or connection strings are present.
- [ ] No real names, email addresses, IP addresses, hostnames, customer records, or other identifying data are disclosed without explicit permission.
- [ ] Screenshots are cropped and checked for browser tabs, usernames, terminal history, metadata, and secrets.
- [ ] Logs, packet captures, database exports, and incident evidence are synthetic or safely sanitized; raw evidence is never committed.
- [ ] Targets and test activities were explicitly authorized; no third-party systems are tested without written scope.
- [ ] Findings avoid unnecessary weaponizable detail and include mitigations and validation guidance.
- [ ] The repository history has been checked; deleting a secret from the latest file does not remove it from Git history.

If a secret is exposed, revoke or rotate it immediately. Do not rely on `.gitignore` to protect a file that was already tracked. For an accidental public disclosure, follow the provider's incident process and remove the data from repository history as appropriate.

**This repository is public-facing portfolio material. Treat all committed content as permanently public.**
