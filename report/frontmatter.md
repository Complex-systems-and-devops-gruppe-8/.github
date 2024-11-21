# Complex Systems and DevOps: Deliverable 2

**Date:** November 25, 2024

---

### Course Details

**Course Name:** Complex Systems and DevOps
**Course Code:** 62582
**Semester:** Fall 2024

---

### Team Members

| Name                            | Student Number |
|---------------------------------|----------------|
| **Christoffer Fink**            | *s205449*      |
| **Kasper Falch Skov**           | *s205429*      |
| **Johan Søgaard Jørgensen**     | *s224324*      |
| **Henrik Lynggaard Skindhøj**   | *s205464*      |
| **Kevin Wang Højgaard**         | *s195166*      |
| **Sebastian Halfdan Lauridsen** | *s215769*      |

[**Link to GitHub Project**](https://github.com/Complex-systems-and-devops-gruppe-8)

---

### Table of Contents

1. [Introduction](#introduction)
   - [Project Scope and Objectives](#project-scope-and-objectives)
   - [Problem Statement and Solution Overview](#problem-statement-and-solution-overview)
   - [Methodology](#methodology)

I. [Analysis](#analysis)

2. [Domain Analysis](#domain-analysis)
   - [User Stories and Requirements](#user-stories-and-requirements)
   - [System Architecture Overview](#system-architecture-overview)
   - [Technical Stack Selection](#technical-stack-selection)
   - [Security Requirements](#security-requirements)

3. [Technical Foundation](#technical-foundation)
   - [Framework Selection Rationale](#framework-selection-rationale)
   - [Development Environment Setup](#development-environment-setup)
   - [Project Structure](#project-structure)

II. [Implementation and DevOps Practices](#implementation-and-devops-practices)

4. [Backend Development](#backend-development)
   - [Quarkus Framework Implementation](#quarkus-framework-implementation)
   - [REST API Design with Siren Hypermedia](#rest-api-design-with-siren-hypermedia)
   - [Database Integration](#database-integration)
   - [Business Logic Implementation](#business-logic-implementation)
   - [Security Implementation](#security-implementation)
     - [JWT Authentication](#jwt-authentication)
     - [Backend Security Measures](#backend-security-measures)
   - [Testing Strategy](#testing-strategy)
     - [JUnit Implementation](#junit-implementation)
     - [REST-assured Testing](#rest-assured-testing)
   - [OpenAPI Documentation](#openapi-documentation)

5. [Frontend Development](#frontend-development)
   - [React Application Structure](#react-application-structure)
   - [TypeScript Integration](#typescript-integration)
   - [Vite Build Tool Implementation](#vite-build-tool-implementation)
   - [State Management](#state-management)
   - [Component Architecture](#component-architecture)
   - [Security Features](#security-features)
     - [Token Security Implementation](#token-security-implementation)
   - [Package Management](#package-management)

6. [DevOps Implementation](#devops-implementation)
   - [Version Control Practices](#version-control-practices)
     - [Git Workflow](#git-workflow)
     - [GitHub Integration](#github-integration)
   - [Continuous Integration/Continuous Deployment](#continuous-integrationcontinuous-deployment)
     - [GitHub Actions Configuration](#github-actions-configuration)
     - [Build Server Setup](#build-server-setup)
     - [Testing Pipeline](#testing-pipeline)
   - [Containerization](#containerization)
     - [Docker Implementation](#docker-implementation)
     - [Container Registry](#container-registry)
   - [Cloud Deployment](#cloud-deployment)
     - [Google Cloud Setup](#google-cloud-setup)
     - [Netlify Frontend Deployment](#netlify-frontend-deployment)
   - [Monitoring and Maintenance](#monitoring-and-maintenance)

7. [Conclusion](#conclusion)
   - [Project Outcomes](#project-outcomes)
   - [Future Improvements](#future-improvements)
   - [Lessons Learned](#lessons-learned)

---
