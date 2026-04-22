A [Git branch](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) allows you to keep track of different changes separately.

For example, let's say you have a big web project and you want to experiment with changing the color scheme. Instead of changing the entire project directly (as of right now, our `master` branch), you can create a new branch called `color_scheme` and work on that branch. When you're done, if you like the changes, you can [merge](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) the `color_scheme` branch back into the `master` branch to keep the changes. If you don't like the changes, you can simply delete the `color_scheme` branch and go back to the `master` branch.

## Under the Hood

A branch is just a named [pointer](https://en.wikipedia.org/wiki/Pointer_\(computer_programming\)) to a specific commit. When you create a branch, you are creating a new pointer to a specific commit. The commit that the branch points to is called the tip of the branch.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/iH1kl8l-539x588.png)

Because a branch is just a pointer to a commit, they're lightweight and "cheap" resource-wise to create. When you create 10 branches, you're not creating 10 copies of your project on your hard drive.

Check which branch you're currently on by running:
```bash
git branch
```
Make sure you are in the `project` directory before running the command.

Remember, you should be on `master` because we set `init.defaultBranch` to `master` at the start of the course

1. [ ] Delete the `add_classics` branch:

```bash
git branch -d add_classics
```