# Git & GitHub Guide for 2CP Students

A concise, practical guide to help 2CP students manage projects with Git and GitHub. Use this as a checklist and reference while working on coursework.

## 1) Why use Git/GitHub?
- **Track changes**: See what changed and why.
- **Collaborate safely**: Work in parallel without overwriting each other.
- **Recover work**: Restore older versions easily.
- **Show progress**: Your history documents your contributions.

## 2) Key Concepts (simple view)
- **Repository (repo)**: The project folder tracked by Git.
- **Commit**: A saved snapshot of your work.
- **Branch**: A separate line of work (feature, fix, experiment).
- **Merge**: Combine work from one branch into another.
- **Remote**: The GitHub copy of your repo.
- **Pull request (PR)**: A request to merge work on GitHub (review + discussion).

## 3) Setup (one-time)
1. **Install Git**
2. **Configure identity**
   - `git config --global user.name "Your Name"`
   - `git config --global user.email "you@email.com"`
3. **Create GitHub account**
4. **Create or clone a repository**

## 4) Basic Daily Workflow
### A) Start working
1. Open a terminal in your project folder.
2. Create/checkout a branch:
   - `git checkout -b feature/short-task-name`

### B) Save your work (commit)
1. See changes:
   - `git status`
2. Stage changes:
   - `git add .`
3. Commit with a clear message:
   - `git commit -m "Add login form validation"`

### C) Share to GitHub
1. Push your branch:
   - `git push -u origin feature/short-task-name`
2. Open a Pull Request on GitHub.

## 5) Branching Strategy (simple, safe)
- **main**: Always stable. Only merged work goes here.
- **feature/***: One branch per task (e.g., `feature/navbar`).
- **fix/***: Bug fixes (e.g., `fix/api-error`).

## 6) Pull Requests (PRs)
**Before opening a PR**:
- Code compiles/runs.
- No extra debug files.
- Descriptive PR title + short summary.

**Reviewing a PR**:
- Check if it solves the task.
- Ask questions in comments.
- Approve when it’s good.

## 7) Useful Commands (cheat sheet)
- `git status` — see current state
- `git add <file>` — stage file
- `git add .` — stage all
- `git commit -m "message"` — save snapshot
- `git log --oneline` — history
- `git checkout -b new-branch` — create branch
- `git checkout main` — switch branch
- `git pull` — get latest from GitHub
- `git push` — send commits to GitHub
- `git merge branch-name` — merge into current branch

## 8) Common Problems (and fixes)
### “I forgot to add a file”
- `git add <file>`
- `git commit --amend --no-edit`

### “I pushed to the wrong branch”
- Create correct branch:
  - `git checkout -b feature/right-branch`
- Push it:
  - `git push -u origin feature/right-branch`
- (Optional) delete wrong branch from GitHub.

### “Merge conflict”
1. Open conflicted files.
2. Decide which code to keep.
3. Remove conflict markers.
4. `git add <file>`
5. `git commit`

## 9) Project Management Tips
- **Agree on tasks early** (use GitHub Issues or a simple checklist).
- **Small commits**: easier to review and fix.
- **Meaningful messages**: describe what and why.
- **Push often**: avoid losing work.
- **Use branches**: never code directly on `main`.

## 10) Example Workflow for a Team Task
1. Create Issue: “Add user login page.”
2. Create branch `feature/login-page`.
3. Implement the task.
4. Commit and push.
5. Open PR, request review.
6. Merge into `main`.

## 11) Minimal .gitignore (example)
Use a .gitignore to avoid committing build files, secrets, and temporary files.

Example for common projects:
```
node_modules/
.env
.DS_Store
*.log
```

## 12) Quick Checklist Before Submitting
- [ ] Code runs on a clean machine.
- [ ] No secrets in repo.
- [ ] README describes how to run.
- [ ] Each feature has commits.
- [ ] `main` is clean and stable.

---
If you want, I can tailor this guide to your project language (web, Java, C, Python, etc.) or add a more detailed GitHub workflow diagram.
