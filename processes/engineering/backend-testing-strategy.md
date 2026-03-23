# Backend Engineering Testing Strategy

## Philosophy: Quality is Built-In, Not Inspected

As a team, we have shifted from relying on a separate test department to a model where quality is an engineering responsibility from the start. This means:
-   **We own our quality**: We build quality into our work, rather than having it inspected at the end.
-   **Automation is our safety net**: We invest in robust automated testing to catch regressions and enable confident deployments.
-   **We are accountable**: We are accountable for the build quality and automated validation of the features we ship.

This document outlines the automated testing strategy for the Backend team.

## Guiding Principles

-   **Developers Own Quality**: The engineer who writes the code is responsible for ensuring it is well-tested.
-   **The Testing Pyramid**: We follow the testing pyramid model, emphasizing a large base of fast, isolated unit tests and a smaller number of integration tests.
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
