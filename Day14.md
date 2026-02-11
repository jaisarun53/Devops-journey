# Day 14: Configuration Management with Ansible 🚀

## 📖 Overview
As infrastructure grows, manually SSH-ing into servers to install packages or update security patches becomes a bottleneck. Day 14 covers how **Configuration Management** solves this by treating infrastructure as code.

## 🛠️ Why Ansible?
While tools like Puppet, Chef, and Salt exist, Ansible is the "winner" for most DevOps teams due to several factors:

| Feature | Ansible | Puppet / Chef |
| :--- | :--- | :--- |
| **Architecture** | **Agentless** (No software needed on nodes) | **Agent-based** (Requires master-slave setup) |
| **Model** | **Push** (Configurations sent from laptop/master) | **Pull** (Nodes pull config from master) |
| **Language** | **YAML** (Human readable) | **DSL** (Proprietary language) |
| **Connection** | SSH (Linux) / WinRM (Windows) | Custom Protocols / Certificates |

## 🏗️ Core Concepts
1. **Inventory File:** A simple file (or dynamic script) containing the IP addresses or DNS of the servers you want to manage.
2. **Playbooks:** YAML files where you define the "desired state" of your servers (e.g., "Ensure Nginx is installed and running").
3. **Modules:** Pre-written Python scripts that Ansible executes on the target machine (e.g., `apt`, `yum`, `copy`, `service`).
4. **Ansible Galaxy:** A community hub to find and share re-usable roles and modules.

## 💡 Key Takeaways
- **Agentless is King:** You don't need to manage "agent" software versions on 10,000 servers. If you have SSH access and Python installed, you can manage it with Ansible.
- **Dynamic Inventory:** In AWS, servers are often "ephemeral" (created and destroyed quickly). Ansible can automatically query AWS to find all instances in a specific region and apply configurations without manual IP entry.
- **Support:** While built on Python, it has robust support for both Linux and Windows environments.

## ❓ Common Interview Questions Covered
- **Push vs. Pull:** Why use one over the other?
- **Protocols:** How does Ansible connect to Linux (SSH) vs. Windows (WinRM)?
- **Python Dependency:** Does the target machine need Python? (Yes, for most modules).

---
[⬅️ Day 13](./day13.md) | [Home](../README.md)
