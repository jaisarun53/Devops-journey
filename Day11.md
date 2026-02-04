# 🚀 Day 11: Git Advanced Commands & Interview Guide

## 📖 Overview
Today's session focused on moving from basic Git usage to professional, real-world workflows. We explored how DevOps engineers manage code history, handle collaboration across teams, and secure their repositories.

---

## 🏗️ The Professional Git Lifecycle
The core workflow in any organization follows a specific rhythm to ensure code is tracked and shared safely.

1. **`git init`**: Initializes a local repository. This creates the hidden `.git` folder [00:03:03].
    * **Interview Insight:** The `.git` folder is the "brain" of the repo. It handles tracking, logging, and **Hooks** (like pre-commit hooks to prevent pushing secrets like passwords) [00:04:15].
2. **`git add <file>`**: Moves files to the **Staging Area** so Git begins tracking changes [00:06:56].
3. **`git commit -m "message"`**: Creates a versioned snapshot of your work. This allows you to "traverse" back in time if a new feature breaks the code [00:10:06].
4. **`git push`**: Sends local commits to a **Remote Repository** (GitHub, Bitbucket, etc.) [00:12:25].
    * **Note:** You must configure a **Remote Reference** (`git remote add origin <url>`) before you can push for the first time [00:16:42].

---

## 🔐 Authentication: HTTPS vs. SSH
When cloning or pushing code, you have two main options:
* **HTTPS:** Requires a username and password/token for every session [00:19:44].
* **SSH:** The professional standard. It uses an **RSA Key Pair** (`ssh-keygen`) [00:21:13].
    * **Setup:** Copy your public key (`id_rsa.pub`) and add it to your GitHub Settings > SSH keys to enable passwordless, secure access [00:22:41].

---

## 🍴 Clone vs. Fork
| Action | Description |
| :--- | :--- |
| **`git clone`** | Downloads an existing repository to your local machine [00:18:48]. |
| **`git fork`** | Creates a personal copy of someone else's repository on your GitHub account. This is the heart of "Distributed" version control [00:24:04]. |

---

## 🌳 Advanced Branching & Merging
To work on massive features (like adding a "House Services" section to Amazon) without breaking the live site, we use **Isolation** [00:28:21].

* **`git checkout -b <branch>`**: Creates and switches to a new branch instantly [00:31:35].
* **`git merge <branch>`**: Combines changes. It can result in a non-linear history [00:41:09].
* **`git rebase <branch>`**: Re-writes history to be **Linear**. This makes the commit history much easier to read in large projects [00:48:57].
* **`git cherry-pick <commit-id>`**: Used to pick a *single* specific commit from one branch and apply it to another [00:34:32].

### ⚠️ Handling Merge Conflicts
Conflicts happen when two people edit the same line of code. Git stops the process and asks you to choose which change to keep.
* **The Fix:** Open the file, consult with the developer who wrote the other code, resolve the lines manually, `git add`, and then finish the commit [00:43:31].

---

## 🛠️ Key Commands Summary
| Command | Purpose |
| :--- | :--- |
| `git status` | Check current state (staged/unstaged) [00:05:49]. |
| `git log --oneline` | View a clean, single-line history [00:40:24]. |
| `git diff` | See exact line changes made [00:07:43]. |
| `git remote -v` | See where your local repo is connected [00:16:08]. |

---
[⬅️ Day 10](./day10.md) | [Main README](../README.md)
