##My-Web-App CI/CD Pipeline
Project Overview
This project demonstrates a CI/CD pipeline using jenkins, Docker and AWS . The pipeline is design to build , test and deploy a web application . The key steps include:
Building a docker image for a simple web application 
pushing the docker image to docker hub
optionally, we can deploy the image to a container platform like aws ecs or k8s. 

Tools Required:-
Jenkins: Automation server for continuous integration and delivery 
Docker : To containerize the application 
AWS: For hosting the application or storing the docker image on ecr . 
GitHub: Source code version control and repository hosting 

Features:
Automated pipeline triggered on new commits to the GitHub repository.
Docker image build and push to Docker Hub.
Secure handling of credentials using Jenkins credentials.

Project Structure:
