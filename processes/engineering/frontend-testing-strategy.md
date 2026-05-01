# Frontend Engineering Testing Strategy

## Philosophy: Quality is Built-In, Not Inspected

As a team, we have shifted from relying on a separate test department to a model where quality is an engineering responsibility from the start. This means:
-   **We own our quality**: We build quality into our work, rather than having it inspected at the end.
-   **Automation is our safety net**: We invest in robust automated testing to catch regressions and enable confident deployments.
-   **We are accountable**: We are accountable for the build quality and automated validation of the features we ship.

This document outlines the automated testing strategy for the Frontend team.

## Guiding Principles

-   **Developers Own Quality**: The engineer who writes the code is responsible for ensuring it is well-tested.
-   **The Testing Pyramid**: We follow the testing pyramid model, emphasizing a large base of fast, isolated unit tests, a good number of integration/contract tests, and a select few end-to-end tests.
-   **Automation is Key**: All tests must be automated and integrated into our Continuous Integration (CI) pipeline.

## Testing Layers & Responsibilities

### 1. Unit Tests

-   **Purpose**: To test individual UI components or functions in isolation.
-   **Responsibility**: Every developer is responsible for writing unit tests for the code they produce.
-   **Coverage Target**: We aim for a minimum of **80% code coverage** for all new code.
-   **Execution**: Run automatically on every commit in the CI pipeline.

### 2. Contract Tests (GraphQL)

-   **Purpose**: To verify that the GraphQL service adheres to the agreed-upon schema and that the data returned matches the expected structure. This ensures that the contract between the frontend and backend is maintained.
-   **Responsibility**: The Frontend team is primarily responsible for writing contract tests against the GraphQL schema.
-   **Execution**: Run automatically as part of the CI pipeline for the frontend application.

### 3. E2E Regression Tests

-   **Purpose**: To simulate real user journeys through the entire application to catch regressions before a release. These are our highest-level, most comprehensive tests.
-   **Responsibility**: E2E tests are a shared responsibility. The developer building a feature is responsible for adding or updating E2E tests for the critical user paths they are affecting.
-   **Framework**: Playwright
-   **Execution**: Run automatically against a Test/Staging environment (TBD). A passing E2E suite is mandatory for a release to proceed.

### 4. Smoke Tests

-   **Purpose**: To perform a quick, critical-path validation on the production environment immediately after a deployment to ensure core functionality is working.
-   **Responsibility**: The engineering team is collectively responsible for maintaining the smoke test suite.
-   **Framework**: Playwright
-   **Execution**: Run automatically against the **Production** environment as part of the post-deployment process.
