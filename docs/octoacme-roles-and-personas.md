# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

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

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

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

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

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

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

---

## QA / Testing

### Role Summary
QA Engineers validate that features meet acceptance criteria and quality standards before release. They partner with developers and Product Managers to define testable requirements.

### Responsibilities
- Design and execute test plans (functional, regression, exploratory)
- Define and uphold acceptance criteria and the Definition of Done
- Automate tests in CI where feasible
- File and triage defect reports
- Sign off on release readiness

### Goals
- Prevent defects from reaching production
- Maintain high test coverage and confidence in every release
- Provide fast, clear feedback to developers

### Typical Communication
- Sprint ceremonies and review demos
- Bug reports and test result summaries
- Definition of Done reviews with Project Manager and developers

### Interactions with Existing Roles
- **Project Manager (PM):** Coordinates test timelines; flags blockers that may impact milestones.
- **Product Manager (PdM):** Clarifies acceptance criteria and validates feature behavior matches requirements.
- **Developers:** Reviews code changes, provides reproduction steps, and aligns on fix verification.
- **UX Designer:** Reviews UI implementations against design specs.
- **Security Lead:** Executes security test cases provided by the Security Lead.

---

## UX Designer

### Role Summary
UX Designers lead user research and interface design to ensure products are usable, accessible, and aligned with customer needs. They bridge product requirements and technical implementation.

### Responsibilities
- Conduct user research (interviews, usability tests, surveys)
- Create wireframes, prototypes, and high-fidelity designs
- Define and document interaction patterns and design system usage
- Facilitate design reviews and hand off specs to developers
- Advocate for accessibility and inclusive design

### Goals
- Deliver intuitive experiences that reduce friction for end users
- Ensure design intent is faithfully implemented by engineering
- Continuously incorporate user feedback into the design process

### Typical Communication
- Design reviews with Product Manager and developers
- Prototype walkthroughs and usability test readouts
- Async comments via design tooling (e.g., Figma) and GitHub PRs

### Interactions with Existing Roles
- **Product Manager (PdM):** Aligns on feature requirements and user stories; participates in prioritization to balance UX investment.
- **Project Manager (PM):** Coordinates design timelines and review milestones to avoid blocking development sprints.
- **Developers:** Provides design handoff assets and clarifies specifications during implementation; reviews UI in PRs.
- **QA / Testing:** Shares design specs so QA can validate visual and interaction correctness against acceptance criteria.
- **Business Analyst:** Collaborates on user flows and process diagrams to ensure designs match real-world workflows.

---

## DevOps Engineer

### Role Summary
DevOps Engineers build and maintain the CI/CD pipelines, infrastructure, and tooling that enable fast, reliable delivery. They bridge development and operations to improve deployment safety and observability.

### Responsibilities
- Design, build, and maintain CI/CD pipelines and automation
- Provision and manage infrastructure (cloud, containers, etc.)
- Monitor system health, performance, and availability
- Define and enforce deployment standards and rollback procedures
- Support incident response and post-incident reviews
- Collaborate with Security Lead on compliance and toolchain hardening

### Goals
- Minimize deployment risk through automation and testing gates
- Reduce mean time to recovery (MTTR) for production incidents
- Keep infrastructure costs and operational overhead manageable

### Typical Communication
- Release planning sessions and deployment windows
- Runbooks, incident reports, and post-mortems
- Infrastructure change proposals and review comments in PRs

### Interactions with Existing Roles
- **Project Manager (PM):** Coordinates deployment scheduling, release windows, and infrastructure capacity needs.
- **Developers:** Provides build and deployment tooling, reviews infrastructure-as-code, and unblocks CI issues.
- **QA / Testing:** Provisions and maintains testing environments; ensures CI gates run the agreed test suite.
- **Security Lead:** Implements security tooling in the pipeline (SAST, dependency scanning) and co-owns compliance controls.
- **Product Manager (PdM):** Communicates infrastructure constraints or risks that may affect roadmap timelines.

---

## Security Lead

### Role Summary
The Security Lead owns the security posture of projects and products. They ensure security considerations are embedded throughout the project lifecycle—from design through release and beyond.

### Responsibilities
- Conduct threat modeling and security reviews for new features and architecture changes
- Identify, prioritize, and track vulnerabilities (CVEs, findings from scanning tools)
- Define security acceptance criteria and add security gates to CI/CD pipelines
- Create and maintain incident response runbooks
- Educate the team on secure coding practices and organizational security policies
- Act as the escalation point for security-impacting incidents

### Goals
- Prevent security vulnerabilities from reaching production
- Ensure timely remediation of identified risks
- Foster a security-conscious engineering culture

### Typical Communication
- Threat model reviews and security design walkthroughs
- Vulnerability reports and remediation status updates
- Security incident communications and post-incident retrospectives

### Interactions with Existing Roles
- **Project Manager (PM):** Flags security risks that affect timelines; ensures security tasks are tracked in the project board.
- **Product Manager (PdM):** Escalates risk acceptance decisions; inputs security requirements into feature definitions.
- **Developers:** Provides secure coding guidance, reviews security-sensitive code, and validates fixes.
- **DevOps Engineer:** Collaborates on pipeline security controls, secrets management, and infrastructure hardening.
- **QA / Testing:** Provides security test cases and participates in security-focused test reviews.

---

## Customer Support Representative

### Role Summary
Customer Support Representatives are the primary point of contact for end users. They surface customer feedback, report issues, and help ensure product changes are communicated clearly to customers.

### Responsibilities
- Receive, triage, and escalate customer-reported issues
- Document reproducible steps for bugs and forward to the development team
- Communicate upcoming changes, releases, and known issues to customers
- Synthesize recurring user pain points and surface them as input to roadmap planning
- Maintain customer-facing release notes and FAQ documentation

### Goals
- Minimize customer impact from bugs and unexpected changes
- Ensure the team has visibility into real-world usage patterns and pain points
- Reduce escalation volume through proactive communication and documentation

### Typical Communication
- Bug and feedback reports shared with PM/PdM and QA
- Customer-facing release announcements and change logs
- Support escalation summaries in weekly syncs

### Interactions with Existing Roles
- **Product Manager (PdM):** Shares aggregated customer feedback and feature requests to inform backlog prioritization.
- **Project Manager (PM):** Raises urgent customer-impacting issues for prioritization and escalation.
- **Developers:** Provides detailed reproduction steps for bugs and validates fixes from a customer perspective.
- **QA / Testing:** Collaborates on edge case scenarios surfaced from real customer reports.
- **Stakeholders:** Represents the voice of the customer in stakeholder reviews and planning sessions.

---

## Business Analyst

### Role Summary
Business Analysts bridge business strategy and technical delivery. They gather, analyze, and document requirements to ensure the team builds the right thing for the right reasons.

### Responsibilities
- Elicit and document business and functional requirements
- Create process diagrams, use cases, and workflow models
- Validate that proposed solutions address underlying business needs
- Facilitate requirements workshops with stakeholders and engineering
- Support data analysis and impact assessment for proposed changes
- Maintain traceability between business goals and implemented features

### Goals
- Ensure requirements are complete, clear, and actionable before development begins
- Reduce rework caused by late-stage requirement changes
- Enable data-driven decisions by providing analysis and impact models

### Typical Communication
- Requirements documents and process diagrams
- Facilitated workshops and requirements review meetings
- Backlog refinement sessions with Product Manager and developers

### Interactions with Existing Roles
- **Product Manager (PdM):** Collaborates on scope definition, translating business goals into detailed requirements and acceptance criteria.
- **Project Manager (PM):** Aligns on timeline feasibility and helps prioritize requirements to meet project milestones.
- **Developers:** Provides detailed requirement specifications and is available to clarify ambiguities during implementation.
- **Stakeholders:** Facilitates requirements-gathering sessions and validates that delivered solutions meet business value expectations.
- **UX Designer:** Co-creates user flows and process diagrams to ensure designs reflect actual business workflows.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- For ownership assignments across roles, see the [RACI-lite template in octoacme-templates-and-checklists.md](./octoacme-templates-and-checklists.md#raci-lite--ownership-matrix).

