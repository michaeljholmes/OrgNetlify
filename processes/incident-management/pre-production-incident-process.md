# Pre-Production Incident and Bug Management

## Scope

This process covers:

- Bugs found by the product team in dev/test/staging environments

## Principles

- Severity is based on release-blocking potential and quality risk, not effort.
- The engineering team that owns the area owns investigation and remediation.
- Product owns priority decisions based on feature importance and release timelines.

## Bug sources and how they are handled

### Bugs found by product in dev/test/staging environments

- Log the bug with clear acceptance criteria expectation vs actual behaviour.
- Assign a severity (P1-P4) and confirm if it blocks release/sign-off.
- Development triages and fixes within the agreed priority.
- Product validates the fix against acceptance criteria.
- Release of fix TBD.

## Severity levels (P1-P4)

| Priority | Definition | Typical examples | Handling |
| --- | --- | --- | --- |
| P1 | Critical defect blocking a release or major feature sign-off. | A core user journey is broken with no workaround, data corruption, security vulnerability found in testing. | Immediate attention required. Fix is a top priority for the responsible team. Must be fixed and verified before release. |
| P2 | High impact defect that significantly degrades a feature. A workaround may exist but is not acceptable for release. | A key feature is partially functional, significant performance issue found, a confusing or broken UI flow. | High priority in the current sprint or backlog. Should be fixed before release if possible. |
| P3 | Medium impact defect. Non-critical issue with a reasonable workaround, or an issue in a non-essential part of the product. | Minor UI issue with a workaround, incorrect validation on an edge case. | Triage in normal cadence. Schedule into the backlog to be fixed in a future sprint. |
| P4 | Low impact or cosmetic issue. Minimal impact on functionality. | Copy/layout issues, minor UI inconsistencies. | Log and backlog. Fix opportunistically when time allows. |

## Roles and responsibilities

### Product team

- Own severity assessment inputs (release impact, quality risk) and prioritisation.
- Provide clear expected behaviour/acceptance criteria for reported issues.
- Validate fixes against acceptance criteria.

### Development team

- Own technical triage (reproduction, root cause investigation, mitigation, fix).
- Own safe delivery of changes (tests, rollout plan, monitoring where appropriate).
- For recurring regressions, add/strengthen automated tests and preventative measures.

## Triage checklist

- Does this block a release or feature sign-off?
- What is the impact on the feature/user journey being tested?
- Is there a risk of data corruption?
- Is there a workaround available for testing to continue?
- Is the issue reproducible and what are the steps?
- What changed recently (code commit/version/feature flags)?
- Who owns the area and who needs to be involved?

## Closure

- Confirm fix is deployed and verified.
- Ensure the ticket includes:
  - reproduction steps
  - expected vs actual
  - severity (P1-P4)
  - resolution notes
- For P1/P2 issues, ensure the fix is robust and consider if a new automated test is required. 
