# 🚀 Day 12: Deploy and Expose Your First App to AWS

## 📖 Project Overview
Today’s project was a practical dive into cloud infrastructure. We transitioned a real-time **NodeJS application** (integrated with a Stripe payment gateway) from a local development environment to a live production environment on **AWS EC2**.

---

## 🏗️ Deployment Architecture
The workflow involves setting up a secure environment, provisioning a virtual server, and configuring networking to allow public traffic.



### 1. Identity & Access Management (IAM)
Following DevOps best practices, we avoided using the Root account.
* **IAM User**: Created a specific user with restricted permissions for this project.
* **Permissions**: Assigned policies to manage EC2 instances.
* **Benefit**: Reduces security risks and provides an audit trail for account actions.

### 2. Provisioning the EC2 Instance
* **AMI**: Ubuntu 22.04 LTS (HVM).
* **Instance Type**: `t2.micro` (Free Tier eligible).
* **Key Pair**: Generated and downloaded a `.pem` key for secure SSH access.
* **Security Group**: Initial configuration allowed only Port 22 (SSH).

---

## 🛠️ Step-by-Step Implementation

### Phase 1: Server Access & Preparation
After the instance status changed to "Running," we connected via the terminal to bootstrap the environment.

```bash
# Set key permissions (essential for SSH)
chmod 400 your-key.pem

# SSH into the Ubuntu server
ssh -i "your-key.pem" ubuntu@<EC2-Public-IP>

# Update package lists and install Node.js/NPM
sudo apt update
sudo apt install nodejs npm -y



```
## Phase 2: Application Deployment

### We pulled the source code from GitHub and configured the environment variables required for the Stripe API to function.

# Clone the repository
git clone <your-repo-link>
cd <repo-folder>

# Install app dependencies
npm install

# Create environment file for API keys
touch .env
vim .env
# [Inside vim: add STRIPE_API_KEY and PORT=3000]


## Phase 3: Exposing the App

### By default, AWS blocks all traffic except SSH. To make our application visible to users, we modified the Inbound Rules in the Security Group.

  Go to: EC2 Console > Security Groups > Inbound Rules.

  Action: Add Rule -> Custom TCP -> Port 3000 -> Source 0.0.0.0/0 (Anywhere).



## 🎯 Final Result

### The application became accessible globally via the browser at: http://<Your-EC2-Public-IP>:3000
💡 Key Learning Points

  Security Groups act as a virtual firewall, controlling both inbound and outbound traffic at the instance level.

   Environment Variables (.env) are crucial for keeping secrets (like Stripe API keys) out of Version Control (Git).

  Manual Bootstrapping provides a clear understanding of application dependencies before moving toward automation tools like Docker or Ansible.

    
