"What's the point of having multiple [[Branch]]es?" you might ask. They're most often used to safely make changes without affecting your (or your _team's_) primary branch. However, once you're happy with your changes, you'll want to [merge](https://git-scm.com/docs/git-merge) them back into the main branch so that they make their way into the final product.


## Visual

Let's say you're in a state where you have two branches, each with their own unique commits:

```
A - B - C    main
   \
    D - E    other_branch
```

If you merge `other_branch` into `main`, Git combines both branches by creating a new commit that has _both_ histories as parents. In the diagram below, `F` is a [merge commit](https://git-scm.com/docs/git-merge#_true_merge) that has `C` and `E` as parents. `F`brings all the changes from `D` and `E` back into the `main` branch.

```
A - B - C - F    main
   \     /
    D - E        other_branch
```

# Merge Commits

A merge [[Commit]] is the result of merging two branches together.


Let's say we start with this:

```
A - B - C    main
   \
    D - E    vimchadsonly
```

And we merge `vimchadsonly` into `main` by running this while on `main`:

```bash
git switch main
git merge vimchadsonly
```

The merge will:

1. Find the "merge base" commit, or "best common ancestor" of the two branches. In this case, `A`.
2. Replay the changes from `main`, starting from the best common ancestor, into a new commit.
3. Replay the changes from `vimchadsonly` onto `main`, starting from the best common ancestor.
4. Records the result as a new commit, in our case, `F`.
5. `F` is special because it has _two parents_, `C` and `E`.

**After:**

```
A - B - C - F    main
   \     /
    D - E        vimchadsonly
```



Just as we merged branches within a single local repo, we can also merge branches between local and remote repos.

## Syntax

```bash
git merge [<remote>/<branch>]
```

For example, if you wanted to merge the `primeagen` branch of the remote `origin` into your local `main` branch, you would run this inside the local repo while on the `main` branch:

```bash
git merge origin/primeagen
```

## Assignment

1. [ ] Merge the remote `origin/main` into the local repo's `main` branch. Because we are on an empty branch, we should get a nice clean [fast-forward](https://git-scm.com/docs/git-merge#_fast_forward_merge) merge.
2. [ ] Make sure it worked with `git log`. You should see all the same commits on your local `main` branch as you do on the remote `origin/main` branch.

**Run and submit** the CLI tests from inside the new **`webflyx-local` directory**.

Boots

bootdev run eb6e6c58-4948-4438-af6e-daff6eaa10e7 -s