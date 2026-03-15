# Udemy.GitDeepDive — Advanced Git Practice Repo

This repository contains **deeper Git exercises** I completed while following the Udemy course:
**“Git & GitHub – The Practical Guide”**.

It is focused on understanding **advanced Git mechanics**:
merge vs rebase, cherry-pick, tags, reflog, resets, and history manipulation across branches.

---

## What I practiced here

- Comparing **merge** and **rebase**
- Understanding fast-forward vs merge commit behavior
- Rebasing feature work onto `main`
- Using `git cherry-pick` to copy selected commits
- Exploring project history with `git reflog`
- Recovering from resets and history changes
- Creating and checking tags
- Observing how Git history changes after rewrite operations

---

## Repository structure

| Path | Purpose |
|------|---------|
| `main/` | Main branch practice files |
| `feature/` | Feature branch practice files |
| `tags/` | Files used while learning tag-related workflow |

---

## Key Git commands used (core set)

> Exact flags/options can vary, but these are the commands I used to perform the actions reflected in the reflog.

```bash
# basic branch work
git switch -c feature
git switch main
git merge feature

# rebase workflow
git rebase main
git rebase --continue
git rebase --abort

# cherry-pick
git cherry-pick <commit-sha>

# history recovery
git reflog
git reset HEAD~1
git reset --hard <commit-sha>

# tags
git tag 1.0
git tag 2.0
git checkout 1.0
git checkout main

# history inspection
git log --oneline --graph --decorate --all
