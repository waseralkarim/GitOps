# **Remote repo**

Remote allow us to make a copy of our project on the git/internet.

It also allows us to:

- Collab with teammates
- Backup our code
- Check the change-logs
- Remote access from anywhere

### **Basic Git Remote Commands**

- **List remotes:**
  ```bash
  git remote -v
  ```
- **Add a remote repository:**
  ```bash
  git remote add <name> <repo-url>
  ```
  > Commonly, origin is used as the default name for the remote repository.
- **Fetch changes from a remote:**
  ```bash
  git fetch <name>
  ```
- **Rename the current branch to `main`:**
  ```bash
  git branch -M main
  ```
- **Push to the remote repository and set upstream:**
  ```bash
  git push -u origin main
  ```
  > -u sets the upstream tracking reference so future git push and git pull can be used without specifying the branch.
- **Pull from the remote repository:**
  ```bash
  git pull origin main
  ```

### **Handling SSH Certificate Issues (Authentication)**

If you face certificate error on instances:

Generate the key:

```bash
ssh-keygen -t rsa -b 4096 -c <email address>
```

Copy the certificate for public key:

```bash
cat -/.ssh/id_rsa.pub
```

Paste the certificate on GitHub:

- Go to **GitHub > Settings > SSH and GPG keys > New SSH key**
