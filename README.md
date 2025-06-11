# Task Service CI/CD Pipeline

This repository contains the source code for a task service and a Jenkins pipeline configuration for building, testing, and deploying the application using Docker.

## Overview

The included `Jenkinsfile` defines a continuous integration and delivery (CI/CD) pipeline for the task service. The pipeline:

- **Checks out the code from the main branch**
- **Builds the project using Maven**
- **Runs unit tests and archives test reports**
- **Builds a Docker image tagged with the build number**
- **Pushes the image to Docker Hub**
- **Deploys the service to a development environment (only on the main branch)**
- **Sends Slack notifications on build success or failure**

## Prerequisites

- **Jenkins server** with Pipeline plugin installed
- **Git** for source code management
- **Maven** for building the Java project
- **Docker** for building and running container images
- **Docker Hub credentials** stored as a Jenkins credential (`docker-hub-creds`)
- **Slack Notification plugin** installed and configured in Jenkins (for Slack notifications)

## Pipeline Stages

| Stage            | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| Checkout         | Clones the repository from the main branch                                  |
| Build            | Builds the project with Maven and archives the JAR file                     |
| Unit Tests       | Runs unit tests and archives test reports                                   |
| Docker Build     | Builds a Docker image tagged with the Jenkins build number                  |
| Docker Push      | Pushes the Docker image to Docker Hub (also pushes the `latest` tag)        |
| Deploy to Dev    | Deploys the service to a development environment (only on the main branch)  |

## Configuration

**Environment Variables**

- **DOCKER_HUB_CREDENTIALS:** Jenkins credential for Docker Hub
- **DOCKER_IMAGE:** Your Docker Hub username and image name (e.g., `your-dockerhub-username/task-service`)
- **VERSION:** Set to the Jenkins build number

**Repository URL**

Update the `git` step in the pipeline to match your repository URL.

**Docker Image**

Replace `your-dockerhub-username` with your actual Docker Hub username.

## Usage

1. **Clone the repository**
git clone https://github.com/your-username/task-service.git

2. **Push changes to the main branch to trigger the pipeline.**
3. **Jenkins will automatically execute the pipeline stages as defined in the Jenkinsfile.**

## Troubleshooting

- **Docker Hub credential issues:** Verify the credential ID in Jenkins matches the one used in the pipeline.
- **Failed builds:** Check the Jenkins build logs for detailed error messages.
- **Slack notifications not working:** Confirm the Slack Notification plugin is installed and configured correctly.

## Contributing

Feel free to submit pull requests or report issues.

---
![WhatsApp Image 2025-06-11 at 19 27 53](https://github.com/user-attachments/assets/80929f49-6e99-483b-b991-dd107220c6c0)
![WhatsApp Image 2025-06-11 at 19 28 31](https://github.com/user-attachments/assets/27694b47-cdc2-4726-91f5-449acb51d11a)
![WhatsApp Image 2025-06-11 at 19 29 32](https://github.com/user-attachments/assets/b6d88ac2-cc9c-4465-886c-b1139d5f5d56)
![WhatsApp Image 2025-06-11 at 19 29 50](https://github.com/user-attachments/assets/a13879a4-4895-4ce7-b249-eaab9ec31f6a)



License MIT © AKASH M
