As you know, [[Git Log]] shows you the history of [[Commit]]s in your repo. There are a few flags I like to use from time to time to make the output easier to read.

The first is [`--decorate`](https://git-scm.com/docs/git-log#Documentation/git-log.txt---decorateshortfullautono). It can be one of:

- `short` (the default)
- `full` (shows the full ref name)
- `no` (no decoration)

`--decorate` is now automatically applied as of version `2.12.2`. Here are more options you should know:

Run `git log --decorate=full`. You should see that instead of just using your branch name, it will show the full ref name. A [ref](https://git-scm.com/book/en/v2/Git-Internals-Git-References) is just a pointer to a commit. All branches are refs, but not all refs are branches.

Run `git log --decorate=no`. You should see that the branch names are no longer shown at all.

The second is [`--oneline`](https://git-scm.com/docs/git-log#Documentation/git-log.txt---oneline). This flag will show you a more compact view of the log. I use this one all the time, it just makes it so much easier to see what's going on.

```bash
git log --oneline
```

## Assignment

Run `git log` with full decoration and the oneline flag.