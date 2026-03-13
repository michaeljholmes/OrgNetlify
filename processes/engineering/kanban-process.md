# Engineering Team Kanban Process

This document outlines the Kanban methodology adopted by the engineering team to manage workflow, improve efficiency, and ensure a continuous delivery of value.

## Core Principles

1.  **Visualize the Workflow**: We use a Kanban board to make all work items visible, providing transparency on who is working on what.
2.  **Limit Work-In-Progress (WIP)**: We set explicit limits on how many items can be in progress at any given stage. This prevents bottlenecks and improves focus.
3.  **Manage Flow**: We measure and optimize the flow of work through the system, aiming to reduce the time it takes for a task to move from 'To Do' to 'Done'.
4.  **Make Policies Explicit**: All our processes, from how we prioritize work to our 'Definition of Done', are clearly defined and visible to everyone.
5.  **Implement Feedback Loops**: We use regular meetings and reviews (such as our **Design Reviews**, **Show-and-Tells**, and **Retrospectives**) to inspect and adapt our process.

## Kanban Board Structure

Our board is designed to mirror our staggered development workflow. Each column has a Work-In-Progress (WIP) limit to ensure a smooth flow.

| Column | Description | Suggested WIP Limit |
| --- | --- | --- |
| **Backlog** | A prioritized list of all upcoming features, bugs, and technical debt. Managed by the Product Owner. | N/A |
| **To Do** | Work items that have been committed to and are ready to be started. | 5 |
| **BE Development** | Backend implementation is in progress. | 3 |
| **BE Review** | A pull request has been created and is awaiting review from another BE engineer. | 2 |
| **Ready for FE** | BE work is complete, merged, and deployed to a development/staging environment. The GraphQL service is updated. | N/A (Buffer column) |
| **FE Development** | Frontend implementation and integration are in progress. | 3 |
| **FE Review** | A pull request has been created and is awaiting review (includes Design Review). | 2 |
| **Ready for UAT** | The feature is fully integrated and ready for functional and user experience verification. | N/A (Buffer column) |
| **UAT / E2E Testing** | The feature is being actively reviewed by the BA and UI/UX team. E2E tests are running. | 3 |
| **Done** | The feature has been signed off and is ready to be included in the next release. | N/A |

## Handling Different Work Types

-   **Features**: Follow the standard flow from left to right across the board.
-   **Bugs/Incidents**: Critical production bugs (P1/P2) can be expedited. They are placed at the top of the 'To Do' column and are picked up as soon as a team member has capacity, respecting WIP limits.

## Meetings & Ceremonies

While Kanban is less prescriptive than Scrum, we will adopt the following meetings to ensure alignment and continuous improvement.

-   **Daily Stand-up** (15 mins, daily)
    -   Focus on the flow of work. Team members walk the board from right to left, discussing blocked items and what's needed to move tasks to the next column.

-   **Backlog Refinement** (Continous)
    -   The Product Owner, BA, and engineering leads review and prioritize the backlog. Upcoming work is discussed to ensure it's ready to be pulled into 'To Do'.

-   **Retrospective** (1 hour, bi-weekly)
    -   A review of the team's workflow and effectiveness. We analyze our metrics (e.g., lead time, cycle time) and discuss what went well, what didn't, and what we can improve.

-   **Release Planning** (30 mins, TBD)
    -   When a sufficient number of features have reached the 'Done' column, a meeting is held to coordinate the release process.
