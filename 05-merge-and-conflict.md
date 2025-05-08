## Merge and Conflict

When we combine branches with one another it is called merging. For example, we have two branch called dev and feature. When a developer finish his task on feature branch he have to merge his work on dev branch. Then we use merge command for combine the finished work.

```bash
git checkout <target-branch>
git merge <source-branch>
```

![Image](https://github.com/user-attachments/assets/3aab53e6-02d1-4ef8-98f0-91dc90f763ba)

We can check the error logs in a visualized way by using these commands:

```bash
git log --graph
git log --graph --oneline --all
```
