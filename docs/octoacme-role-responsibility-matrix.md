# OctoAcme Role Responsibility Matrix

> **Changelog:** Added in PR "docs: expand personas and add role matrix & checklists" (2026-04-23). Relates to #4.

## Purpose

This matrix provides a quick reference for who is Responsible, Accountable, Consulted, and Informed (RACI) for core project activities. Use it to reduce ambiguity about ownership, clarify handoffs, and accelerate decision-making.

For full descriptions of each role, see [Roles and Personas](./octoacme-roles-and-personas.md).

---

## RACI Key

| Symbol | Meaning |
|--------|---------|
| **R** | **Responsible** — Does the work. |
| **A** | **Accountable** — Owns the outcome; final decision-maker. Only one per row. |
| **C** | **Consulted** — Provides input before or during; two-way communication. |
| **I** | **Informed** — Kept up to date; one-way communication. |

---

## Matrix

| Activity | Developer | Product Manager (PdM) | Project Manager (PM) | UX Designer | DevOps Engineer | QA Lead | Data Analyst | Scrum Master |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **Define success metrics** | I | **A** | I | C | I | C | **R** | I |
| **Prioritize backlog** | C | **A** | C | C | I | C | C | **R** (facilitates) |
| **Implement feature** | **R/A** | C | I | C | C | C | I | I |
| **Acceptance testing** | C | **A** | I | C | I | **R** | I | I |
| **CI/CD & deployment** | C | I | I | I | **R/A** | C | I | I |
| **Monitor production** | C | I | I | I | **R/A** | C | C | I |
| **Run retrospectives** | C | C | C | C | C | C | C | **R/A** |
| **Stakeholder communication** | I | C | **R/A** | I | I | I | C | I |
| **Risk management** | C | C | **R/A** | I | C | C | I | C |
| **UX research** | I | C | I | **R/A** | I | C | C | I |
| **Data analysis** | I | C | I | C | I | C | **R/A** | I |

---

## Notes

- **R/A** in a single cell means the same person or role is both responsible for doing the work and accountable for the outcome. This is common when a role is the sole owner of an activity.
- Where multiple roles share **R**, agree upfront on a primary owner to avoid diffusion of responsibility.
- The **Scrum Master** role for "Prioritize backlog" is listed as facilitation only; the Product Manager retains accountability.

---

## Adapting for team size

| Team size | Recommendation |
|-----------|---------------|
| **Small (< 5)** | Combine roles where needed (e.g., Developer covers QA Lead duties). Update the matrix to reflect one person holding multiple role columns. |
| **Medium (5–15)** | This matrix applies as-is with minor adjustments. Identify coverage for any roles that are not staffed. |
| **Large (> 15)** | Consider splitting roles into sub-roles (e.g., multiple QA engineers under a QA Lead) and adding organization-specific governance roles (e.g., Release Manager, Security Champion). |

For onboarding new team members to their role's responsibilities, see [Role Onboarding Checklist](./role-onboarding-checklist.md).
