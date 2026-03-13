# Engineering Workflow

This document outlines the standard process for engineering work, from feature refinement through to delivery. It covers our core principles and the collaborative process between Frontend (FE) and Backend (BE) teams.

## Core Engineering Principles

- **Accountability**: The Engineering Team is accountable for delivering to agreed requirements and acceptance criteria and for defects introduced by their changes.
- **Quality**: The Engineering Team implements sufficient automated tests (unit, integration, contract, E2E as appropriate) to prevent regressions.
- **Continuous Improvement**: Recurring defects or regressions in the same area after delivery must result in corrective engineering actions (e.g., test coverage improvements, root-cause fixes, and/or refactoring).

## 1. Feature Kick-off & Work Breakdown

- **Participants**: Team Leaders, Senior FE Engineer, Senior BE Engineer, BA, and UI/UX.
- **Goal**: To achieve a shared understanding of the feature, clarify requirements, and identify dependencies.
- **Assumption**: This process begins after the lower-level requirements have been reviewed by the team and the work is deemed ready to begin.

### Process:
1.  **Initial Review**: The senior engineers review the low-level requirements from the Product team.
2.  **Technical Breakdown Session**: A meeting is held to:
    -   Decompose the feature into smaller, manageable tasks for both FE and BE.
    -   Identify required API endpoints and GraphQL operations (queries, mutations).
    -   For GraphQL, map out the required data graph; this will form the basis of the contract.
    -   Discuss potential complexities, risks, and edge cases.
    -   Identify if any **spikes** are required to investigate technical unknowns before committing to an approach.
    -   Create initial tickets for the identified tasks.

## 2. API Contract Definition

- **Owner**: The Backend team is responsible for building underlying endpoints and updating the GraphQL service.
- **Goal**: To establish a clear, agreed-upon GraphQL schema that serves as the contract for the Frontend team.

### Process:
1.  **Contract Definition**: Based on the technical breakdown, the BE team updates the GraphQL schema with the necessary types, queries, and mutations. This schema is the primary source of truth and the contract for the FE team.
2.  **Review & Agreement**:
    -   The proposed contract (GraphQL schema) is shared with the FE team for review, typically via a pull request.
    -   The FE team provides feedback to ensure the contract meets UI requirements and is efficient to consume.
    -   Both teams iterate on the contract until a final agreement is reached.
3.  **Contract Finalization**: Once merged, the contract is considered final. The agreed schema becomes part of the official documentation and is stored in the documentation repository. It is used to generate mock servers for the FE and guide implementation for the BE. Any subsequent changes must be communicated and agreed upon via the same review process.

## 3. Staggered Development & Testing

- **Goal**: To have Backend development slightly lead Frontend development, allowing FE to build components and prepare tests while BE work is in progress.

### Process:
1.  **BE Implementation**: The BE team builds the underlying data-source APIs and implements the GraphQL resolvers. Once complete, the service is deployed to a development environment.
2.  **FE Component & Test Preparation**: While the BE implementation is in progress, the FE team builds out the required UI components based on the agreed designs and prepares the testing suite.
    -   This includes writing contract tests against the agreed GraphQL schema, which may involve mocking the schema.

## 4. Integration, Testing & Handoff

- **Goal**: To ensure the FE and BE components work together seamlessly and meet the feature requirements.

### Process:
1.  **Integration**: Once the GraphQL service is deployed to a shared development or staging environment, the FE team integrates the live service into the components.
2.  **E2E Testing**: Both teams collaborate on E2E testing to identify and fix any issues at the boundary between the FE and BE.
3.  **QA & Validation**: The completed feature is handed over to the Product team and/or QA for validation against the acceptance criteria.
4.  **Release**: Once validated, the feature is scheduled for release according to the standard release process.
