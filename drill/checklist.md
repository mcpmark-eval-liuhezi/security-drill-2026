# Hardening Checklist — Q4 2026 Tabletop Security Drill

This checklist is the primary drill artifact for the quarterly tabletop security drill.
The full change flow rehearsed during the drill: branch → pull request → squash merge to the default branch.

## 1. Access & Authentication

- [ ] Review and revoke stale OAuth app and PAT authorizations
- [ ] Enforce multi-factor authentication for all organization members
- [ ] Verify no dormant accounts retain repository access
- [ ] Confirm SSO / SCIM provisioning reflects the current org roster

## 2. Secrets & Scanning

- [ ] Confirm secret scanning is enabled (push protection on where available)
- [ ] Confirm Dependabot alerts are enabled
- [ ] Confirm code scanning / static analysis is enabled on the default branch
- [ ] Review and clear any open secret scanning alerts

## 3. Branch & Merge Protection

- [ ] Require pull request reviews before merging to the default branch
- [ ] Require status checks to pass before merging
- [ ] Require linear history / restrict force pushes to protected branches
- [ ] Restrict who can push directly to protected branches

## 4. CI/CD & Runners

- [ ] Audit and remove unused or forked workflow runners
- [ ] Verify workflow permissions use least-privilege (read-only default)
- [ ] Pin third-party actions to full commit SHAs
- [ ] Remove cached credentials and self-hosted runner leftovers

## 5. Repository Hygiene

- [ ] Confirm no secrets committed in history (review scanning alerts)
- [ ] Archive or delete abandoned repositories
- [ ] Review webhooks and deploy keys for orphaned entries

## 6. Incident Readiness

- [ ] Confirm on-call rotation is current
- [ ] Verify escalation contacts and runbooks are up to date
- [ ] Schedule the next quarterly drill

---

**Status:** Drill artifact committed via pull request and squash-merged to `main`.
