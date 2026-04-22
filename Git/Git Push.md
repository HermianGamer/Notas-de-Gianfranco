The `git push` command pushes (sends) local changes to any "remote" - in our case, GitHub. For example, to push our local `main` branch's commits to the remote `origin`'s `main` branch we would run:

```bash
git push origin main
```

_You need to be authenticated with the remote to push changes, which you should have done in the last lesson._

## Alternative Options

You can also push a local [[Branch]] to a [[Remote]] with a _different_ name:

```bash
git push origin <localbranch>:<remotebranch>
```

_It's less common to do this, but nice to know._

You can also _delete_ a remote branch by pushing an empty branch to it:

```bash
git push origin :<remotebranch>
```

## Assignment

Let's push our local `main` branch to the remote `origin` repo for safekeeping!

1. [ ] In your local `webflyx` repo, switch back to `main`. Its most recent commit should be G.
2. [ ] Run `git push origin main`.
3. [ ] Navigate to your GitHub repo in your browser and make sure that all the files and commits from your local `main` branch are there.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/La5X4z4-1280x452.png)

Paste in the link to your repo and **submit the tests.**