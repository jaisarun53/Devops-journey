# 🛠️ Day 15: Ansible Practical — Ad-Hoc Commands, Playbooks, and Roles

On Day 15, the focus shifted from the theory of Configuration Management to hands-on practical implementation. We moved from manual server configuration to automated, repeatable processes using Ansible.

---

## 🏗️ 1. Lab Setup & Architecture
The environment consists of an **Ansible Control Node** (where Ansible is installed) and **Managed Nodes** (Target Servers).



### Key Prerequisites:
* **Installation:** Installed via package manager: `sudo apt install ansible`.
* **Agentless Connectivity:** Established passwordless authentication by copying the Control Node's SSH public key (`id_rsa.pub`) into the `authorized_keys` file of the target servers.
* **Inventory File:** Created a file named `inventory` to map target IP addresses and group them (e.g., `[web_servers]`).

---

## ⚡ 2. Ansible Ad-Hoc Commands
Ad-hoc commands are perfect for quick, one-time tasks without the need to write a full YAML file.

**Syntax:** `ansible <group> -i <inventory> -m <module> -a "<arguments>"`

| Task | Command |
| :--- | :--- |
| **Check Connectivity** | `ansible all -i inventory -m ping` |
| **Check Disk Space** | `ansible all -i inventory -m shell -a "df -h"` |
| **Create a File** | `ansible all -i inventory -m shell -a "touch devops.txt"` |
| **Check CPU Info** | `ansible all -i inventory -m shell -a "nproc"` |

---

## 📜 3. Our First Playbook: Automating Nginx
We transitioned from single commands to **Playbooks** (YAML files) to manage complex configurations. This example automates the installation and deployment of an Nginx web server.

**File:** `nginx-setup.yaml`
```yaml
---
- name: Install and Start Nginx Web Server
  hosts: all
  become: true  # Grants sudo privileges
  tasks:
    - name: Install Nginx
      apt:
        name: nginx
        state: present

    - name: Start Nginx Service
      service:
        name: nginx
        state: started
        enabled: yes

```
### To Execute:
`ansible-playbook -i inventory nginx-setup.yaml`

## 📂 4. Mastering Ansible Roles
For large-scale projects (like a Kubernetes cluster setup), writing everything in one file is unmanageable. Roles allow us to break configurations into reusable components.
### Initialize a Role:
`ansible-galaxy role init kubernetes`

### Role Structure Explained:

  tasks/: Contains the main list of tasks to be executed.

  handlers/: Tasks that only run when "notified" (e.g., restarting a service after a config change).

   vars/: Stores variables used within the role.

  templates/: Holds .j2 (Jinja2) templates for dynamic configuration files.

  meta/: Information about the role (author, license, dependencies).

  💡 Pro Tip: Use the -vvv flag when running playbooks to see detailed debug logs, which show exactly how Ansible is communicating with the target servers.

  ### 🎯 Summary of Learning
  Configured a professional Control Node / Managed Node environment.

  Mastered Idempotency: Ensuring that running a playbook multiple times doesn't cause unintended side effects.

  Learned to target specific server groups using Inventories.

  Understood how to scale automation using Ansible Roles.
