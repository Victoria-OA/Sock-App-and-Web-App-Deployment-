# Sock-App-and-Web-App-Deployment

This repository contains the configurations and resources for deploying a Sock Shop microservices application, a web application, and managing the deployment workflow using Terraform, CircleCI, and Kubernetes.
### Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Deployment Workflow](#deployment-workflow)
- [Terraform Configuration](#terraform-configuration)
- [CircleCI Configuration](#circleci-configuration)
- [Kubernetes Configuration](#kubernetes-configuration)
- [Conclusion](#conclusion)

### Overview
The repository provides a comprehensive setup for deploying and managing applications using Terraform for infrastructure provisioning, CircleCI for continuous integration and deployment, and Kubernetes for container orchestration. The deployment includes a Sock Shop microservices application, a web application, and the necessary infrastructure components.

### Requirements
To use the deployment workflow and configurations provided in this repository, ensure you have the following prerequisites:

    Access to an AWS account with the necessary permissions to create resources like EKS clusters and IAM roles.
    Installed Docker on your local machine for building container images.
3.     Installed kubectl for interacting with the Kubernetes cluster.
4.     Access to a Docker Hub account for pushing Docker images.

### Deployment Workflow
The deployment workflow in this repository follows the steps below:

1.     Terraform Initial: Initializes the Terraform configuration and provisions the initial infrastructure.
2.     Terraform Planning: Performs a Terraform plan to preview the changes before applying them.
3.     Hold Apply: A manual approval step to review the Terraform plan and approve the changes.
4.     Terraform Applying: Applies the Terraform plan to create or update the infrastructure.
5.     Terraform Stop: Stops the infrastructure by creating a destroy plan.
6.     Hold Destroy: A manual approval step to review the destroy plan and approve the destruction of resources.
7.     Terraform Destroy: Destroys the infrastructure based on the approved destroy plan.
8.     Build Blog App: Builds the Docker image for the blog application.
9.     Deploy Blog App: Deploys the blog application to the Kubernetes cluster.
10.     Deploy Sock Shop: Deploys the Sock Shop microservices application to the Kubernetes cluster.
11.     Deploy Prometheus: Deploys Prometheus monitoring to the Kubernetes cluster.

Each step in the workflow is designed to be modular and can be run independently or in sequence as needed.
### Terraform Configuration
The Terraform configuration in this repository is used to provision the required AWS infrastructure, including VPC, EKS cluster, and IAM roles. The configuration is modular and can be extended to include additional resources as needed.

### CircleCI Configuration
The CircleCI configuration in this repository defines the CI/CD pipeline for building, testing, and deploying the applications. It includes steps for installing the AWS CLI, Terraform, and kubectl, as well as building and pushing Docker images.

### Kubernetes Configuration
The Kubernetes configuration in this repository includes deployment manifests for deploying the applications to the Kubernetes cluster. It includes deployment and service definitions for the applications, as well as any required configuration for other Kubernetes resources.

### Conclusion
By using the configurations and workflow provided in this repository, you can set up a robust deployment process for your applications using Terraform, CircleCI, and Kubernetes. This setup enables you to automate the deployment and management of your applications, making your development and deployment processes more efficient and reliable.
