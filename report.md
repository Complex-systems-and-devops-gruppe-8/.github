# Complex System and DevOps project report

## Table of Contents

- [Complex System and DevOps project report](#complex-system-and-devops-project-report)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
    - [Background](#background)
    - [Purpose](#purpose)
    - [Scope](#scope)
  - [Analysis](#analysis)
    - [Requirements](#requirements)
    - [Challenges](#challenges)
  - [Design](#design)
    - [Architecture](#architecture)
    - [Design Decisions](#design-decisions)
  - [Implementation](#implementation)
    - [Technologies Used](#technologies-used)
    - [Code Structure](#code-structure)
  - [Test](#test)
    - [Test Plan](#test-plan)
    - [Results](#results)
  - [Conclusion](#conclusion)
    - [Summary](#summary)
    - [Future Work](#future-work)

---

## Introduction

### Background
[Brief overview of the project background.]

### Purpose
[State the purpose of the project.]

### Scope
[Define the scope of the document or project.]

## Analysis

### Requirements
[List the functional and non-functional requirements.]

### Challenges
[Highlight the challenges encountered during analysis.]

## Design

### Architecture
[Overview of the system architecture.]

### Design Decisions
[Discuss key design decisions and their rationale.]

## Implementation

### Technologies Used
[List the technologies and tools used.]

### Code Structure
[Provide an overview of the code organization and structure.]

## Test

### Test Plan
This test plan descripes our current idea of the approach, tools and strategies we are going to be using to ensure the quality and stability of the full-stack application developed using the specified tech stack in this repport for the front and backend. 
#### Testing opbjectives
- Ensure application functions correctly across all integrated systems (backend, frontend, database)
- Validate application security features particularly token mangement and authorization (OIDC)
- Verify the frontend provides a seamless user experience with state management and responsive design
- Ensure CI/CD pipelin (Github Actions) operates effectiveely, catching bugs early in the build process

#### Test types and strategies
 -  Unit testing (Backend & frontend) 
    - Each backend service (Api endpoints, business logic, token management) will be tested individually
    - Frontend components and utility functions will be tested for correctness using unit testing frameworks like Jest and React Testing Library.

 - Integration testing
    - Ensure the backend interacts correctly with the PostgreSQL database for CRUD operations.
    - Verify that the frontend correctly communicates with backend REST APIs


 - End-to-end (E2E) testing
    - Using Cypress or playwright we are able to simulate real user interactions with the app for testing
    - We will test critical flows such as authentication, CRUD operations and state management scenarios

 - Security testing
    - The security tests validate access control through Quarkus’s token-based authentication mechanism (OIDC).
    - Public endpoints (/all) are tested to ensure they are accessible without authentication.
    - Protected endpoints (/admin, /user) are restricted based on roles, ensuring that:
        - Admin users have access to both /admin and /all, but are restricted from user-specific resources.
        - User accounts have access to /user and proper identity checks are performed (e.g., user-specific greetings).
    - Tests ensure that unauthorized access attempts are met with appropriate error codes (401 Unauthorized, 403 Forbidden).

 - Performance Testing
    - To evalute frontend performance we will be using Lighthouse to ensure optimal load times and responsiveness
#### Enviroment setup for testing
- Local development
  - Tests are run in both the backend and frontend during local development and building to ensure  the application functions correctly across the full stack.
  - Backend tests include unit and integration tests, while frontend tests focus on component and UI logic validation.
  - Developers can run the tests continuously as they work on the application, ensuring immediate feedback and preventing integration issues before code is pushed to the repository.
- CI/CD (Github Actions)
    - Each commit triggers automated test runs. Both unit and integration tests are part of the CI pipeline, ensuring no broken code is deployed.
    - Upon successful test completion, the build will proceed, else rollbacks or alerts are triggered.


 

### Results
At this stage of the project not all test are setup so not many results have been found. But the result of the implemented test help us understand and identify current problems and validate that our new implementations are correct implemented.
 

## Conclusion

### Summary
[Summarize the main points of the project.]

### Future Work
[Mention any potential future improvements or follow-up work.]
