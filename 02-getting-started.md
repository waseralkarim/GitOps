# Getting Started

Follow this [Git for Linux](https://git-scm.com/downloads/linux) official documentation for installing git.

### **Debian/Ubuntu**

For the latest stable version for your release of Debian/Ubuntu

```bash
apt-get install git
```

For Ubuntu, this PPA provides the latest stable upstream Git version

```bash
add-apt-repository ppa:git-core/ppa
```

```bash
apt update; apt install git
```

### **Fedora**

```bash
yum install git
```

(up to Fedora 21)

```bash
dnf install git
```

(Fedora 22 and later)

# Configurations:

Initialize a new Git repository

```bash
git init <repo name>
cd <repo name
```

Creating our initial commit

```bash
echo "Initial commit" > [README.md](http://readme.md/)
git add [README.md](http://readme.md/)
git commit -m "Initial commit"
```

Configuring the Git user details

```bash
git config --global [user.name](http://user.name/) "<your name"
git config --global user.email "<email address>"
```

# Basic Commands

These are the essential Git commands you'll use regularly:

| Command | Description |
| --- | --- |
| `git init` | Initializes a new Git repository in your current directory |
| `git clone <repo-url>` | Creates a local copy of a remote repository |
| `git status` | Shows the status of your working directory (changes, staged files, etc.) |
| `git add <file>` | Stages a specific file for commit |
| `git add .` | Stages all changed files for commit |
| `git commit -m "message"` | Commits staged changes with a descriptive message |
| `git log` | Displays a list of recent commits |
| `git diff` | Shows the differences between files or commits |
| `git branch` | Lists all branches or creates a new one |
| `git checkout <branch>` | Switches to another branch |
| `git merge <branch>` | Merges another branch into your current branch |
| `git pull` | Fetches and merges changes from the remote repo to your local one |
| `git push` | Pushes your local commits to the remote repository |

> 💡 Tip: Always commit with meaningful messages and pull before pushing to avoid merge conflicts.
