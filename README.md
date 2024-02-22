# This repository focuses on setting up a CI/CD pipeline using Jenkins, Docker,Kubernetes (K8s), and Helm. The goal is to automate the deployment process for applications within a K8s cluster. Below are the key components and steps:

# Key Components:

- Jenkins:
The continuous integration and continuous deployment (CI/CD) server.
Jenkins jobs are configured to build, test, and deploy applications.

- Docker:
Used for containerization of application code.
Docker images are created for the application.

- Kubernetes (K8s):
The container orchestration platform.
K8s manifests define how the application should be deployed.

- Git:
Version control system for managing code changes.

- Workflow:
-- Developers commit code to the Git repository.
-- Jenkins triggers a pipeline script upon code changes.
-- The pipeline performs the following steps:
 - Builds the application code.
 - Creates a Docker image.
 - Pushes the Docker image to a registry (e.g., Docker Hub).
 - Deploys the Dockerized application to a K8s cluster.

- Helm Folder:
The Helm folder contains Helm charts for managing K8s deployments. Helm simplifies the process of defining, installing, and upgrading applications in K8s. Within the Helm folder, you’ll find charts for different services or components of your application.

# Setup Instructions:
- Create a K8s Cluster using KOPS:
- Set up an Ubuntu EC2 instance.
- Install AWS CLI and KOPS.
- Create an IAM role with necessary permissions.
- Create an S3 bucket for K8s cluster data storage.
- Configure Jenkins:
- Install Jenkins on a separate server.
- Set up Jenkins jobs to build, test, and deploy applications.
- Integrate Jenkins with Git repositories.
- Dockerize Applications:
- Write Dockerfiles for your applications.
- Build Docker images.
- Push images to a Docker registry.
- Deploy to K8s using Helm:
- Define Helm charts for your services.
- Use Helm to install and manage your application components.


