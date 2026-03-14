# OctoAcme — Templates & Checklists

This file is the canonical hub for reusable templates and checklists referenced across OctoAcme process docs.  
Use relative links from other docs to point here rather than duplicating content.

---

## RACI-lite / Ownership Matrix

Use this lightweight ownership table to clarify who is **Responsible**, **Accountable**, **Consulted**, or **Informed** for key activities. Copy and fill in for each project or workstream.

| Activity | Project Manager (PM) | Product Manager (PdM) | Developer | QA / Testing | UX Designer | DevOps Engineer | Security Lead | Customer Support | Business Analyst |
|---|---|---|---|---|---|---|---|---|---|
| Define requirements | C | A/R | C | C | C | I | C | C | R |
| Prioritize backlog | C | A/R | C | I | C | I | C | C | C |
| Design UX / wireframes | I | C | C | I | A/R | I | I | I | C |
| Implement features | I | I | A/R | C | C | C | C | I | I |
| Security review | I | C | R | C | I | R | A/R | I | I |
| CI/CD pipeline | C | I | C | C | I | A/R | C | I | I |
| Test & QA sign-off | C | C | R | A/R | C | C | C | I | I |
| Release readiness | A/R | C | C | C | I | C | C | C | I |
| Stakeholder comms | A/R | C | I | I | I | I | I | R | C |
| Risk tracking | A/R | C | C | C | I | C | C | I | C |

> **Key:** R = Responsible, A = Accountable, C = Consulted, I = Informed  
> Adapt this matrix to your specific project — not every activity applies to every project.

---

## Project Kickoff Agenda Template

Use at the start of a new project or major initiative.

```
## Kickoff Meeting Agenda

**Project name:**  
**Date:**  
**Facilitator (PM):**  
**Attendees:**  

1. Welcome & introductions (5 min)
2. Problem statement & goals — PdM presents (10 min)
3. Scope walkthrough — what's in / out (10 min)
4. Roles & responsibilities — confirm owners using RACI-lite (10 min)
5. Timeline & milestones overview (10 min)
6. Risks & dependencies — initial list (10 min)
7. Communication plan & meeting cadence (5 min)
8. Q&A and next steps (10 min)

**Action items captured:**
| Action | Owner | Due date |
|---|---|---|
|  |  |  |
```

---

## Risk Register Table Template

Use this table in your risk register. Align with the risk lifecycle in [octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md).

```
| ID | Description | Impact (H/M/L) | Likelihood (H/M/L) | Owner | Mitigation plan | Status |
|---|---|---|---|---|---|---|
| R-001 |  |  |  |  |  | Open |
| R-002 |  |  |  |  |  | Open |
```

> **Impact & Likelihood guide:**  
> - **High:** Significant schedule slip (>1 sprint), revenue/customer impact, or security breach  
> - **Medium:** Minor delay (<1 sprint) or degraded quality  
> - **Low:** Unlikely or negligible impact  

> **Status values:** Open, Mitigated, Accepted, Closed

---

## Release Readiness Checklist

Use before every release. Align with [octoacme-release-and-deployment.md](./octoacme-release-and-deployment.md).

- [ ] All acceptance criteria for in-scope features are met
- [ ] All PRs for this release are merged to the target branch
- [ ] CI pipeline passes (tests, lint, security scans)
- [ ] QA sign-off obtained (functional, regression, and exploratory testing complete)
- [ ] Security Lead has reviewed security-sensitive changes
- [ ] DevOps Engineer has confirmed deployment pipeline and rollback procedure
- [ ] Release notes drafted and reviewed by PdM
- [ ] Customer Support briefed on changes, known issues, and customer-facing messaging
- [ ] Deployment window scheduled and communicated to stakeholders
- [ ] Post-deploy monitoring and alerting verified to be active
- [ ] Rollback plan documented and tested (staging)

---

## Definition of Done / Acceptance Criteria Checklist

Apply this checklist to every backlog item (story/feature) before marking it **Done**. Adapt as needed per project.

### Code & Implementation
- [ ] Code implements all acceptance criteria as defined in the backlog item
- [ ] Code reviewed and approved by at least one peer (PR approved)
- [ ] No new linting errors or warnings introduced
- [ ] Automated tests written (unit and/or integration) for new logic

### Quality & Testing
- [ ] All automated tests pass in CI
- [ ] QA has validated the feature against acceptance criteria
- [ ] Edge cases and error states tested (manual or automated)
- [ ] No regressions introduced in related features

### Security & Compliance
- [ ] Security Lead consulted for security-sensitive changes
- [ ] No new high/critical vulnerabilities introduced (security scan clean)
- [ ] Secrets and credentials not committed to source control

### Documentation & Communication
- [ ] Relevant docs updated (README, process docs, API docs, etc.)
- [ ] Release notes updated or backlog item tagged for release notes
- [ ] Stakeholders and Customer Support informed of any user-facing changes

### Deployment Readiness
- [ ] Feature can be deployed independently or is gated behind a feature flag
- [ ] DevOps Engineer notified of any infrastructure or pipeline changes required
