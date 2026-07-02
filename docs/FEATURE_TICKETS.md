# Feature Tickets

## Backlog Overview

| Field | Value |
| --- | --- |
| Project | {{ProjectName}} |
| Product owner | {{ProductOwner}} |
| Technical owner | {{TechnicalOwner}} |
| Last updated | {{YYYY-MM-DD}} |

## Ticket Template

Copy this section for each feature, improvement, or technical task.

### {{TICKET-ID}}: {{TicketTitle}}

| Field | Value |
| --- | --- |
| Status | {{Backlog/Ready/In Progress/In Review/Done/Blocked}} |
| Priority | {{P0/P1/P2/P3}} |
| Phase | {{MVP/Phase 2/Nice To Have/Future/Technical Debt}} |
| Owner | {{Owner}} |
| Estimate | {{Small/Medium/Large or points}} |
| Dependencies | {{DependenciesOrNone}} |

**Problem**

{{ProblemStatement}}

**User Story**

As a {{UserRole}}, I want {{Capability}}, so that {{Benefit}}.

**Scope**

- {{InScopeItem1}}
- {{InScopeItem2}}
- {{InScopeItem3}}

**Out Of Scope**

- {{OutOfScopeItem1}}
- {{OutOfScopeItem2}}

**Acceptance Criteria**

- [ ] {{Criterion1}}
- [ ] {{Criterion2}}
- [ ] {{Criterion3}}

**Implementation Notes**

- {{TechnicalNote1}}
- {{TechnicalNote2}}
- {{AnalyticsOrSEOOrSecurityNote}}

**Design And Content**

- Design: {{DesignLinkOrStatus}}
- Copy: {{CopyRequirement}}
- Assets: {{AssetRequirement}}

**Testing**

- [ ] Unit or component tests: {{Requirement}}
- [ ] Integration tests: {{Requirement}}
- [ ] E2E tests: {{Requirement}}
- [ ] Accessibility review: {{Requirement}}
- [ ] Responsive review: {{Requirement}}

**Release Notes**

{{UserFacingReleaseNoteOrInternalNote}}

---

## MVP

### MVP-001: {{CoreFeatureName}}

| Field | Value |
| --- | --- |
| Status | {{Backlog}} |
| Priority | {{P0}} |
| Owner | {{Owner}} |
| Estimate | {{Estimate}} |
| Dependencies | {{DependenciesOrNone}} |

**Problem**

{{CoreProblemStatement}}

**User Story**

As a {{PrimaryUser}}, I want {{CoreCapability}}, so that {{PrimaryBenefit}}.

**Acceptance Criteria**

- [ ] {{MvpCriterion1}}
- [ ] {{MvpCriterion2}}
- [ ] {{MvpCriterion3}}

**Implementation Notes**

- {{ImplementationNote}}
- {{SecurityOrValidationNote}}
- {{AnalyticsEventNote}}

### MVP-002: {{OnboardingOrConversionFeature}}

| Field | Value |
| --- | --- |
| Status | {{Backlog}} |
| Priority | {{P0}} |
| Owner | {{Owner}} |
| Estimate | {{Estimate}} |
| Dependencies | {{DependenciesOrNone}} |

**Problem**

{{ProblemStatement}}

**User Story**

As a {{UserRole}}, I want {{Capability}}, so that {{Benefit}}.

**Acceptance Criteria**

- [ ] {{Criterion1}}
- [ ] {{Criterion2}}
- [ ] {{Criterion3}}

**Implementation Notes**

- {{ImplementationNote}}
- {{ContentOrDesignNote}}
- {{MeasurementNote}}

## Phase 2

### P2-001: {{ExpansionFeatureName}}

| Field | Value |
| --- | --- |
| Status | {{Backlog}} |
| Priority | {{P1}} |
| Owner | {{Owner}} |
| Estimate | {{Estimate}} |
| Dependencies | {{DependenciesOrNone}} |

**Problem**

{{ProblemStatement}}

**User Story**

As a {{UserRole}}, I want {{Capability}}, so that {{Benefit}}.

**Acceptance Criteria**

- [ ] {{Criterion1}}
- [ ] {{Criterion2}}
- [ ] {{Criterion3}}

**Implementation Notes**

- {{ImplementationNote}}
- {{OperationalNote}}

### P2-002: {{IntegrationOrWorkflowFeature}}

| Field | Value |
| --- | --- |
| Status | {{Backlog}} |
| Priority | {{P1}} |
| Owner | {{Owner}} |
| Estimate | {{Estimate}} |
| Dependencies | {{DependenciesOrNone}} |

**Problem**

{{ProblemStatement}}

**User Story**

As a {{UserRole}}, I want {{Capability}}, so that {{Benefit}}.

**Acceptance Criteria**

- [ ] {{Criterion1}}
- [ ] {{Criterion2}}
- [ ] {{Criterion3}}

**Implementation Notes**

- {{ImplementationNote}}
- {{DataOrAPIContractNote}}

## Nice To Have

### NTH-001: {{NiceToHaveFeatureName}}

| Field | Value |
| --- | --- |
| Status | {{Backlog}} |
| Priority | {{P2}} |
| Owner | {{Owner}} |
| Estimate | {{Estimate}} |
| Dependencies | {{DependenciesOrNone}} |

**Problem**

{{ProblemStatement}}

**User Story**

As a {{UserRole}}, I want {{Capability}}, so that {{Benefit}}.

**Acceptance Criteria**

- [ ] {{Criterion1}}
- [ ] {{Criterion2}}

**Implementation Notes**

- {{ImplementationNote}}

## Future Ideas

| Idea | Target user | Expected value | Trigger to revisit |
| --- | --- | --- | --- |
| {{Idea1}} | {{User}} | {{Value}} | {{SignalOrMilestone}} |
| {{Idea2}} | {{User}} | {{Value}} | {{SignalOrMilestone}} |
| {{Idea3}} | {{User}} | {{Value}} | {{SignalOrMilestone}} |

## Technical Debt

### TD-001: {{TechnicalDebtItem}}

| Field | Value |
| --- | --- |
| Status | {{Backlog}} |
| Priority | {{P1/P2/P3}} |
| Owner | {{Owner}} |
| Estimate | {{Estimate}} |
| Risk if deferred | {{Risk}} |

**Problem**

{{TechnicalProblemStatement}}

**Acceptance Criteria**

- [ ] {{DebtCriterion1}}
- [ ] {{DebtCriterion2}}

**Implementation Notes**

- {{RefactorOrCleanupNote}}
- {{TestingOrMigrationNote}}

## Backlog Triage Checklist

- [ ] Every P0 ticket has clear acceptance criteria.
- [ ] MVP scope supports the primary product goal.
- [ ] Dependencies and blockers are visible.
- [ ] Security, accessibility, analytics, and SEO needs are represented.
- [ ] Technical debt is tracked separately from user-facing feature work.
- [ ] Deferred ideas include a signal for when to revisit them.
