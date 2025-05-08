# Subtree

### **What is Subtree?**

`git subtree` allows you to manage repositories inside other repositories, treating them as subdirectories instead of separate submodules.

### **Why use subtree?**

- Easier than `git submodule` (no `.gitmodules` file).
- No need for users to run `git submodule update`.
- Commits remain in the main repository, avoiding detached submodule states.

### **Common Commands**

**Add a subtree**

```bash
git subtree add --prefix=<dir> <remote-url> <branch> --squash
```

- Adds a remote repository inside `<dir>`.
- `-squash`: Combines remote commits into one.

**Pull latest changes**

```bash
git subtree pull --prefix=<dir> <remote-url> <branch> --squash

```

- Fetches and merges updates from the remote repo.

**Push subtree changes**

```bash
git subtree push --prefix=<dir> <remote-url> <branch>
```

- Pushes updates made in the subtree to the remote repo.

**Extract a subtree into a separate repository**

```bash
git subtree split --prefix=<dir> --branch=<new-branch>
```

- Creates a new branch with just the subtree history.

**Merge subtree changes into the main repo**

```bash
git merge -s subtree <branch>

```

- Merges a subtree branch into the main branch.

### **Key Differences: Subtree vs Submodule**

| Feature               | git subtree         | git submodule              |
| --------------------- | ------------------- | -------------------------- |
| Repo Structure        | Stored in main repo | Separate sub-repo          |
| Ease of Use           | Simple commands     | Requires extra setup       |
| External Dependencies | None                | Needs git submodule update |
