# Git LFS

**What is Git LFS?**

Git Large File Storage is an extension for Git that improves handling of large files like images, videos, datasets by storing them outside the main Git repository while keeping lightweight references in Git.

**Why Use Git LFS?**

- Reduces repository size by storing large files separately.
- Speeds up cloning and fetching operations.
- Optimized for large binary files that don’t diff well.

Command for installing Git LFS:

```jsx
git lfs install
```

Using this command the git hook will be updated and git lfs will be initialized.

```bash
git lfs track "file name"
```

LFS tracks the files. Git will only manage the pointers and LFS will handle the storage.

After using this command .gitattributes file will be created on .git folder.

![Image](https://github.com/user-attachments/assets/a13d8fab-74ba-49a0-9940-1010f2a62b02)

Usually LFS handles tracks psd, binary, exe, png, psd etc. formatted files. It doesn’t track text format.

```bash
git add .gitattributes <file name>
```

**Add & Commit Files**

```bash
git add "file name"
git commit -m "Added large file with LFS"
git push origin <branch location>
```

**Also if we like we can clone a repo with LFS Files using this command:**

```bash
git lfs clone <repo-url>
```

To check the current lfs tracking files we have to use this command:

```bash
git lfs ls-files
```

**Tip:** Always install Git LFS before cloning an LFS-enabled repo to avoid missing files.

Additionally:

`git lfs status` → Check tracked files' status.

`git lfs migrate import --include="*.mp4"` → Convert existing large files to LFS.

```bash
git lfs pointer --file=<file-name>
```

This command displays the Git LFS pointer file for a specific file. A pointer file is a lightweight reference stored in Git instead of the actual large file. Usually for normal pull requests the pointers gets pulled. But for Git LFS the data is also included.
