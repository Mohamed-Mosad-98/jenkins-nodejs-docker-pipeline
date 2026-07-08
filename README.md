# Jenkins CI/CD Pipeline for Dockerized Node.js Application

This project demonstrates how to build a complete **CI/CD pipeline** using **Jenkins** to automatically build and deploy a Dockerized **Node.js** application hosted on GitHub.

The main objective of this project is to demonstrate **Pipeline as Code**, **GitHub Integration**, **Docker Build Automation**, and **Container Deployment** using Jenkins.

---

## Project Overview

This project was completed as part of a Jenkins CI/CD lab.

The sample **Node.js application** used during this lab was cloned from a public GitHub repository created for educational purposes.

The original repository was forked into my GitHub account to integrate it with Jenkins and implement a complete CI/CD pipeline.

This repository focuses on the **DevOps implementation** rather than the application source code.

---

## Original Application

The application source code was obtained from the following public repository:

**Original Repository**

https://github.com/abdelrahmanonline4/sourcecode

After forking the repository, I integrated it with Jenkins and implemented an automated CI/CD workflow.

---

# Technologies Used

- Jenkins
- Docker
- Git
- GitHub
- Node.js
- Linux (Ubuntu)

---

# Project Workflow

```text
                GitHub Repository
                        │
                        ▼
              Jenkins Pipeline Job
                        │
                        ▼
               Checkout Source Code
                        │
                        ▼
              Build Docker Image
                        │
                        ▼
              Run Docker Container
                        │
                        ▼
           Node.js Application Running
```

---

# Pipeline Stages

## Stage 1 — Checkout

Jenkins automatically clones the latest source code from the GitHub repository.

---

## Stage 2 — Build Docker Image

A Docker image is built using the project's Dockerfile.

```bash
docker build -t nodeapp:latest .
```

---

## Stage 3 — Run Docker Container

After successfully building the image, Jenkins starts a Docker container.

```bash
docker run -d --name nodeapp -p 3000:3000 nodeapp:latest
```

---

# Project Structure

```text
jenkins-nodejs-docker-pipeline/
│
├── Jenkinsfile
├── README.md
│
└── screenshots/
    ├── 01-jenkins-service-running.png
    ├── 02-pipeline-success.png
    ├── 03-docker-container.png
    └── 04-running-application.png
```

---

# Verification

The project was successfully verified by:

- Jenkins service running successfully
- Jenkins Pipeline executed successfully
- Docker image built successfully
- Docker container running
- Application accessible on Port 3000

---

# Screenshots

## Jenkins Service Running

![Jenkins Service](screenshots/01-jenkins-service-running.png)

---

## Successful Jenkins Pipeline

![Pipeline Success](screenshots/02-pipeline-success.png)

---

## Running Docker Container

![Docker Container](screenshots/03-docker-container.png)

---

## Running Node.js Application

![Running Application](screenshots/04-running-application.png)

---

# Skills Demonstrated

- Jenkins Administration
- Jenkins Pipeline
- Pipeline as Code
- GitHub Integration
- Docker Image Build
- Docker Container Deployment
- CI/CD Automation
- Linux Administration

---

# Learning Outcomes

By completing this project, I gained hands-on experience with:

- Configuring Jenkins on Ubuntu
- Integrating Jenkins with GitHub repositories
- Writing Jenkins Pipelines using Jenkinsfile
- Building Docker images automatically
- Deploying Docker containers through Jenkins
- Automating application deployment using CI/CD principles

---

# Author

**Mohamed Mosad Fahmy**

Computer & Software Engineering Graduate

GitHub:

https://github.com/Mohamed-Mosad-98

LinkedIn:

https://www.linkedin.com/in/mohamed-mosad-516aa717b/
