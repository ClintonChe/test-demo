# 🚀 Git & GitHub Project Setup Guide

Welcome! This repository is part of a hands-on session on Git and GitHub.  
Follow the steps below to set up your environment and start contributing.

---

## 📌 Prerequisites

Make sure you have the following installed:

- Git
- A GitHub account
- Terminal (Git Bash / PowerShell / Linux shell)

---

## 🔧 Step 1: Configure Git

Set your global username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
````

Verify configuration:

```bash
git config --list
```

---

## 🔑 Step 2: Generate SSH Key

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

* Press **Enter** to accept default location
* Optionally add a passphrase

---

## ⚙️ Step 3: Start SSH Agent

### Windows (PowerShell)

```bash
Start-Service ssh-agent
ssh-add $env:USERPROFILE\.ssh\id_ed25519
```

### Linux / Mac

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

---

## 📋 Step 4: Copy SSH Public Key

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the output.

---

## ➕ Step 5: Add SSH Key to GitHub

1. Go to GitHub → Settings
2. Click **SSH and GPG keys**
3. Click **New SSH key**
4. Paste your key
5. Click **Add SSH key**

---

## ✅ Step 6: Test SSH Connection

```bash
ssh -T git@github.com
```

Expected output:

```
Hi username! You've successfully authenticated...
```

---

## 📥 Step 7: Clone Repository (Using SSH)

```bash
git clone git@github.com:username/repository-name.git
```

---

## 🌱 Basic Git Workflow

### Check status

```bash
git status
```

### Add files

```bash
git add .
```

### Commit changes

```bash
git commit -m "Your message"
```

### Push to GitHub

```bash
git push origin main
```

---

## 🌿 Branching

Create a new branch:

```bash
git checkout -b feature-branch
```

Switch branches:

```bash
git checkout main
```

---

## 🔄 Pull Latest Changes

```bash
git pull origin main
```

---

## 🧠 Best Practices

* Write meaningful commit messages
* Pull before pushing
* Use branches for features
* Never commit sensitive data (passwords, keys)

---

## 🎯 Objective

By the end of this exercise, you should be able to:

* Configure Git
* Authenticate with GitHub using SSH
* Clone, commit, and push code
* Work with branches

---

## 👨‍💻 Author

Your Name

---

## 📚 Resources

* [https://git-scm.com/docs](https://git-scm.com/docs)
* [https://docs.github.com/en/authentication/connecting-to-github-with-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

---

Happy Coding! 🚀

```
