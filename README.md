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
     
**  Prerequisites**

**      Jenkins server with Pipeline plugin installed.
      
      Git for source code management.
      
      Maven for building the Java project.
      
      Docker for building and running container images.
      
      Docker Hub credentials stored as a Jenkins credential (docker-hub-creds).
**
