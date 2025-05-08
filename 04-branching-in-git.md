# Branching in Git

![Image](https://github.com/user-attachments/assets/9822aab7-dbab-4f60-ae63-efc8858e5721)

Master/Main: Production grade code. Any changes will impact customer visibility

Sub-branches: Created from main branch which gives us more isolated environment for R&D and collaboration with others.

commands:

Check the available branches:

```bash
git branch
```

Create a new branch:

```bash
git branch <branch name>
```

Switch to a branch:

```bash
git  checkout <branch name>
```

Check status of current branch and changes:

```bash
git status
```

Delete a branch:

```bash
git branch -d <branch name>
```

## **Branching Strategies**

### **1. Gitflow Workflow**

**Use case:** This strategy is used for large scale projects with a proper set of team environment and resources.

Key Benefit's:

- Properly organized and systematic approach
- Great for managing multiple branches
- Good correlation with the team

Disadvantages:

- For smaller projects it can be complex
- Development cycle is longer
- More overhead in maintenance

### **2. Github Flow**

**Use case:** Best for **web applications** and **continuous delivery** environments.

Key Benefit’s:

- Simple and easy to learn
- Good for continuous delivery
- Good for web applications

Disadvantages:

- No hotfix branches
- Cannot version control
- Limited support for multiple env

### **3. Trunk-Based Development**

**Use case:** Used primarily in organizations that have implemented sophisticated automation systems and follow DevOps best practices. This approach works exceptionally well for teams that have established robust continuous integration pipelines, comprehensive testing frameworks, and efficient deployment mechanisms that allow for rapid verification and release of code changes.

Key Benefit’s:

- Merge conflict is minimal
- Better for CI/CD
- Fast integration cycles

Disadvantages:

- High risk without proper automation
- Requires strong QA testing culture
- Every small change needs to recognized
