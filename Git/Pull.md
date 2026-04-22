[[Fetch]]ing is nice, but most of the time we want the _actual file changes_ from a [[Remote]] [[repositorio]], not just the metadata.

## Command Syntax

`git pull [<remote>/<branch>]`

_The `[...]` syntax means that the bracketed remote and branch are optional. If you execute git pull without anything specified it will pull your current branch from the remote repo_.

## Assignment

Let's use the GitHub UI to commit a change to our remote repo. Then we'll pull that change down to our local repo.

1. [ ] Navigate to your GitHub repo in your browser
2. [ ] Ensure the GH repo's `main` branch's latest commit is `G`
3. [ ] Navigate to the `classics.csv` file on the `main` branch
4. [ ] In the top right corner of the file, click the pencil icon to edit it in place:

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/db5JNUQ-495x381.png)

5. [ ] Add a new line to the end of the file:

```
Willow, Ron Howard, 1988
```

6. [ ] Commit the change using the UI, **but change the commit message** to:

```
J: update classics.csv
```

No need for an extended description.

7. [ ] On your command line, make sure you're on your `main` branch.
8. [ ] Run `git config set pull.rebase false` to make sure git will merge on a pull

Omitting the `set` part of the command was deprecated in Git `2.46.0`.

9. [ ] Merge the changes from the `update_dune` branch back into `main` so that main has everything we've done so far (`A` through `I`)
10. [ ] Run `git pull origin main` to pull in the most recent `J` commit that you made remotely. You should see that it starts a merge commit.
11. [ ] Rename the merge commit message to start with `K:`
12. [ ] Make sure everything worked with `git log --oneline`. You should have commits "A" through "K" locally.
13. [ ] Delete the `update_dune` branch locally

**Run and submit** the CLI tests from inside your **`webflyx` directory**.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/gmj5WB9-600x425.png)