# 📘 Git & GitHub Workflow Notes

This document contains my practice workflow for:

* Git setup and configuration
* Creating repositories
* SSH setup with GitHub
* Collaboration with a friend’s repository
* Simulating merge conflicts

---

# 🧰 1. Git Setup & Configuration

```bash
git --version
```

Check installed Git version.

```bash
git config --list
```

Show current Git configuration.

```bash
git config --global user.name "tester"
```

Set global Git username.

```bash
git config --global user.email "tooltesting07@gmail.com"
```

Set global Git email.

```bash
git config --list
```

Verify updated configuration.

---

# 📁 2. Creating a New Git Project

```bash
cd Documents/
ls
mkdir testgit
```

Navigate to Documents and create project folder.

```bash
git init
```

Initialize Git repository.

```bash
git status
```

Check repository status.

```bash
cd testgit
git init
```

Initialize Git inside project folder.

---

# 📝 3. First Commit

```bash
nano gitcommands.md
```

Create/edit file.

```bash
git add gitcommands.md
```

Add file to staging area.

```bash
git commit -m "First commit"
```

Create first commit.

---

# 🌿 4. Branch Setup

```bash
git branch
```

Show current branches.

```bash
git branch -M main
```

Rename branch to `main`.

```bash
git branch
```

Verify branch name.

---

# 🔗 5. Connect Repository to GitHub (SSH)

```bash
git remote add origin git@github.com:tester-2070/testgit.git
```

Add GitHub remote using SSH.

```bash
git push -u origin main
```

Push code and set upstream.

---

# 🔐 6. SSH Setup for GitHub

```bash
ls -al ~/.ssh
```

Check existing SSH keys.

```bash
ssh-keygen -t ed25519 -C "tooltesting007@gmail.com"
```

Generate SSH key.

```bash
cat ~/.ssh/id_ed25519.pub
```

Display public key (add this to GitHub).

```bash
ssh -T git@github.com
```

Test SSH connection.

```bash
git push -u origin main
```

Push using SSH authentication.

---

# 📊 7. Status & History

```bash
git status
```

Check current state of repository.

```bash
history > history.md
```

Save terminal history to file.

---

# 🤝 8. Collaborating with Friend's Repository

## Clone Repository

```bash
cd Documents/
mkdir gitcolab
cd gitcolab/
```

```bash
git clone git@github.com:sumanthbhegdemca/testing-connection.git
```

Clone friend's repository.

```bash
git status
ls
ls -a
```

Check files and repository status.

```bash
cd testing-connection/
```

Enter project folder.

---

## Make Changes

```bash
cat test.txt
```

View file content.

```bash
nano test.txt
```

Edit file.

```bash
git add .
git commit -m "commit by pavan1"
git push -u origin main
```

Commit and push changes.

---

# 💥 9. Simulating Merge Conflict

## Create Branch

```bash
git checkout -b pavan
```

Create and switch to new branch.

---

## Change File in Branch

```bash
nano test.txt
git add .
git commit -m "pavan branch"
git push -u origin pavan
```

---

## Change Same File in Main

```bash
git checkout main
nano test.txt
git add .
git commit -m "main 2"
git push
```

---

## Merge and Trigger Conflict

```bash
git checkout main
git merge pavan
```

Conflict occurs if both branches changed the same lines.

---

## Resolve Conflict

```bash
nano test.txt
```

Manually edit conflict markers.

```bash
git add .
git commit -m "merge conflict resolved"
git push
```

---

## Delete Branch After Merge

```bash
git branch -d pavan
```

Delete merged branch.

```bash
git status
git branch
```

Verify cleanup.

---

# 🧠 Best Practices

* Always create a new branch for features
* Pull latest changes before starting work
* Use SSH for easier authentication
* Resolve conflicts carefully
* Keep commits small and meaningful

---

# 📌 Quick Workflow Summary

```
Setup Git → Create Repo → Commit → Add Remote → Push
        ↓
Clone Repo → Create Branch → Commit → Push
        ↓
Merge → Resolve Conflicts → Push → Delete Branch
```

