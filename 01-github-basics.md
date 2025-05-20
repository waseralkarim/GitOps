# Creating Repositories

- Click on the **"New"** button from your GitHub homepage.
- Choose a **repository name**.
- Decide whether it will be **public** (visible to everyone) or **private**.
- Optionally, initialize the repo with a `README.md`, `.gitignore`, and license.

# Cloning Repositories

To work on a project locally, you need to clone it.

```bash
git clone https://github.com/username/repository-name.git

```

# Understanding Commits and Commit History

A **commit** is a snapshot of your changes. Each commit should be meaningful and include a clear message describing what was changed.

```bash

git add .
git commit -m "Add meaningful message"
git push origin main

```

You can view your commit history using:

```bash
git log

```

Or on GitHub through the **"Commits"** tab of your repository.

This creates a local copy on your machine. You can then make changes and push them back to GitHub.

# Some basic GitHub terminology

### **Repository**

In simple term it is storage location which:

- Stores our code, files and projects datas.
- Tracks the changes in the system.
- Commit history etc.

### **Hashing**

Hashing is one of the core knowledge that is pre requisite for GitHub.

What is hashing value used for?

- It is used for security purposes. For example we can check the file integrity of the downloaded file or software.
- It enables efficient data retrieval and comparison through creating a unique fixed-size output for data of any size. This makes operations like lookups in hash tables very fast.
- Hashing is essential for cryptographic applications like digital signatures and password storage, where it helps verify authenticity without revealing actual data.

We can check the hash value of a file by using this command:

```bash
sha256sum <filename>
```
