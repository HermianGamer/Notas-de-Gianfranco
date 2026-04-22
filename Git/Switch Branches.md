We talked about using [[Git]] [git switch](https://git-scm.com/docs/git-switch) to change [[Branch]]es. There's another command that you'll certainly run into because it's been around for a long time and older developers are used to it: [git ºcheckout](https://git-scm.com/docs/git-checkout). `git switch` is a newer command that is meant to be more intuitive and user-friendly. It's recommended to use `git switch` over `git checkout` for simply switching branches.

To switch to a branch called `prime`:

```bash
git switch prime

# or, the old way:
git checkout prime
```

For this course, we will stick to `git switch`.

## Assignment

1. [ ] Switch to `main`.
2. [ ] Run `git branch` to make sure it worked (the branch you are "on" has an asterisk next to it).
3. [ ] Switch back to `add_classics`
4. [ ] Run `git branch` to make sure it worked.