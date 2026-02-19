# ♾️ My 45-Day DevOps Journey: Zero to Hero

Welcome to my documentation of the **Zero to Hero DevOps Course**. This repository is a living log of my transition into the world of DevOps—tracking daily progress, technical insights, and the cultural shifts required to master modern software delivery.

<details open>
<summary>🚀 <b>Day 1: The Genesis – Understanding the "Why" and "What" of DevOps</b></summary>
<br>

### The Narrative: Beyond the Textbook
In the traditional software world, delivery was a slow, fragmented process. Developers wrote code and "tossed it over the wall" to the Operations team. This resulted in silos, manual bottlenecks, and delivery cycles that took weeks or even months. 

**DevOps emerged as the solution.** It isn’t just a set of tools; it is a **culture** and a **practice**. The goal is to increase an organization’s ability to deliver applications at high velocity without sacrificing quality.



### 🏗️ The Four Pillars of DevOps
While many equate DevOps solely with CI/CD, it actually rests on four critical pillars that ensure a healthy delivery ecosystem:

1. **Automation 🤖**: Moving away from manual labor to repeatable, automated processes. If a task is performed twice, it should be automated.
2. **Quality ✅**: Ensuring every piece of code is reliable. Speed is useless if the application is broken upon arrival.
3. **Monitoring & Observability 📉**: You cannot improve what you cannot measure. Continuous monitoring ensures the system's health is always visible.
4. **Continuous Testing 🧪**: Testing is no longer a "final phase." It is integrated into every step of the lifecycle to catch bugs as early as possible.

> **The Professional Definition:** DevOps is a culture and process of improving application delivery by ensuring proper automation, maintained quality, continuous monitoring, and rigorous testing.

### 🕰️ The Evolution: Why We Need It
* **The Old World:** System Admins, Build & Release Engineers, and Server Admins worked in separate bubbles. A simple deployment could take 10+ days because of manual hand-offs and a lack of shared responsibility.
* **The New World:** DevOps breaks these silos. By integrating these roles into a unified culture, we reduce that 10-day cycle to hours or even minutes. This is how modern tech giants maintain their competitive edge.

### 🎤 Professional Growth: The Art of the Introduction
A key part of Day 1 was learning how to position oneself in the industry. Whether coming from a System Admin, Developer, or Testing background, the secret to a great DevOps introduction is highlighting your **problem-solving mindset**.

Instead of just listing tools (like Jenkins or Docker), focus on how you implement the **Four Pillars** to solve business problems. Being authentic about your background and showing an eagerness to adapt to the "DevOps Culture" is what sets a candidate apart in an interview.

### 💡 Key Takeaways
* DevOps is a **mindset shift**, not just a job title.
* The ultimate goal is **Velocity + Reliability**.
* Silos and manual processes are the primary enemies of efficiency.

---
</details>




<details open>
<summary>🚀 <b>Day 2: SDLC & The Role of DevOps</b></summary>
<br>

### Bridging the SDLC Gap with DevOps
On Day 2, the focus shifted to the backbone of the IT industry: the **Software Development Life Cycle (SDLC)**. Understanding this lifecycle is non-negotiable, as it defines the standard process for designing, developing, and testing high-quality software.

#### 🏗️ The 6 Phases of SDLC
1. **Planning & Requirement Gathering 📝**: Gathering customer feedback to define the "What."
2. **Defining 📑**: Creating the **Software Requirement Specification (SRS)**.
3. **Designing 🎨**: Blueprints for architecture (HLD) and specific logic (LLD).
4. **Building (Developing) 💻**: Developers writing code and pushing to **Git**.
5. **Testing 🧪**: QA Engineers validating the code in staging environments.
6. **Deployment 🚀**: Promoting the code to production for the end user.


---

## 🏛️ Phase 0: The Business of DevOps (Prerequisites)
Before writing code, I explored how software moves from a customer's idea to a DevOps engineer's task.

* **Organizational Awareness:** Understanding the roles of Product Managers, Architects, and the Scrum Team.
* **Agile Methodology:** Working in Sprints, attending Daily Stand-ups, and managing blockers.
* **The Jira Workflow:** How "Business Requirements" (BRD) become "Technical Tasks" via Epics and Stories.

👉 **[Detailed Prerequisite Documentation](./Absolute%20Prerequisite%20for%20Learning%20DevOps.md)**

---

#### 🛠️ The DevOps Battleground
A DevOps engineer acts as the "accelerant" for the SDLC. While we are aware of all phases, our primary focus is on **automating** the **Building, Testing, and Deployment** phases. 

By removing manual intervention, we ensure:
* **Efficiency:** Faster delivery cycles.
* **Reliability:** Reduced human error during deployment.
* **Agility:** Moving away from rigid models to fast-paced, iterative Sprints.

> **Key Takeaway:** SDLC is about *Quality*; DevOps is about *Quality at Speed*.

---
</details>

<details open>
<summary>🚀 <b>Day 3: Virtual Machines & Virtualization</b></summary>
<br>

**Focus:** Moving from physical hardware to logical infrastructure.

* **The Shift:** Moving away from "Bare Metal" (physical servers) to **Virtual Machines (VMs)** to eliminate resource waste.
* **The Land Analogy:** Understanding how one physical server (the land) can host multiple isolated VMs (houses) without interference.
* **The Hypervisor:** Learning about the software (Type 1 & Type 2) that acts as the "Resource Traffic Controller" for CPU and RAM.
* **Cloud Mechanics:** How AWS and Azure use hypervisors in global Data Centers to provide EC2 instances on demand.



> **Key Takeaway:** Virtualization is the core engine of the Cloud. It provides the **Efficiency** and **Scaling** that DevOps requires.

👉 **[Read Full Day 3 Documentation](./day3.md)**

---
</details>

<details>
<summary>🚀 <b>Day 4: AWS & Azure – Hands-on VM Creation</b></summary>
<br>

**Focus:** Moving from theory to practice by launching cloud infrastructure.

* **Manual vs. Automated:** Understanding that while the **AWS Console** and **Azure Portal** are great for learning, DevOps engineers use **APIs** and **CLI** for efficiency.
* **EC2 Instance Creation:** Successfully navigated the AWS lifecycle: Choosing an **AMI (Ubuntu)**, selecting **Free Tier (t2.micro)**, and generating **Key Pairs (.pem)** for secure access.
* **Automation Tools:** Brief introduction to **Infrastructure as Code (IaC)** tools like **Terraform, AWS CDK, and CloudFormation** that eliminate manual human error.
* **Security & Networking:** Learned that a request must be **Valid, Authenticated, and Authorized** before a Hypervisor provisions resources.



> **Key Takeaway:** A DevOps engineer’s goal is **Efficiency**. If you have to create 100 servers, you write a script; you don't click the button 100 times.

👉 **[Read Full Day 4 Documentation](./day4.md)**

---
</details>
<details>
<summary>🛠️ <b>Day 5: AWS CLI & SSH Mastery</b></summary>
<br>

**Focus:** Mastering the command line and secure remote access.

* **SSH Connectivity:** Learned how to log into EC2 instances using the terminal and the importance of setting correct permissions (`chmod 400`) on `.pem` keys.
* **AWS CLI Setup:** Configured local environments using `aws configure` to interact with AWS services without opening a browser.
* **Resource Management:** Practiced managing S3 buckets and EC2 instances directly through terminal commands.
* **Automation Teaser:** Explored how **Boto3 (Python)** and **CloudFormation** are used to automate resource creation at scale.

> **Key Takeaway:** Real DevOps work happens in the terminal. Mastering the CLI and SSH is the first step toward true automation.

👉 **[Read Full Day 5 Documentation](./day5.md)**

---
</details>

<details>
<summary>🐧 <b>Day 6: Linux & Shell Scripting Fundamentals</b></summary>
<br>

**Focus:** Understanding the Linux OS and mastering the terminal.

* **Linux Architecture:** Explored the relationship between **Hardware**, the **Kernel** (Heart of OS), and the **Shell** (Command Interpreter).
* **Navigation Mastery:** Learned essential commands for file management: `pwd`, `ls -ltr`, `cd`, `mkdir`, and `touch`.
* **System Monitoring:** Practiced checking server health using `top` (Task Manager), `free -m` (RAM), and `df -h` (Disk space).
* **File Editing:** Introduction to the **VI editor**—learning to switch between Command and Insert modes to edit configuration files.
* **Why Linux?** Discussed why Linux's security, speed, and open-source nature make it the standard for DevOps.

> **Key Takeaway:** You cannot be a DevOps Engineer without being comfortable in a Linux terminal. It is the foundation for Docker, Kubernetes, and Cloud.

👉 **[Read Full Day 6 Documentation](./day6.md)**

---
</details>

---

## 📅 Day 8: GitHub API Integration Project

Automated user access auditing for GitHub repositories using Shell Scripting and REST APIs. This project focuses on the intersection of automation, security, and data parsing.

### 🚀 Key Features
* **GitHub REST API:** Consumed live endpoints to fetch repository metadata.
* **Authentication:** Implemented secure API access using Personal Access Tokens (PAT) and environment variables.
* **JSON Parsing:** Utilized `jq` to filter complex nested data and extract specific collaborator information.
* **User Audit:** Created a script that identifies users with specific permissions (Read/Write) for security compliance.

### 🛠️ Tech Stack
`Bash` | `GitHub API` | `Curl` | `JQ` | `Linux`



**[View Day 8 Project Details](./day8.md)**

---

---

## 📅 Day 9: Git & GitHub Mastery

Mastered the core concepts of Version Control Systems (VCS) and the practical workflow of Git and GitHub, which are essential for collaboration in DevOps.



### 🚀 Key Features
* **Version Control Fundamentals:** Deep dive into why VCS is critical for code sharing and disaster recovery.
* **Architecture:** Compared **Centralized** (SVN) vs. **Distributed** (Git) systems to understand fault tolerance.
* **Git Internals:** Explored the local lifecycle of code—Moving files from the **Working Directory** to the **Staging Area** and finally to **Commits**.
* **GitHub Integration:** Learned how to bridge local development with cloud hosting using Remote repositories and **Forking**.

### 🛠️ Tech Stack
`Git` | `GitHub` | `Version Control` | `Linux Terminal`



**[View Day 9 Project Details](./day9.md)**

---


---

## 📅 Day 10: Git Branching Strategies

Focused on how enterprise-level organizations manage massive codebases using advanced Git branching workflows. This knowledge is essential for maintaining production stability while allowing for rapid feature development.



### 🚀 Key Features
* **Feature Branching:** Isolated development environments for new functionality to prevent breaking the main codebase.
* **Release Management:** Using dedicated Release branches to perform final testing and "freeze" code before production deployment.
* **Emergency Hotfixes:** Implementing the Hotfix workflow to patch critical production bugs without waiting for the next release cycle.
* **Industry Standards:** Analyzed the branching models used by **Kubernetes** and **Uber** to handle thousands of concurrent contributors.

### 🛠️ Tech Stack
`Git` | `GitHub` | `SDLC` | `DevOps Workflows`



**[View Day 10 Project Details](./day10.md)**

---
---

## 📅 Day 11: Git for DevOps - Real World Scenarios

Deep dived into the practical application of Git in a professional DevOps environment, focusing on automation, security, and advanced history management.



### 🚀 Key Features
* **Professional Workflow:** Mastered the `Add-Commit-Push` lifecycle and understood the internal role of the `.git` directory for tracking and security hooks.
* **Authentication Security:** Configured **SSH Key-based authentication** (`ssh-keygen`) to implement secure, passwordless communication between local machines and GitHub.
* **Complex Merging:** Analyzed the technical trade-offs between **Merge** and **Rebase**, focusing on how to maintain a clean linear history in large-scale enterprise projects.
* **Precision Operations:** Practiced **Cherry-picking** to isolate and apply specific commits across branches without performing a full merge.
* **Conflict Resolution:** Learned to manually resolve merge conflicts, a critical skill when multiple teams collaborate on the same microservice or configuration file.

### 🛠️ Tech Stack
`Git` | `GitHub` | `SSH` | `Linux CLI` | `Version Control`



**[View Full Day 11 Project Details](./day11.md)**

---
---

## 📅 Day 11: Git for DevOps — Real-World Scenarios

Today’s session focused on professional Git workflows, moving beyond simple commands to understand how DevOps engineers manage collaboration, security, and complex code histories.



### 🚀 Key Takeaways
* **Inside the `.git` Directory:** Explored the internal structure of Git and how **Hooks** (like pre-commit) can be used to scan for secrets or enforce coding standards.
* **Secure Authentication:** Configured **SSH Key-based authentication** (`ssh-keygen`) to implement secure, passwordless communication between local environments and GitHub.
* **Strategic Branching:** Learned to use feature branches to isolate massive changes (e.g., a "House Services" feature) without disrupting the production-ready `main` branch.
* **Precision Operations:** Mastered **Cherry-picking** to pull specific, high-priority commits (like bug fixes) into a branch without performing a full merge.
* **Merge vs. Rebase:** Deep dive into the trade-offs between preserving an exact history (**Merge**) versus maintaining a clean, linear project timeline (**Rebase**).
* **Conflict Resolution:** Learned the manual process of resolving merge conflicts that occur when multiple teams edit the same lines of code.



### 🛠️ Tech Stack & Essential Commands
`Git` | `GitHub` | `SSH` | `CLI`

* `git checkout -b <branch>` — Create and switch to a new feature branch.
* `git cherry-pick <commit-id>` — Apply a specific change from another branch.
* `git rebase <branch>` — Re-write history for a cleaner timeline.
* `git remote add origin <url>` — Connect a local repository to the cloud.

**[View Full Day 11 Project Details](./day11.md)**

---
---

## 📅 Day 12: Deploy and Expose Your First App to AWS

Today’s session was a hands-on live project featuring Kunal Verma. We moved from local development to the cloud by deploying a real-time NodeJS application (integrated with Stripe) onto an AWS EC2 instance and making it accessible to the world.

### 🚀 Key Takeaways
* **Local Testing First:** Cloned the repository and tested the NodeJS app locally to ensure all dependencies and environment variables (`.env`) were working correctly.
* **AWS IAM Best Practices:** Instead of using the Root account, we created an **IAM User** with specific permissions. This is a critical security standard in DevOps to minimize risk.
* **Provisioning EC2:** Launched an **Ubuntu 22.04 LTS** instance on AWS, selecting the `t2.micro` instance type to stay within the Free Tier.
* **Server Configuration:** Connected via **SSH** and manually bootstrapped the remote server by installing:
    * **Git**: To pull the source code.
    * **NodeJS & NPM**: To build and run the application environment.
* **Environment Security:** Used **Vim** to securely create a hidden `.env` file on the server to store Stripe API keys without exposing them in the version control.
* **Networking & Security Groups:** The most crucial step—learned how to edit **Inbound Rules** to open **Port 3000**, allowing the public internet to access the application hosted on the EC2 instance.

### 🛠️ Tech Stack & Essential Commands
`AWS EC2` | `IAM` | `NodeJS` | `Linux` | `Stripe API`

* `ssh -i <key.pem> ubuntu@<public-ip>` — Securely connect to the AWS instance.
* `sudo apt update && sudo apt install nodejs npm` — Prepare the server environment.
* `touch .env && vim .env` — Create and edit hidden configuration files.
* **Security Group Config**: Added a Custom TCP rule for **Port 3000** with source `0.0.0.0/0`.

**[View Day 12 Video Tutorial](http://www.youtube.com/watch?v=NLmF64KdLN0)**

---
### 🗓️ Day 13: Top 15 AWS Services for DevOps

On Day 13, I shifted from manual deployment to a strategic overview of the **AWS Cloud Ecosystem**. With over 200+ services available, the focus was on identifying the core tools that drive **Automation, Security, and Efficiency** in a modern DevOps pipeline.



**Key Highlights:**
* **Infrastructure & Networking:** Explored the foundational roles of **EC2** (Compute), **VPC** (Networking), and **Lambda** (Serverless).
* **Native CI/CD:** Studied the AWS Developer stack—**CodePipeline**, **CodeBuild**, and **CodeDeploy**—as alternatives to external tools like Jenkins.
* **Security & Governance:** Deep-dived into **IAM** for access control, **AWS Config** for compliance, and **CloudTrail** for API auditing.
* **Containers:** Analyzed the differences between **EKS** (Managed Kubernetes) and **ECS** (AWS Proprietary) for container orchestration.
* **Monitoring:** Leveraged **CloudWatch** for observability and **Billing/Cost Management** for infrastructure optimization.

> **Crucial Takeaway:** DevOps is about using the right tool for the job. Mastering these 15 services allows for building resilient, "Well-Architected" cloud environments.

---

### 🛠️ Day 14: Configuration Management & Ansible Theory

This session introduces the concept of **Configuration Management** and why it is critical for maintaining consistency across a fleet of servers. We explore **Ansible** as the primary tool for solving manual overhead.

**Key Learning Objectives:**
* **Manual vs. Automated Management:** Why logging into 100 servers individually is a security and operational risk.
* **The Agentless Advantage:** Understanding how Ansible uses SSH to manage nodes without requiring client-side software installation.
* **Idempotency:** Learning how Ansible ensures a task is only performed if the system is not already in the desired state.
* **Ansible Architecture:** Introduction to Control Nodes, Managed Nodes, and the Inventory system.



---

### 📜 Day 15: Ansible Playbooks & Practical Implementation

In this session, we move from theory to hands-on automation by learning how to write and execute **Ansible Playbooks** to manage infrastructure at scale.

**Key Learning Objectives:**
* **YAML for Automation:** Mastering the syntax used to write declarative Ansible Playbooks.
* **Inventory Management:** Organizing servers into groups (e.g., [web_servers], [db_servers]) for targeted automation.
* **Tasks & Modules:** Using built-in modules like `apt`, `yum`, `copy`, and `service` to perform complex operations.
* **Practical Workflow:** Setting up passwordless SSH authentication and executing playbooks using the `ansible-playbook` command.

### ☁️ Day 16: Infrastructure as Code (IaC) & Terraform Foundations

This session explores the theoretical shift from manual infrastructure configuration to automated, code-based management. We dive deep into why **Terraform** has become the industry standard for modern DevOps.

**Key Learning Objectives:**
* **The Problem with Platform Lock-in:** Understanding why native tools like AWS CloudFormation (CFT) or Azure Resource Manager (ARM) create challenges in hybrid-cloud environments.
* **The Terraform Solution:** How a single, provider-agnostic tool can manage multiple cloud platforms (AWS, Azure, GCP) and on-premise systems.
* **API as Code:** A deep dive into how Terraform translates HCL (HashiCorp Configuration Language) into programmatic API calls to talk to cloud providers.
* **Hybrid & Multi-Cloud Strategy:** Why organizations are moving toward architectures that utilize the best services from different clouds simultaneously.



---
**Detailed Documentation:** [day16.md](./day16.md)

## 🚀 Day 17: Terraform Production-Grade Management

Day 17 marked the transition from basic Terraform usage to professional, team-oriented infrastructure management. The focus was on ensuring state security, collaboration, and code reusability.

### 🔑 Key Learning Objectives

* **Remote State Management:** Migrated the `terraform.tfstate` from local storage to **Amazon S3** for centralized access and durability through versioning.
* **State Locking:** Implemented **DynamoDB** to handle state locking. This prevents race conditions and state corruption when multiple engineers work on the same infrastructure simultaneously.
* **Modular Architecture:** Explored **Terraform Modules** to package resource configurations into reusable "Lego blocks," enforcing DRY (Don't Repeat Yourself) principles and organizational standards.
* **Professional Workflow:** Mastered the clean separation of concerns using `variables.tf`, `outputs.tf`, and `backend.tf` to keep projects manageable and scalable.

### 🛠️ Technical Concepts Covered
* **Backend Configuration:** Setting up S3 and DynamoDB within the `terraform` block.
* **Lifecycle Management:** Deep dive into `init`, `plan`, `apply`, and `destroy` in a remote context.
* **State Drift:** Understanding the limitations of Terraform when manual changes occur in the AWS Console.
* **Multi-Cloud Strategy:** Leveraging different Providers (AWS, Azure, GCP) under the same HCL syntax.

### ✅ Accomplishments
- [x] Secured the infrastructure "Source of Truth" using an S3 Remote Backend.
- [x] Prevented concurrent execution conflicts with DynamoDB State Locking.
- [x] Created reusable resource templates using Terraform Modules.
- [x] Standardized project structure for better team collaboration.

**Detailed Documentation:** [day17.md](./day17.md)

📅 Day 18: Introduction to CI/CD — The Heart of DevOps Automation
Today’s session transitioned from manual infrastructure and scripting to the architectural foundation of Modern Pipelines. We explored how Continuous Integration and Continuous Delivery (CI/CD) turn code commits into customer value through automated trust and "Quality Gates."

### 🔑 Key Learning Objectives

* **Core Pipeline Philosophy:** Mastered the distinction between **Continuous Integration** (build/test), **Continuous Delivery** (manual release gate), and **Continuous Deployment** (fully automated live release).
* **The "Safety Net" Strategy:** Explored the automation lifecycle—from Unit Testing and **Static Code Analysis** (SonarQube) to Vulnerability Scanning and Artifact creation.
* **Environment Promotion:** Learned how to architect a staging-to-production flow, ensuring that software is benchmarked in a "mirror" environment before reaching the end user.
* **Legacy vs. Advanced Setup:** Compared traditional **Jenkins** (static Master/Slave nodes) with modern, event-driven, and cost-optimized pipelines used by top MNCs (like **GitHub Actions** or Kubernetes-based runners).

### 🛠️ Technical Concepts Covered
* **Orchestration:** Using a central engine (Jenkins/GitLab) to coordinate diverse tools (Maven, Docker, Sonar).
* **Feedback Loops:** Implementing instant notifications so developers can "Fail Fast" and fix bugs within minutes.
* **Artifact Management:** Understanding the "Source of Truth" for compiled binaries (JARs/WARs) and Docker Images.
* **Zero-Waste Compute:** Transitioning from 24/7 idle servers to dynamic, container-based pipeline runners.

### ✅ Accomplishments
- [x] Defined the standard stages of a production-grade CI/CD pipeline.
- [x] Analyzed the cost-benefit ratio of Legacy vs. Advanced CI/CD setups.
- [x] mapped out the "Gatekeeping" process for secure code promotion.
- [x] Prepared the architectural blueprint for the upcoming Jenkins Live Project.

**Detailed Documentation:** [day18.md](./day18.md)

🚀 Day 18: Kubernetes Kubectl & Pod Management

Day 18 shifted focus from infrastructure provisioning to container orchestration. The session covered the fundamental interaction with a Kubernetes cluster using the Kubectl CLI, moving from simple commands to declarative configuration files.

🔑 Key Learning Objectives

* **Kubernetes Hierarchy:** Mastered the relationship between Deployments, ReplicaSets, and Pods. Learned that we manage Deployments to let Kubernetes handle Pod lifecycles.
* **Imperative vs. Declarative:** Compared quick CLI commands (`kubectl create`) against the professional standard of using YAML files (`kubectl apply`) for version-controlled infrastructure.
* **Pod Blueprinting:** Explored the Deployment configuration, understanding how to define container images, ports, and replica counts in a single manifest.
* **Container Scaling:** Learned how the ReplicaSet ensures the "Desired State" by automatically spinning up new pods if one fails.



🛠️ Technical Concepts Covered

* **CRUD Operations:** Mastering `get`, `create`, `edit`, and `delete` for various cluster resources.
* **Debugging Toolkit:** Using `describe` to find infrastructure errors (like ImagePullBackOff) and `logs` to find application-level crashes.
* **Interactive Debugging:** Leveraging `kubectl exec -it` to drop into a running container's terminal for real-time troubleshooting.
* **State Updates:** Managing live updates to deployments using `kubectl edit` and observing how Kubernetes performs rolling updates.

✅ Accomplishments

* Deployed and managed a multi-pod Nginx environment.
* Successfully troubleshot failing pods using the Describe/Logs/Exec workflow.
* Implemented a declarative deployment using a YAML configuration file.
* Scaled applications horizontally by modifying replica counts in real-time.

**Detailed Documentation:** [day18.md](./day19.md)

### 🚀 Day 20: GitHub Actions – Zero to Hero Automation

**Focus:** Modernizing CI/CD by transitioning from self-hosted Jenkins to cloud-native GitHub Actions.

* **Platform Integration:** Leveraged GitHub’s native event-driven system to trigger pipelines on `push`, `pull_request`, and `issue` events.
* **Workflow as Code:** Defined entire CI/CD lifecycles using YAML manifests stored in `.github/workflows/`, ensuring pipelines version-control alongside application code.
* **Infrastructure Flexibility:** Explored **GitHub-hosted runners** for convenience and configured **Self-hosted Runners** on AWS EC2 for high-compute tasks and private VPC access.
* **Parallel Execution:** Implemented the **Matrix Strategy** to test applications across multiple OS and language versions (Python/Node.js) simultaneously.
* **Real-world Projects:** Built automated testing for Python, a Docker build-and-push workflow, and a K8s deployment pipeline using GitHub Secrets.



---

**Detailed Documentation:** [day18.md](./day20.md)

