# Git Workflow & Conflict Resolution Assignment

## Overview
This repository serves as a practical demonstration of standard Git workflows, fulfilling the requirements for branching, merging via Pull Requests, and resolving merge conflicts. 

## Acceptance Criteria Met
- [x] Created at least 2 branches and merged them via PR.
- [x] Resolved at least one merge conflict.
- [x] Documented the difference between `merge` and `rebase`.

## Workflow Executed
1. **Base Setup:** Initialized the repository with a `main.py` file on the `master` branch.
2. **Standard Feature Merge:** Created the `feature-user-auth` branch, updated the code, and successfully merged it into `master` via a GitHub Pull Request.
3. **Conflict Generation:** Created two parallel branches (`conflict-branch-A` and `conflict-branch-B`) that modified the exact same line of code to intentionally trigger a conflict.
4. **Conflict Resolution:** Merged branch A first. When attempting to merge branch B, a merge conflict was triggered. The conflict was manually resolved in the GitHub UI, and the final merge was completed.

---

## Technical Concept: Merge vs. Rebase

As part of this assignment, here is the technical distinction between merging and rebasing:

### `git merge`
* **Mechanism:** Takes two distinct branch histories and ties them together by creating a brand new "merge commit."
* **Use Case:** Best for bringing finished feature branches into a shared `master` or `main` branch. 
* **Pros/Cons:** It is non-destructive and preserves the exact chronological history of the repository. However, frequent merging can result in a cluttered, web-like commit history.

### `git rebase`
* **Mechanism:** Takes the commits from a feature branch and "replays" them one by one at the very tip of the base branch.
* **Use Case:** Best for cleaning up local, private branches before sharing them with the team.
* **Pros/Cons:** It creates a perfectly linear, clean, and readable commit history. However, because it rewrites repository history (creating new commit hashes), it should **never** be used on public branches that other developers are actively using.
