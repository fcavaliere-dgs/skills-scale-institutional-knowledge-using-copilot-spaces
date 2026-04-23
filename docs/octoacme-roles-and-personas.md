# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

## How to use these persona definitions

Use these entries to:
- Assign clear ownership and accountability across the project lifecycle.
- Frame scenarios and sample interactions in Copilot Spaces exercises.
- Adapt each persona to your team's actual structure — not every project will include every role listed here.

**Customizing for team size:** On small teams, one person may cover multiple roles (e.g., a Developer who also acts as QA Lead). On larger teams, each role may be staffed by multiple individuals. Adjust responsibilities and interaction lines accordingly. For Agile teams, the Scrum Master persona is especially relevant; for non-Agile delivery models it can be omitted or adapted.

For a quick view of who does what across key activities, see the [Role Responsibility Matrix](./octoacme-role-responsibility-matrix.md).

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Interactions / Collaborations
- Work closely with QA Lead on testability and defect triage.
- Collaborate with DevOps Engineer on CI/CD pipeline requirements and build stability.
- Receive design specifications and user flows from UX Designer.
- Participate in backlog refinement with the Product Manager and Scrum Master.

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

### Example Artifacts
- Pull requests with linked acceptance criteria
- Unit and integration test suites
- Technical design documents and ADRs

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Interactions / Collaborations
- Partner with UX Designer on user research synthesis and feature discovery.
- Align with Data Analyst on success metrics and post-launch measurement.
- Work with Project Manager on roadmap timing, dependencies, and risk trade-offs.
- Engage Stakeholders regularly for input and sign-off.

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

### Example Artifacts
- Product brief / one-pager
- Prioritized backlog with acceptance criteria
- Success metrics dashboard

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Interactions / Collaborations
- Coordinate closely with Product Manager on scope, priorities, and timeline trade-offs.
- Escalate blockers and risks to Stakeholders with recommended mitigations.
- Support Scrum Master in ceremony facilitation and impediment removal.
- Keep DevOps Engineer informed of release and deployment schedule.

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

### Example Artifacts
- Project charter and milestone plan
- Risk register and decision log
- Status report and escalation memo

---

## UX Designer

### Role Summary
UX Designers craft and validate the user experience to ensure products are usable, accessible, and aligned with customer needs. They translate user research and business requirements into concrete interface designs.

### Responsibilities
- Conduct user research (interviews, usability tests, surveys)
- Create wireframes, prototypes, and user flow diagrams
- Maintain and evolve the design system and component library
- Collaborate on acceptance criteria to include usability standards
- Iterate designs based on feedback and usability testing results

### Goals
- Ensure the product is intuitive and meets user needs
- Reduce usability defects and support requests post-launch
- Align visual design with brand guidelines and accessibility standards

### Typical Interactions / Collaborations
- Work with Product Manager to translate feature requirements into user stories and design briefs.
- Hand off design specs and assets to Developers for implementation.
- Collaborate with QA Lead to define usability acceptance criteria.
- Share research insights with Data Analyst and Product Manager to inform prioritization.

### Example Artifacts
- Wireframes and interactive prototypes (e.g., Figma files)
- User journey maps and flow diagrams
- Usability test reports and design decision log

---

## DevOps Engineer

### Role Summary
DevOps Engineers build and maintain the infrastructure, CI/CD pipelines, and operational tooling that enable the team to ship software reliably and quickly. They bridge the gap between development and production operations.

### Responsibilities
- Design, implement, and maintain CI/CD pipelines and deployment automation
- Manage cloud infrastructure, environments, and infrastructure-as-code (IaC)
- Implement monitoring, alerting, and observability tooling
- Manage secrets, certificates, and access controls
- Perform capacity planning and incident response

### Goals
- Maximize deployment frequency while minimizing change failure rate and recovery time
- Ensure production environments are stable, secure, and observable
- Reduce toil through automation

### Typical Interactions / Collaborations
- Work with Developers to ensure builds, tests, and deployments run reliably in CI/CD.
- Coordinate with QA Lead on automated test integration in pipelines.
- Inform Project Manager and stakeholders of environment readiness and release windows.
- Engage Security/Compliance on hardening requirements.

### Example Artifacts
- CI/CD pipeline configuration (e.g., GitHub Actions workflows)
- Infrastructure-as-code templates (e.g., Terraform, Bicep)
- Runbooks and incident post-mortems
- Monitoring dashboards and alert definitions

---

## QA Lead

### Role Summary
QA Leads own the overall test strategy, quality standards, and defect management process. They ensure that acceptance criteria are verifiable and that releases meet quality thresholds before reaching production.

### Responsibilities
- Define and maintain the test strategy (unit, integration, E2E, performance, security)
- Coordinate manual and automated test execution
- Manage defect tracking, triage, and escalation
- Define and enforce the Definition of Done and acceptance test criteria
- Report on quality metrics (defect rates, test coverage, open bugs)

### Goals
- Prevent defects from reaching production
- Increase test automation coverage to reduce manual testing overhead
- Ensure every release meets agreed quality gates

### Typical Interactions / Collaborations
- Partner with Developers on testability, test data setup, and defect resolution.
- Align with Product Manager on acceptance criteria and release readiness.
- Coordinate with DevOps Engineer on integrating automated tests into CI/CD pipelines.
- Provide quality sign-off to Project Manager and Stakeholders before releases.

### Example Artifacts
- Test plan and test cases
- Defect reports and triage notes
- Quality metrics dashboard
- Release sign-off checklist (see also [Release Readiness & QA Checklist](./checklists/release-readiness-and-qa-checklist.md))

---

## Data Analyst

### Role Summary
Data Analysts define, track, and interpret success metrics. They provide actionable insights that help the team understand product performance and make evidence-based decisions.

### Responsibilities
- Define KPIs and measurement plans in alignment with product goals
- Build and maintain dashboards and reports
- Analyze usage data to identify trends, regressions, or opportunities
- Support A/B test design and results interpretation
- Provide data-driven input to backlog prioritization and roadmap decisions

### Goals
- Ensure the team has timely, accurate data to measure feature impact
- Make data accessible and understandable to non-technical stakeholders
- Identify risks or regressions from data before they escalate

### Typical Interactions / Collaborations
- Collaborate with Product Manager to define success metrics at feature inception.
- Work with Developers and DevOps Engineer to ensure instrumentation and event tracking are implemented correctly.
- Present insights to Project Manager and Stakeholders in regular review cadences.
- Support UX Designer with quantitative data to complement qualitative research.

### Example Artifacts
- KPI and measurement plan
- Analytics dashboards (e.g., Looker, Grafana, Power BI)
- A/B test design and results summary
- Data quality validation report

---

## Scrum Master

> **Note:** This persona is most relevant for teams following Agile/Scrum methodology. Adapt or omit for non-Agile delivery models.

### Role Summary
Scrum Masters serve as process facilitators and coaches. They protect the team's focus, remove impediments, and continuously improve team effectiveness by applying Agile principles.

### Responsibilities
- Facilitate all Scrum ceremonies (sprint planning, daily standup, sprint review, retrospective)
- Identify and remove impediments that slow the team down
- Coach team members on Agile practices and Scrum values
- Shield the team from unplanned work and external distractions
- Track and surface team health and velocity metrics

### Goals
- Improve team velocity and predictability sprint over sprint
- Foster a culture of continuous improvement and psychological safety
- Enable the team to self-organize effectively

### Typical Interactions / Collaborations
- Facilitate collaboration between Product Manager (backlog grooming) and Developers (sprint execution).
- Support Project Manager with ceremony outputs (sprint reviews, retrospective action items).
- Coach the team and individual members on Agile practices.
- Escalate systemic impediments to management or Project Manager when team-level resolution is insufficient.

### Example Artifacts
- Sprint velocity charts and burndown charts
- Retrospective notes and action-item log
- Team working agreements and norms document
- Impediment log

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

