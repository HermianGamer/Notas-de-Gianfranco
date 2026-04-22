You should already be on the `main` [[Branch]]: your "default" branch. You can always check with `git branch`.

## Two Ways to Create a Branch

```bash
git branch my_new_branch
```

This creates a new branch called `my_new_branch`. The thing is, I rarely use this command because usually I want to create a branch and [[Switch Branches]] to it immediately. So I use this [[command]] instead:

```bash
git switch -c my_new_branch
```

The [switch](https://git-scm.com/docs/git-switch) command allows you to switch branches. Including the `-c` flag tells Git to create a new branch and switch to it.

When you create a new branch, it uses the _current [[Commit]]_ you are on as the branch base. For example, if you're on your `main` branch with 3 commits, `A`, `B`, and `C`, and then you run `git switch -c my_new_branch`, your new branch will look like this:

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/oah2FRD-1228x682.png)

## Assignment

1. [ ] Create and switch to a new branch called `add_classics`, it should have the same commits as the `main` branch.
2. [ ] Run `git branch` to verify that you are on the new branch.

**Run and submit** the CLI tests.

## Troubleshooting

The switch command was introduced in Git version 2.23.0, so you might not have it if you're using an older version of Git.