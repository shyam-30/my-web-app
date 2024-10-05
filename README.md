## My-Web-App CI/CD Pipeline

### Project Overview
This project demonstrates a CI/CD pipeline using **Jenkins**, **Docker**, and **AWS**. The pipeline is designed to build, test, and deploy a web application. The key steps include:

- Building a Docker image for a simple web application.
- Pushing the Docker image to **Docker Hub**.
- Optionally, deploying the image to a container platform like **AWS ECS** or **Kubernetes (K8s)**.

### Tools Required
- **Jenkins**: Automation server for continuous integration and delivery.
- **Docker**: To containerize the application.
- **AWS**: For hosting the application or storing the Docker image on ECR.
- **GitHub**: Source code version control and repository hosting.

### Features
- Automated pipeline triggered on new commits to the GitHub repository.
- Docker image build and push to Docker Hub.
- Secure handling of credentials using **Jenkins credentials**.
