# Pipeline-4

Task Service CI/CD Pipeline
This repository contains the source code for a task service and a Jenkins pipeline configuration for building, testing, and deploying the application using Docker.

**Overview**
   * The included Jenkinsfile defines a continuous integration and delivery (CI/CD) pipeline for the task service. The pipeline * 
    
      --Checks out the code from the main branch.
      
      --Builds the project using Maven.
      
      --Runs unit tests and archives test reports.
      
      --Builds a Docker image tagged with the build number.
      
      --Pushes the image to Docker Hub.
      
      --Deploys the service to a development environment (only on the main branch).
      
      --Sends Slack notifications on build success or failure.
     
  **Prerequisites**

  --Jenkins server with Pipeline plugin installed.
  
  --Git for source code management.
  
  --Maven for building the Java project.
  
  --Docker for building and running container images.
  
  --Docker Hub credentials stored as a Jenkins credential (docker-hub-creds).


 **Pipeline Stages**

   <img width="744" alt="Screenshot 2025-06-11 at 00 51 54" src="https://github.com/user-attachments/assets/d0696fce-c24f-438c-bbc3-264c79426ba8" />


  **Configuration**
    Environment Variables

      DOCKER_HUB_CREDENTIALS: Jenkins credential for Docker Hub.
      
      DOCKER_IMAGE: Your Docker Hub username and image name.
      
      VERSION: Set to the Jenkins build number.

  Repository URL

      Update the git step in the pipeline to match your repository URL.

  Docker Image

      Replace your-dockerhub-username with your actual Docker Hub username.

**Usage**

1.Clone the repository

  ```bash
git clone https://github.com/your-username/task-service.git
```

2.Push changes to the main branch to trigger the pipeline.

3.Jenkins will automatically execute the pipeline stages as defined in the Jenkinsfile.




