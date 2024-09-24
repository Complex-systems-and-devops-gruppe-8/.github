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

### Frontend Development

The frontend of the project is developed using **React**, which is a JavaScript library used for building user interfaces. React uses a component-based architecture, which facilitates breaking down the UI into small reusable components. All these components have their own logic and rendering characteristics, which is useful for keeping a codebase clean and maintainable.

#### Routing

In the frontend, we utilize **React Router** for the routing of the application. This allows the user to navigate between different pages without doing a full page reload. This is done by wrapping a `Router` tag around different `Route` tags and specifying what component should be rendered if the user navigates to said routes.

```react
<Router>
  <Routes>
    <Route path="/" element={<LandingPage />} />
    <Route path="/coinflip" element={<CoinFlipPage />} />
    <Route path="/poker" element={<PokerPage />} />
    <Route path="/blackjack" element={<BlackjackPage />} />
  </Routes>
</Router>

```

#### Component Structure

Our component structure so far is such that each page in the application is built as a separate component. This means that we have four different page components:

- **LandingPage**: The first page of the application that the user will see.
- **PokerPage**: A page for the poker game.
- **CoinflipPage**: A page for the coin flip game.
- **BlackjackPage**: A page for the blackjack game.

These components are just empty at this point, but functionality will be developed further as the project progresses.

#### TypeScript Integration

The frontend is also built using **TypeScript**, which enables typing. This is useful to help catch errors during development rather than at runtime. TypeScript is best used by defining **interfaces** and **types** for components’ props and states. This ensures that data passed between components is structured correctly.

[EXAMPLES]

#### Styling with Tailwind CSS

For the styling of the front end, **Tailwind CSS** is used. Tailwind CSS is one of many CSS frameworks that makes it easier to style different components. One of the advantages of Tailwind is that it has built-in responsiveness, making it simple to create a layout that adapts to different screen sizes.

#### Build Tool: Vite

As for building the application, we use **Vite**. Vite is a build tool that focuses on the developer experience by enabling hot-reloading, which improves the experience for developers when working on the application.

[EXAMPLES]


## Test

### Test Plan
[Describe the testing approach and methodologies.]

### Results
[Summarize the test results and key findings.]

## Conclusion

### Summary
[Summarize the main points of the project.]

### Future Work
[Mention any potential future improvements or follow-up work.]
