# 🚀 Day 8: GitHub API Integration with Shell Scripting

## 📖 Overview
In real-world DevOps environments, managing user access across hundreds of repositories manually is inefficient. This project demonstrates how to use **Shell Scripting** and the **GitHub REST API** to automate the process of listing users with access to a specific repository.



---

## 🏗️ Project Architecture
The project follows a standard API consumption pattern:
1.  **Authentication:** Uses a Personal Access Token (PAT) for secure access.
2.  **API Request:** Uses `curl` to send GET requests to GitHub's REST API.
3.  **Data Processing:** Uses `jq` to parse the JSON response and filter for specific user roles.
4.  **Reporting:** Outputs a clean list of collaborators to the terminal.

---

## 🎯 Project Objective
* Understand the difference between **UI**, **CLI**, and **API**.
* Learn how to read and use **API Documentation**.
* Automate the audit of GitHub repository collaborators.
* Practice secure handling of credentials using environment variables.

---

## 🛠️ Prerequisites
* **GitHub Account:** You need a Personal Access Token (PAT).
    * *Path:* Settings -> Developer Settings -> Personal access tokens (classic).
* **JQ Installed:** Essential for parsing JSON.
    * *Install:* `sudo apt install jq -y`
* **Environment Variables:**
    ```bash
    export username="your_github_username"
    export token="your_github_pat_token"
    ```

---

## 📜 The Shell Script: `list_users.sh`

```bash
#!/bin/bash

#########################################
# Author: arun jaiswal
# Purpose: List users with access to a GitHub Repo
#########################################

# GitHub API URL
API_URL="[https://api.github.com](https://api.github.com)"

# GitHub username and personal access token (exported in env)
USERNAME=$username
TOKEN=$token

# User and Repository information (passed as arguments)
REPO_OWNER=$1
REPO_NAME=$2

# Function to make a GET request to the GitHub API
function github_api_get {
    local endpoint="$1"
    local url="${API_URL}/${endpoint}"

    # Send a GET request to the GitHub API with authentication
    curl -s -u "${USERNAME}:${TOKEN}" "$url"
}

# Function to list users with read access to the repository
function list_users_with_read_access {
    local endpoint="repos/${REPO_OWNER}/${REPO_NAME}/collaborators"

    # Fetch the list of collaborators and filter using JQ
    collaborators="$(github_api_get "$endpoint" | jq -r '.[] | select(.permissions.pull == true) | .login')"

    if [[ -z "$collaborators" ]]; then
        echo "No users with read access found for ${REPO_OWNER}/${REPO_NAME}."
    else
        echo "Users with read access to ${REPO_OWNER}/${REPO_NAME}:"
        echo "$collaborators"
    fi
}

# Main Execution
echo "Listing users with access to ${REPO_OWNER}/${REPO_NAME}..."
list_users_with_read_access
