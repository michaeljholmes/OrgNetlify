# Production Incident and Bug Management

## Scope

This process covers:

- Bugs raised in production (customer reported, monitoring alerts, ops escalations)

## Principles

- Severity is based on customer impact and risk, not effort.
- Mitigation comes before root cause fix for high severity issues.
- The engineering team that owns the area owns investigation and remediation.
- Product owns priority decisions and user impact trade-offs.

## Bug sources and how they are handled

### Bugs raised in production

- Bugs raised must contain clear customer impact, and any immediate reproduction steps.
- Assign a severity (P1-P4) - if P1 - handle in a different way....
- Development investigates and mitigates.
- Product coordinates customer/stakeholder comms where needed alongside Support Team (especially P1/P2).
- Fix is implemented and verified. Releasing of issue TBD.

## Severity levels (P1-P4)

| Priority | Definition | Typical examples | Handling |
| --- | --- | --- | --- |
| P1 | Critical production incident. Major customer impact, security risk, data loss/corruption, or system-wide outage. | Outage, payments/critical workflows broken for many users, data corruption, security incident. | Immediate swarming. Create incident channel. Mitigate first (rollback/feature flag/hotfix). Frequent updates until stable. Post-incident review required (process TBD) |
| P2 | High impact bug with significant degradation or impact to a subset of customers/workflows. No immediate data loss but urgent. | Key workflow broken for one customer/segment, severe performance regression, repeated failures with workaround. | Same-day triage. Prioritise fix ahead of normal work. Mitigation if available. Regular updates to stakeholders. Review recommended. |
| P3 | Medium impact defect. Non-critical workflow issue, limited impact, or acceptable workaround exists. | UI issue with workaround, incorrect validation edge case, minor performance issue. | Triage in normal cadence. Schedule into sprint/backlog. Fix with standard release process. |
| P4 | Low impact defect or cosmetic issue. Minimal customer impact. | Copy/layout issues, minor inconsistencies, low-priority edge cases. | Log and backlog. Fix opportunistically or when bundled with related work. |

## Roles and responsibilities

### Product team

- Own severity assessment inputs (impact, affected users, business risk) and prioritisation.
- Provide clear expected behaviour/acceptance criteria for reported issues.
- Coordinate stakeholder/customer communication where needed alongside Support Team (especially P1/P2).
- Validate fixes against acceptance criteria.

### Development team

- Own technical triage (reproduction, root cause investigation, mitigation, fix).
- Own safe delivery of changes (tests, rollout plan, monitoring where appropriate).
- For recurring regressions, add/strengthen automated tests and preventative measures.

## Triage checklist

- What is the customer impact and how many users/customers are affected?
- Is there data loss/corruption risk?
- Is there a workaround?
- Is the issue reproducible and what are the steps?
- What changed recently (release/version/feature flags)?
- Who owns the area and who needs to be involved?

## Closure

- Confirm fix is deployed and verified.
- Ensure the ticket includes:
  - reproduction steps
  - expected vs actual
  - severity (P1-P4)
  - resolution notes
- For P1/P2, monitor the issue and update as needed. Complete post-incident review (process TBD). 
