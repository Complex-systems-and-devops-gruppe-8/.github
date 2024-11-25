### 6. DevOps Implementation

#### Version Control Practices

##### Git Workflow

##### GitHub Integration

#### Continuous Integration/Continuous Deployment

##### GitHub Actions Configuration

##### Build Server Setup

##### Testing Pipeline

#### Containerization

##### Docker Implementation
**Docker** is used to host and build the final application that **Quarkus** produces, both for local development and cloud deployment. This approach ensures that the **production environment** closely resembles the **development environment**, minimizing discrepancies and potential issues.

By using Docker, developers can create a **consistent** and **isolated environment** for their applications, which simplifies the deployment process and enhances reliability across different stages of the software lifecycle.

##### Container Registry
For hosting the Docker images in the cloud, we utilize **Google Cloud's Artifact Registry**. This service provides a **centralized location** for storing and managing build artifacts and dependencies, which is crucial for maintaining a streamlined and integrated development workflow.

Given that our final deployment is hosted on **Google Cloud Run**, using Artifact Registry aligns perfectly with our infrastructure, ensuring **seamless integration** and **efficient management** of our container images.

#### Cloud Deployment

##### Google Cloud Setup
As mentioned in the Container Registry chapter, the deployment of the backend is hosted on the **Google Cloud Platform (GCP)**. Why did we chose Google Cloud over Microsoft Azure, especially since DTU provides students with an Azure subscription. Initially, we attempted to set up our cloud infrastructure on Azure but quickly encountered authentication issues when integrating our GitHub Actions workflows.

A runner/account in Azure's IAM is required, but creating one requires access to Microsoft Entra ID, formerly known as Azure Active Directory, which students don't have. Instead of dealing with this complexity and risking losing access after further development, we decided to use Google Cloud, which offers us full control over the entire cloud environment.

In our cloud setup, we have the following elements:
- An **SQL instance** to host our SQL database.
- **Container/Artifact Registry** to host our Docker images.
- **Cloud Run** to deploy our images and expose them to the web.
- **Identity and Access Management (IAM)** to create principals and service accounts with the proper access levels, ensuring we adhere to best practices for cybersecurity.
- **Secret Manager**: To ensure that no API keys or credentials are leaked, we use Secret Manager. Since our deployment is through GitHub, we have decided to store our secrets as repository secrets. This approach keeps them as close as possible to where they are needed, enhancing security and accessibility.

##### Netlify Frontend Deployment

#### Monitoring and Maintenance

