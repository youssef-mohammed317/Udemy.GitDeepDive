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
git reflog

54d55b3 (HEAD -> main, tag: 2.0, origin/main) HEAD@{0}: checkout: moving from e27c0a8fe6dfdf564791fc0299ae2b01f665472a to main
e27c0a8 HEAD@{1}: checkout: moving from main to 1.0
54d55b3 (HEAD -> main, tag: 2.0, origin/main) HEAD@{2}: commit: file3 added
e27c0a8 HEAD@{3}: commit: file2 added
2c0dd71 HEAD@{4}: commit: start wroking with tags file1 added
e18ec51 HEAD@{5}: cherry-pick: fix typo in m1
ddba7a0 HEAD@{6}: checkout: moving from feature-2 to main
aab22e4 (feature-2) HEAD@{7}: commit: add f2-new
d34b9cf HEAD@{8}: commit: fix typo in m1
350cc4a HEAD@{9}: commit: add f1-new
ddba7a0 HEAD@{10}: checkout: moving from main to feature-2
ddba7a0 HEAD@{11}: commit: add text to m1
1404eb7 HEAD@{12}: commit (merge): merged feature and main in f1
f29466c HEAD@{13}: reset: moving to HEAD
f29466c HEAD@{14}: checkout: moving from feature to main
e393b99 (feature) HEAD@{15}: commit: change in feature
9c1dd21 HEAD@{16}: checkout: moving from main to feature
f29466c HEAD@{17}: commit: change in main
9c1dd21 HEAD@{18}: merge feature: Fast-forward
1afb12b HEAD@{19}: checkout: moving from feature to main
9c1dd21 HEAD@{20}: rebase (finish): returning to refs/heads/feature
9c1dd21 HEAD@{21}: rebase (pick): f2 added
b24634f HEAD@{22}: rebase (pick): f1 added
1afb12b HEAD@{23}: rebase (start): checkout main
56e6287 HEAD@{24}: checkout: moving from main to feature
