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

