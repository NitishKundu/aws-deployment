# Deploying End-to-End ML Projects in Production on AWS Cloud using CI/CD Pipeline

![pngwing com (2)](https://github.com/NitishKundu/aws-deployment/assets/79974360/2e4f8c6d-94e2-4464-aacd-a9e4e10322ba)

This repository provides a step-by-step guide on deploying an end-to-end Machine Learning (ML) project in a production environment on the AWS Cloud. The deployment process is automated using a Continuous Integration and Continuous Deployment (CI/CD) pipeline, and the code is deployed on an EC2 instance using GitHub Actions. The deployment is containerized using Docker and the ECR (Elastic Container Registry) service, leveraging GitHub Runners for workflow execution.

## Overview

In this project, we aim to deploy a complete ML solution in a scalable and automated way on AWS. The project includes the following key components:

1. ML Model: Develop and train the ML model using the appropriate libraries and frameworks (e.g. scikit-learn).

2. Data Preprocessing: Implement data preprocessing steps to clean and transform raw data for the ML model.

3. AWS Cloud Setup: Configure AWS resources such as EC2 instance, ECR repository, S3 bucket, and IAM roles for deployment.

4. CI/CD Pipeline: Set up a CI/CD pipeline using GitHub Actions to automate the deployment process.

5. Docker Containerization: Containerize the ML model and application using Docker.

6. Deployment on EC2: Deploy the Docker container on an EC2 instance to handle incoming requests.

## Deployment Steps

1. Clone the Repository: Clone this repository to your local development environment.

2. Train and Test the ML Model: Develop and test the ML model on your local machine. Make sure the model meets the desired performance metrics.

3. Data Preprocessing: Implement data preprocessing scripts to clean and prepare the data for deployment.

4. AWS Cloud Setup: Create an AWS account if you don't have one already. Set up an EC2 instance with the necessary configurations, create an ECR repository to store Docker images, an S3 bucket to store data and models, and define IAM roles for proper permissions.

5. Configure AWS Credentials: Set up AWS credentials on your local machine and securely store them for GitHub Actions to use during the deployment process.

6. Dockerize the Application: Create a Dockerfile to package the ML model and application into a Docker container.

7. CI/CD Pipeline: Define the CI/CD pipeline using GitHub Actions. This pipeline will trigger automatic deployments whenever code changes are pushed to the main branch.

8. Deploy using Docker and ECR: Implement the necessary scripts and configurations to build the Docker image, push it to the ECR repository, and deploy it on the EC2 instance using GitHub Actions.

## Getting Started

To get started with deploying the ML project on AWS Cloud using Docker, ECR, EC2, and GitHub Actions, follow these steps:

1. Install Dependencies: Ensure you have the necessary dependencies installed, such as Python, Docker, AWS CLI, and other required libraries.

2. Clone this Repository: Use the following command to clone this repository to your local machine:

```
git clone https://github.com/your-username/your-repo.git
```

3. Set Up AWS Account: Create an AWS account and configure the AWS CLI on your local machine.

4. Train the Model: Develop and train your ML model on your local machine. Save the trained model and other artifacts to the appropriate directories in this repository.

5. Configure CI/CD Pipeline: Modify the `.github/workflows/main.yml` file to suit your project requirements and set up the necessary environment variables for AWS credentials.

6. Build and Deploy using Docker: Create a Dockerfile and push the Docker image to the ECR repository. Set up the deployment scripts on the EC2 instance using GitHub Actions.

7. Test the Pipeline: Push changes to the main branch and verify that the CI/CD pipeline triggers the deployment process successfully.

8. Monitor the Deployment: Monitor the EC2 instance and other AWS resources to ensure the ML model is functioning correctly in the production environment.

## Important
1. Docker Build
2. Github Workflow
3. Iam User In AWS

### Docker Setup In EC2 commands to be Executed
1. sudo apt-get update -y
2. sudo apt-get upgrade
3. curl -fsSL https://get.docker.com -o get-docker.sh
4. sudo sh get-docker.sh
5. sudo usermod -aG docker ubuntu
6. newgrp docker

### Configure EC2 as self-hosted runner:

### Setup github secrets:
1. AWS_ACCESS_KEY_ID
2. AWS_SECRET_ACCESS_KEY
3. AWS_REGION
4. AWS_ECR_LOGIN_URI
5. ECR_REPOSITORY_NAME

## Deployment Snapshot

![Deployment Screenshot](https://github.com/NitishKundu/aws-deployment/assets/79974360/20960c50-9c79-4272-90da-2bddc28ff6b5)

## Notes

- Keep your AWS credentials and sensitive information secure and avoid pushing them to the repository.

- Regularly update the dependencies and monitor security vulnerabilities to maintain a robust and secure deployment.

- Feel free to customize the project to suit your specific ML model and deployment needs.

For any questions or issues, please reach out to nitishkundu1993@gmail.com.

Happy Deploying! 🚀
