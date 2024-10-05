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
## Pipeline Stages
**Checkout Code:** Pull the latest version of the code from the GitHub repository.
**Build Docker Image:** Use the Dockerfile to build the image of the web app.
**Push to Docker Hub:** The built image is pushed to Docker Hub.
**Run Container (Optional):** Run the built Docker container in a test or production environment.
## How to Run the Project
 **Prerequisites**
Jenkins installed with Docker integration.
A Docker Hub account.
GitHub repository set up with a Jenkinsfile for pipeline configuration.
## Steps
**Clone the repository:**
git clone https://github.com/shyam-30/my-web-app.git
**cd my-web-app**
**Build and run Docker image:**
docker build -t shyam30/my-web-app .
docker run -p 3000:3000 shyam30/my-web-app
**Push the Docker image to Docker Hub:**
**docker login**
docker push shyam30/my-web-app
**Configure Jenkins:**
Set up Jenkins with a pipeline to trigger the build and push on new commits.

## Credentials Handling
Docker Hub credentials are securely stored in Jenkins credentials and accessed using withCredentials to prevent exposing sensitive information.
## Future Enhancements
 We can add  automated deployment to AWS ECS or Kubernetes.
