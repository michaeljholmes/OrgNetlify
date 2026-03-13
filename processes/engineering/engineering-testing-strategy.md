# Engineering Testing Strategy

## Philosophy: Quality is Built-In, Not Inspected

As a team, we have shifted from relying on a separate test department to a model where quality is an engineering responsibility from the start. This means:
-   **We own our quality**: We build quality into our work, rather than having it inspected at the end.
-   **Automation is our safety net**: We invest in robust automated testing (unit, integration, E2E) to catch regressions and enable confident deployments.
-   **We are accountable**: We are accountable for the build quality and automated validation of the features we ship.

This document outlines the automated testing strategy and responsibilities that support this philosophy.

## Guiding Principles

-   **Developers Own Quality**: The engineer who writes the code is responsible for ensuring it is well-tested.
-   **The Testing Pyramid**: We follow the testing pyramid model, emphasizing a large base of fast, isolated unit tests, a good number of integration/contract tests, and a select few end-to-end tests.
-   **Automation is Key**: All tests must be automated and integrated into our Continuous Integration (CI) pipeline.

## Testing Layers & Responsibilities

### 1. Unit Tests

-   **Purpose**: To test individual functions, methods, or components in isolation.
-   **Responsibility**: Every developer is responsible for writing unit tests for the code they produce.
-   **Coverage Target**: We aim for a minimum of **80% code coverage** for all new code.
-   **Execution**: Run automatically on every commit in the CI pipeline.

### 2. Integration Tests

-   **Purpose**: To test the interaction between multiple components or services (e.g., interaction between a service and a database, or between two internal services).
-   **Responsibility**: Developers are responsible for writing integration tests for the features they build.
-   **Execution**: Run automatically on every commit in the CI pipeline.

### 3. Contract Tests (GraphQL)

-   **Purpose**: To verify that the GraphQL service adheres to the agreed-upon schema and that the data returned matches the expected structure. This ensures that the contract between the frontend and backend is maintained.
-   **Responsibility**: The Frontend team is primarily responsible for writing contract tests against the GraphQL schema.
-   **Execution**: Run automatically as part of the CI pipeline for the frontend application.

### 4. End-to-End (E2E) Tests (Regression/Smoke TBD)

-   **Purpose**: To simulate real user journeys through the entire application, from the UI to the database. These are our highest-level, most comprehensive tests.
-   **Responsibility**: E2E tests are a shared responsibility. The developer building a feature is responsible for adding or updating E2E tests for the critical user paths they are affecting.
-   **Framework**: Playwright
-   **Execution**: TBD. A passing E2E suite is mandatory for a release to proceed.
