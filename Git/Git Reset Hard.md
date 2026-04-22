In the last lesson, we undid a commit but kept the changes. We don't want to keep the changes to `titles.md`. Here's how to reset those changes:

```bash
git reset --hard COMMITHASH
```

The `--hard` flag makes your working directory and staging area match the specified commit exactly, discarding any local changes. This is useful if you just want to go back to a previous commit and discard all the changes.

## Assignment

1. [ ] Run `git status` to confirm a staged change that modified the `titles.md` file.
2. [ ] Run `git reset --hard <I commit hash>` to undo the change.
3. [ ] Check to make sure the `titles.md` file is reset:

```bash
git status
```

# **Danger**

I want to stress how **dangerous** this command can be. If you were to simply delete a _committed_ file, it would be trivially easy to recover because it is tracked in Git. However, if you used `git reset --hard` to undo committing that file, it would be deleted for good.

Always be careful when using `git reset --hard`. It's a powerful tool, but it's also a dangerous one.