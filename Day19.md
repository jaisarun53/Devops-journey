# Jenkins Day 19: Zero to Hero - Docker Agents & GitOps

## 📌 Overview
This project focuses on advanced Jenkins configurations, specifically using Docker containers as build agents and implementing a GitOps workflow for Kubernetes deployments.

---

## 🛠️ 1. Infrastructure Setup
1.  **EC2 Instance:** Launch an Ubuntu T2.medium instance.
2.  **Jenkins Installation:** Install Java (Prerequisite) and Jenkins.
3.  **Security:** Open Port `8080` in the AWS Security Group to access the Jenkins UI.
4.  **Docker Setup:** Install Docker on the Jenkins machine and grant the `jenkins` user permissions to the Docker socket.

---

## 🏗️ 2. Jenkins Architecture: Master vs. Agent
* **Jenkins Master:** Used only for scheduling and managing jobs.
* **Docker Agents:** Instead of static VMs, Jenkins spins up a container (e.g., Node.js, Maven) only when a job runs and destroys it immediately after.
    * **Advantage:** Saves cost and avoids dependency conflicts between different projects.

---

## 📄 3. Sample: Multi-Stage Multi-Agent Pipeline
This pipeline uses different environments for different stages within a single job.

```groovy
pipeline {
    agent none 
    stages {
        stage('Build Backend') {
            agent { docker { image 'maven:3.8.1-adoptopenjdk-11' } }
            steps {
                sh 'mvn --version'
                // sh 'mvn clean package'
            }
        }
        stage('Build Frontend') {
            agent { docker { image 'node:16-alpine' } }
            steps {
                sh 'node --version'
                // sh 'npm install'
            }
        }
    }
}
```
## ☸️ 4. Full CI/CD with GitOps (Jenkins + Argo CD)
A modern pipeline workflow for Kubernetes:

** Checkout: Jenkins pulls code from GitHub.
** Build & Push: Jenkins builds a Docker image and pushes it to Docker Hub.
** Update Manifest: Jenkins updates the deployment.yaml file in the Git repo with the new image tag.
** Argo CD: Automatically detects the change in Git and synchronizes the state to the Kubernetes Cluster.

## 🔍 5. Interview Questions & Debugging

* **Q: Why use Docker agents over EC2 agents?**
    * **A:** Containers are lightweight, ephemeral, and allow for easy environment versioning without the overhead of manual VM maintenance or configuration drift.

* **Q: How do you handle secrets in Jenkins?**
    * **A:** Use the **Jenkins Credentials Provider** to securely store sensitive data like Docker Hub tokens, Git SSH keys, and API secrets, which are then injected into the pipeline as environment variables.

* **Q: What is GitOps?**
    * **A:** It’s an operational framework where Git is the **"Single Source of Truth."** In this model, tools like Argo CD or Flux continuously monitor Git repositories and ensure the live cluster state matches the configuration defined in the code.


