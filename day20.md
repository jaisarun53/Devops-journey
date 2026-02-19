🚀 Day 20: GitHub Actions – Zero to Hero Automation

Day 20 marked a major shift from managing CI/CD infrastructure (Jenkins) to using **GitHub Actions**, a modern, cloud-native automation platform. The session focused on "Platform-as-a-Service" CI/CD, where the pipeline lives directly alongside the source code.

🔑 Key Learning Objectives

* **Event-Driven Automation:** Learned how to trigger workflows based on GitHub-specific events like `push`, `pull_request`, `fork`, or even `issue` creation.
* **The Workflow Hierarchy:** Understanding the relationship between **Workflows** (the YAML file), **Jobs** (set of steps), and **Steps** (individual tasks/actions).



* **GitHub Marketplace:** Leveraging pre-built, community-verified "Actions" to avoid writing repetitive scripts for common tasks (e.g., setting up Docker, Java, or AWS CLI).
* **Matrix Strategy:** Implementing parallel execution to test applications across multiple OS versions and language runtimes (e.g., Python 3.8, 3.9, 3.10) simultaneously.

---

### 📊 Deep Dive: GitHub Actions vs. Jenkins

| Feature | GitHub Actions | Jenkins |
| :--- | :--- | :--- |
| **Maintenance** | Zero (GitHub handles updates) | High (Manual plugin & OS updates) |
| **Integration** | Native to GitHub | Requires Webhooks & Plugins |
| **Infrastructure** | GitHub-hosted or Self-hosted | Must provide your own servers |
| **Parallelism** | Native Matrix support | Complex to configure (Parallel stages) |
| **Security** | Built-in Secrets Management | Credentials Provider Plugin |

---

🛠️ Technical Concepts Covered

### 1. Workflow Anatomy
* **`on:`**: Defines the trigger (e.g., `on: [push, pull_request]`).
* **`runs-on:`**: Specifies the virtual environment (e.g., `ubuntu-latest`, `windows-latest`).
* **`uses:`**: Calls a reusable action from the Marketplace (e.g., `actions/checkout@v3`).

### 2. Self-Hosted Runners
Learned how to bypass GitHub’s shared resource limits by configuring an **AWS EC2 instance** as a dedicated runner. 



* **When to use:** For high-compute tasks, long-running builds, or access to private VPC resources.
* **Setup:** Executed the runner registration script to connect a local terminal/EC2 to the GitHub Actions pool.

### 3. CI/CD for Java & Python
* **Java:** Configured Maven builds, unit testing, and SonarQube code analysis.
* **Python:** Used the Matrix strategy to ensure code quality across different version environments.

---

✅ Accomplishments & Projects

* **Project 1: Automated Unit Testing:** Built a CI pipeline for a Python application that triggers on every Pull Request to ensure no breaking changes are merged.
* **Project 2: Dockerized Workflow:** Created a workflow that builds a Docker image, tags it with the Git Commit SHA, and pushes it to Docker Hub using GitHub Secrets.
* **Project 3: K8s Deployment:** Explored a full CD pipeline that updates Kubernetes manifests and triggers a deployment to an EKS cluster upon a successful merge to `main`.
* **Runner Configuration:** Successfully registered a custom Linux runner, allowing for faster, dedicated build execution.

