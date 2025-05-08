## Git Rebase

Git rebase is a powerful command that allows developers to modify and reorganize their commit history by changing the base of their current branch to a different commit.

- This process effectively rewrites the project history by creating new commits for each commit in the original branch, resulting in a more linear and cleaner Git history.
- Unlike merging, which creates a new commit that combines changes from different branches, rebasing moves or combines a sequence of commits to a new base commit, making the commit history more straightforward and easier to follow.

Command for git rebase:

```bash
git rebase <branch name>
```

## Pull Request (PR)

Pull request, also known as PR, is a powerful collaborative feature that allows developers to propose changes to a codebase in a structured and reviewable way. It serves as a formal mechanism for discussing, reviewing, and integrating code changes from one branch into another.

**Branch Protection:**

It is a protection for the dev, main, or production branch which is very sensitive. It ensures that without proper approval the code won’t be pushed on the sensitive branches.

**Benefits of branch protection:**

- Enforces code review and approval process.
- Prevents direct pushes or force pushes.
- Ensures CI/CD checks are passed before merge.

When we want to push something on branch protected branch we push it remotely using this command:

```bash
git push --set-upstream origin <branch name>
```

1. After that in the GitHub webpage there will be prompt “Compare and pull request”.
2. Then if we want to push it on main we have to submit PR request from the website.
3. Finally the PR request goes through review process.
