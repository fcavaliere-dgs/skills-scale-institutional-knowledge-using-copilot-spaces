# Release Readiness & QA Checklist

> **Changelog:** Added in PR "docs: expand personas and add role matrix & checklists" (2026-04-23). Relates to #4.

## Purpose

This checklist bridges the Execution & Tracking and Release & Deployment phases to reduce deployment issues and ensure every release meets quality and operational standards before going to production.

Complete this checklist before every production release. Any unchecked item should be documented with a resolution plan or explicit risk acceptance by the Accountable owner listed for that item.

For role responsibilities, see the [Role Responsibility Matrix](../octoacme-role-responsibility-matrix.md).  
For full release guidance, see [Release & Deployment Guide](../octoacme-release-and-deployment.md).

---

## How to use this checklist

1. Copy this file (or create an issue/ticket) for each release.
2. Assign the named owners to verify their sections before the release window.
3. If any item **fails**, follow the escalation path noted in that section.
4. Obtain final sign-off from the Product Manager and Project Manager before proceeding.

---

## 1. Acceptance Criteria & Feature Completeness

> Owner: **QA Lead** (Accountable: **Product Manager**)

- [ ] All acceptance criteria for in-scope user stories are marked as met in the backlog tool.
- [ ] No P0/P1 (critical/high severity) defects are open for in-scope features.
- [ ] Edge cases and error states identified in the spec have been tested.
- [ ] Product Manager has reviewed and approved the feature set for this release.
- [ ] Release scope is documented and communicated to Stakeholders.

**Escalation if failed:** QA Lead and Product Manager agree on scope reduction or defer the release. Project Manager notifies Stakeholders of impact.

---

## 2. Automated Tests

> Owner: **Developer / QA Lead** (Accountable: **QA Lead**)

- [ ] All unit tests pass in CI (0 failures, 0 skipped without documented justification).
- [ ] All integration/E2E tests pass in the staging/pre-production environment.
- [ ] Test coverage meets or exceeds the project's agreed threshold (document threshold: ______%).
- [ ] No known flaky tests are masking real failures.
- [ ] Test results from the latest CI run are linked here or in the release ticket: ___________________

**Escalation if failed:** Developer and QA Lead triage failing tests. If resolution exceeds the release window, escalate to Project Manager for go/no-go decision.

---

## 3. Security Scans

> Owner: **DevOps Engineer** (Accountable: **DevOps Engineer**)

- [ ] Dependency vulnerability scan (e.g., Dependabot, Snyk) shows no critical or high-severity unmitigated findings.
- [ ] SAST (static application security testing) scan has been run and findings reviewed.
- [ ] Secrets scanning has passed — no credentials or tokens committed to the repository.
- [ ] Container image scan (if applicable) shows no critical unmitigated CVEs.
- [ ] Security findings are documented with accepted-risk rationale where not remediated.

**Escalation if failed:** DevOps Engineer escalates unmitigated critical findings to Project Manager and Security/Compliance stakeholder. Release is blocked until mitigated or risk is explicitly accepted by an authorized stakeholder.

---

## 4. Performance Smoke Tests

> Owner: **Developer / DevOps Engineer** (Accountable: **DevOps Engineer**)

- [ ] Key user flows have been exercised against the staging environment and response times are within agreed SLOs.
- [ ] No memory leaks or resource exhaustion observed under representative load.
- [ ] Database query performance has been validated for any new or changed queries.
- [ ] Performance test results are documented and linked: ___________________

**Escalation if failed:** Developer and DevOps Engineer investigate root cause. Project Manager is informed. If unresolvable before release window, escalate to Product Manager for scope decision.

---

## 5. Rollback Plan

> Owner: **DevOps Engineer** (Accountable: **DevOps Engineer**)

- [ ] A documented rollback procedure exists for this release.
- [ ] The rollback has been tested or reviewed in a non-production environment.
- [ ] Rollback triggers (conditions that warrant rollback) are clearly defined.
- [ ] Rollback procedure is accessible to the on-call team during the release window.
- [ ] Rollback has been communicated to Project Manager and relevant Stakeholders.

**Escalation if failed:** Release is blocked until a rollback plan is documented and reviewed. DevOps Engineer owns resolution with support from Lead Developer.

---

## 6. Database Migration Plan

> Owner: **Developer / DevOps Engineer** (Accountable: **DevOps Engineer**)

- [ ] All database migrations are idempotent and have been tested in staging.
- [ ] Migration scripts are backwards-compatible with the current production version (or a maintenance window is scheduled).
- [ ] A rollback/revert migration is scripted and tested.
- [ ] Database backup has been verified before migration execution.
- [ ] Migration execution time is estimated and within the acceptable deployment window.

**Escalation if failed:** DevOps Engineer and Lead Developer resolve migration issues. If a maintenance window is required, Project Manager coordinates scheduling with Stakeholders.

---

## 7. Feature Flags

> Owner: **Developer / DevOps Engineer** (Accountable: **Product Manager**)

- [ ] All new features behind feature flags are toggled off in production at deployment time (unless explicitly releasing).
- [ ] Feature flag names, default states, and rollout plan are documented.
- [ ] Feature flag configuration has been reviewed by Product Manager.
- [ ] Stale or obsolete flags from previous releases have been cleaned up.

**Escalation if failed:** Developer corrects flag configuration before release. Product Manager approves any deviation from the rollout plan.

---

## 8. Monitoring & Alerts

> Owner: **DevOps Engineer** (Accountable: **DevOps Engineer**)

- [ ] Application monitoring (APM) is configured and receiving data from the staging environment.
- [ ] Alerts are defined for error rate, latency, and availability SLOs for this release.
- [ ] Dashboards are updated to reflect new endpoints, services, or metrics introduced in this release.
- [ ] On-call rotation is confirmed and the team knows how to escalate production incidents.
- [ ] Runbook for the most likely failure modes of this release is updated and accessible.

**Escalation if failed:** DevOps Engineer resolves monitoring gaps before release. If gaps cannot be closed in time, Project Manager assesses go/no-go risk with the team.

---

## 9. Stakeholder Sign-Off

> Owner: **Project Manager** (Accountable: **Product Manager**)

- [ ] Product Manager has reviewed and approved the release scope and quality status.
- [ ] Project Manager has confirmed timeline, deployment window, and communication plan.
- [ ] Key Stakeholders have been notified of the upcoming release and any user-facing changes.
- [ ] Release notes or changelog have been drafted and reviewed.
- [ ] Post-release monitoring plan (who watches, for how long, escalation steps) is agreed.

**Escalation if failed:** Project Manager resolves sign-off blockers. If a stakeholder is unavailable, document delegated authority and proceed with explicit documented approval.

---

## Final Go / No-Go Sign-Off

| Check | Status | Owner | Date |
|-------|--------|-------|------|
| Acceptance criteria met | ☐ Go / ☐ No-Go | QA Lead / PdM | |
| Automated tests passing | ☐ Go / ☐ No-Go | QA Lead | |
| Security scans clear | ☐ Go / ☐ No-Go | DevOps Engineer | |
| Performance smoke tests passed | ☐ Go / ☐ No-Go | DevOps Engineer | |
| Rollback plan confirmed | ☐ Go / ☐ No-Go | DevOps Engineer | |
| DB migration plan confirmed | ☐ Go / ☐ No-Go | DevOps Engineer | |
| Feature flags configured | ☐ Go / ☐ No-Go | Developer / PdM | |
| Monitoring & alerts configured | ☐ Go / ☐ No-Go | DevOps Engineer | |
| Stakeholder sign-off received | ☐ Go / ☐ No-Go | PM / PdM | |
| **Overall Release Decision** | ☐ **GO** / ☐ **NO-GO** | **Project Manager** | |
