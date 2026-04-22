

The simplest type of [[Merge]] is a [fast-forward merge](https://git-scm.com/docs/git-merge#_fast_forward_merge). Let's say we start with this:

```
      C     delete_vscode
     /
A - B       main
```

And we run this while on `main`:

```bash
git merge delete_vscode
```

Because `delete_vscode` has _all the commits_ that `main` has, Git automatically does a fast-forward merge. It just moves the pointer of the "base" branch to the tip of the "feature" branch:

```
            delete_vscode
A - B - C   main
```

Notice that with a fast-forward merge, **no [merge commit](https://git-scm.com/docs/git-merge#_true_merge) is created**.

This is a common workflow when working with Git on a team of developers:

1. Create a branch for a new change
2. Make the change
3. Merge the branch back into `main` (or whatever branch your team dubs the "default" branch)
4. Remove the branch
5. Repeat



```zsh
(base) gianfrancoscarpati@MacBook-Air-de-Gianfranco webflyx % git merge update_titles

Updating 7d75bb5..e9248ba

Fast-forward

 titles.md | 1 +

 1 file changed, 1 insertion(+)
```
 
