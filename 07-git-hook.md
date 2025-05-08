# GitHook

It is a custom script that runs automatically at specific time frames in the Git workflow in order to automate repetitive task or enforce the policies.

It is located in ./.git/hooks directory.

- It works like a plugin
- Customizable based on environment

GitHook can be on:

1. Client Side
2. Server Side

### **Types of Git Hooks**

1. **Client-Side Hooks** (triggered by local actions)
   - `pre-commit` → Runs before a commit is created (e.g., code formatting, linting).
   - `prepare-commit-msg` → Modifies the commit message before the editor opens.
   - `commit-msg` → Validates or modifies the commit message before it's saved.
   - `pre-push` → Runs before pushing to the remote repository (e.g., run tests).
   - `post-commit` → Runs after a commit is made (e.g., notifications).
2. **Server-Side Hooks** (triggered on the remote repository)
   - `pre-receive` → Runs before a push is accepted (e.g., reject bad commits).
   - `update` → Runs per branch when updates are pushed.
   - `post-receive` → Runs after changes are received (e.g., deployment, notifications).

### **Creating a Git Hook**

1. Navigate to `.git/hooks/` in your repo.
2. Rename a sample script (e.g., `pre-commit.sample` → `pre-commit`).
3. Make it executable:

   ```bash
   chmod +x .git/hooks/pre-commit
   ```

Example: **Pre-Commit Hook for Linting**

```bash
#!/bin/bash
# Run linting before committing
echo "Running lint checks..."
npm run lint
if [ $? -ne 0 ]; then
  echo "Linting failed. Fix issues before committing."
  exit 1
fi
```

If there are any policy involved, we can bypass it by using this command:

```bash
git commit -am "commit message" --no-verify
```

### **Using Git Hooks for CI/CD**

- Validate commit messages using `commit-msg` (e.g., enforce conventional commits).
- Run tests before pushing using `pre-push`.
- Automate deployments with `post-receive` on the remote server.
