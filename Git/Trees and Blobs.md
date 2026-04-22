Now that we understand some of our [[Git]] plumbing equipment, let's get into the pipes. Here are some terms to know:

- `tree`: git's way of storing a [[Directory]]
- `blob`: git's way of storing a [[File]]

Here's what I got when I inspected my last commit:

```bash
> git cat-file -p 5ba786fcc93e8092831c01e71444b9baa2228a4f

tree 4e507fdc6d9044ccd8a4a3061324c9f711c4667d
author ThePrimeagen <the.primeagen@aol.com> 1705891256 -0700
committer ThePrimeagen <the.primeagen@aol.com> 1705891256 -0700

A: add contents.md
```

Notice that we can see:

- The `tree` object
- The `author`
- The `committer`
- The commit message

However, we _cannot_ see the contents of the `contents.md` file itself! That's because the `blob` object stores it.

1. [ ] Use `git cat-file -p` again, but this time with the hash of the `tree` object instead of the commit hash. You should see a `blob` object with _its_ own hash.
2. [ ] Use `git cat-file -p` again, using the `blob` object's hash to view its contents.