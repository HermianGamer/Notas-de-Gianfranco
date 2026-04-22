"[Rebase](https://git-scm.com/docs/git-rebase) vs [Merge](https://git-scm.com/docs/git-merge)" is one of the most hotly debated topics in the Git world. A lot of the discussions you'll see online come down to the fact that many developers (yes, even professionals) don't understand the purpose of rebase and use it incorrectly, causing a bunch of Git havoc, and then blame the rebase command.

_It's not Git's fault, it's a skill issue._

Click to hide video

## Visualizing Rebase

Say we have this [[Commit]] history:

```
A - B - C    main
   \
    D - E    feature_branch
```

We're working on `feature_branch`, and want to bring in the changes our team added to `main` so we're not working with a stale branch. We could [[Merge]] `main` into `feature_branch`, but that would create an additional merge commit. Rebase avoids a merge commit by replaying the commits from `feature_branch` on top of `main`. After a rebase, the history will look like this:

```
A - B - C         main
         \
          D - E   feature_branch
```


To use [rebase](https://git-scm.com/docs/git-rebase) to bring changes from `main` onto a current branch (let's pretend we're on one called `jdsl`), we would run this while on the `jdsl` branch:

```bash
git rebase main
```

This will do the following:

1. Identify the latest commit from `main` and use it as the temporary new base for the rebase process
2. Replay each commit from `jdsl` one at a time onto this temporary location
3. Update the `jdsl` branch to point to the last replayed commit in the temporary location, making this the new permanent `jdsl`.
4. The rebase does _not_ affect the `main` branch; `jdsl` now includes all changes from `main`.

## Assignment

1. [ ] Add two commits to the `update_dune` branch. Add the following quotes to the `quotes/dune.md`file's list:
    1. [ ] `- "The spice must flow."` (Use a commit message starting with `H:`)
    2. [ ] `- "Fear is the mind-killer."` (Use a commit message starting with `I:`)
2. [ ] While still on the `update_dune` branch, rebase your changes onto `main`. _`main` is the base, and we want `update_dune`'s changes on top of it_.
3. [ ] Run `git log --oneline`. _Even though we originally branched off the `D` commit from `main`, we should see a nice linear history from `A` to `I`._

**Run and submit** the CLI tests from the **`update_dune` branch**.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/tCgqhtr-464x720.png)Ω