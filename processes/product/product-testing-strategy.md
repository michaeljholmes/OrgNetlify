# Product & UAT Testing Strategy

## Philosophy: A Shared Responsibility for Quality

While engineering owns build quality and automated validation, the Product and Support teams play a critical role in ensuring we ship the *right* thing. Our QA process from Product aims to:
-   **Validate business value**: Confirm that features meet the specified requirements and solve the intended user problem.
-   **Incorporate real-world scenarios**: Leverage the Support team's deep understanding of customer usage by having them aid with User Acceptance Testing (UAT).
-   **Shorten feedback loops**: Involve Product and Support earlier in the process to ensure we are aligned and building a high-quality product from every angle.

This document outlines the manual testing strategy that supports this collaborative approach.

## Guiding Principles

-   **User-Centric Focus**: Our manual testing is focused on the user's perspective, verifying workflows and user journeys.
-   **Business Requirement Validation**: The primary goal is to confirm that the software delivers the value defined in the user stories and acceptance criteria.
-   **Collaboration with Engineering**: Testing is a collaborative effort. Feedback and bugs are communicated clearly and constructively to the engineering team.

## Testing Phases & Responsibilities

### 1. Feature Verification

-   **Purpose**: To perform an initial check of a new feature to ensure it functions as designed.
-   **Owner**: The **Product Owner** and/or **Business Analyst (BA)** responsible for the feature.
-   **When**: This occurs when a feature is moved to the 'Ready for UAT' column on the Kanban board and deployed to the staging environment (TBD).
-   **Process**:
    1.  The Product Owner/BA tests the feature against the acceptance criteria defined.
    2.  The focus is on the 'happy path' and key alternative scenarios.
    3.  Any bugs or discrepancies are logged as new tickets, following the `pre-production-incident-process.md`.

### 2. User Acceptance Testing (UAT)

-   **Purpose**: To conduct a broader, more exploratory round of testing that simulates real-world usage. This is the final sign-off before a feature is approved for release.
-   **Owners**: The **Support Team**, with guidance from the Product Owner.
-   **When**: After the initial Feature Verification is complete.
-   **Process**:
    1.  The Product Owner provides the Support Team with a brief overview of the new features ready for testing.
    2.  The Support Team tests the features from a user's perspective, trying different workflows and edge cases they commonly encounter when assisting customers.
    3.  This phase is critical for catching issues related to usability and real-world application.
    4.  All bugs are logged following the `pre-production-incident-process.md`.

### 3. Sign-Off

-   **Purpose**: To formally approve a feature for release.
-   **Owner**: The **Product Owner**.
-   **Process**:
    1.  Once Feature Verification and UAT are complete and any critical or high-priority bugs have been resolved, the Product Owner provides the final sign-off.
    2.  This sign-off confirms that product and user acceptance testing is complete, allowing the release process defined in `release-management.md` to proceed.
