# Submodule

Git submodule allows you to include a separate Git repository inside another repository. It is useful for managing dependencies or shared code across projects.

```bash
git submodule add <repository_url> <path>
```

### **Common Use Cases**

- Sharing libraries or frameworks across multiple projects.
- Keeping dependencies separate from the main repository.
- Managing large projects with modular components.

![Image](https://github.com/user-attachments/assets/7f88c643-1e21-4bdf-8de2-f6a481fe8d59)

### **Cloning a Repository with Submodules**

When cloning a repository with submodules, use:

```bash

git clone --recurse-submodules <repo_url>
```

If you've already cloned it without submodules, initialize them manually:

```bash
git submodule init
git submodule update

```

### **Updating Submodules**

To pull the latest changes from the submodule’s remote repository:

```bash
git submodule update --remote
```

To update all submodules:

```bash
git submodule update --remote --recursive
```

### **Removing a Submodule**

1. Unregister the submodule:

   ```bash
   git submodule deinit -f <path_to_submodule>
   ```

2. Remove the submodule directory:
3. Remove the submodule entry from `.gitmodules` and commit the changes.
