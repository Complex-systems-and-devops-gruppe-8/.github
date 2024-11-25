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
### 1. Introduction

#### Project Scope and Objectives

#### Problem Statement and Solution Overview

#### Methodology


## I. Analysis

### 2. Domain Analysis

#### User Stories and Requirements

#### System Architecture Overview

#### Technical Stack Selection

#### Security Requirements

### 3. Technical Foundation

#### Framework Selection Rationale

#### Development Environment Setup

#### Project Structure

## II. Implementation and DevOps Practices

### 4. Backend Development

#### Quarkus Framework Implementation

#### REST API Design with Siren Hypermedia

#### Database Integration

#### Business Logic Implementation

#### Security Implementation

##### JWT Authentication

##### Backend Security Measures

#### Testing Strategy

##### JUnit Implementation

##### REST-assured Testing

#### OpenAPI Documentation

### 5. Frontend Development

#### React Application Structure

#### TypeScript Integration

#### Vite Build Tool Implementation

#### State Management

#### Component Architecture

#### Security Features

##### Token Security Implementation

#### Package Management

### 6. DevOps Implementation

#### Version Control Practices

##### Git Workflow

##### GitHub Integration

#### Continuous Integration/Continuous Deployment

##### GitHub Actions Configuration

##### Build Server Setup

##### Testing Pipeline

#### Containerization
Containerization is a **lightweight form of virtualization** that packages an application and its dependencies into a single, portable unit called a **container**. This approach allows applications to run consistently across various environments, from development to production, without being affected by differences in underlying infrastructure.

##### Docker Implementation
**Docker** is used to host and build the final application that **Quarkus** builds, both for local development and cloud deployment. This approach ensures that the **production environment** closely resembles the **development environment**, minimizing discrepancies and potential issues.

By using Docker, we can create a **consistent** and **isolated environment** for our application, which simplifies the deployment process and enhances reliability across different stages of the softwares lifecycle.

##### Container Registry
For hosting the Docker container in the cloud, we utilize **Google Cloud's Artifact Registry**. This service provides a **centralized location** for storing and managing build artifacts and dependencies, which is crucial for maintaining a streamlined and integrated development workflow.

Given that our final deployment is hosted on **Google Cloud Run**, using Artifact Registry aligns perfectly with our infrastructure, ensuring **seamless integration** and **efficient management** of our container images.

#### Cloud Deployment
Cloud deployment involves hosting applications and services on cloud infrastructure, allowing for scalable, flexible, and efficient resource management. By leveraging cloud platforms, organizations can deploy applications across global data centers, ensuring high availability and performance. This approach reduces the need for on-premises hardware, enabling teams to focus on development and innovation rather than infrastructure management.

##### Google Cloud Setup
As mentioned in the Container Registry chapter, the deployment of the backend is hosted on the **Google Cloud Platform (GCP)**. Why did we chose Google Cloud over Microsoft Azure, especially since DTU provides students with an Azure subscription. Initially, we attempted to set up our cloud infrastructure on Azure but quickly encountered authentication issues when integrating our GitHub Actions workflows.

A runner/account in Azure's IAM is required, but creating one requires access to Microsoft Entra ID, formerly known as Azure Active Directory, which students don't have. Instead of dealing with this complexity and risking losing access after further development, we decided to use Google Cloud, which offers us full control over the entire cloud environment.

In our cloud setup, we have the following elements:
- An **SQL instance** to host our SQL database.
- **Container/Artifact Registry** to host our Docker images.
- **Cloud Run** to deploy our images and expose them to the web.
- **Identity and Access Management (IAM)** to create principals and service accounts with the proper access levels, ensuring we adhere to best practices for cybersecurity.
- **Secret Manager**: To ensure that no API keys or credentials are leaked, we use Secret Manager. Since our deployment is through GitHub, we have decided to store our secrets as repository secrets. This approach keeps them as close as possible to where they are needed, enhancing security and accessibility.

In summary, choosing Google Cloud Platform for our backend deployment has provided us with greater control and integration capabilities, overcoming the limitations we faced with Azure. This setup ensures a secure and scalable environment, supporting our development and deployment needs effectively.

##### Netlify Frontend Deployment

#### Monitoring and Maintenance

### 7. Conclusion

#### Project Outcomes

#### Future Improvements

#### Lessons Learned

