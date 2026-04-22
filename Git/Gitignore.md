As you've seen, it's _pretty normal_ to use the following workflow from the top level of your repo:

1. `git add .`
2. `git commit -m "some message here"`
3. `git push origin main`

A problem arises when we want to put [[File]]s in our project's [[Directory]], but we _don't_ want to track them with Git. **A [`.gitignore`](https://git-scm.com/docs/gitignore) file solves this.** For example, if you work with Python, you probably want to ignore automatically generated files like `.pyc` and `__pycache__`. If you are building a server, you probably want to ignore `.env` files that might hold private keys. If you (I'm sorry) work with JavaScript, you might want to ignore the `node_modules` directory.


Here's example contents of a `.gitignore` file, which exists at the root of a repo:

```
node_modules
.env
```

This will ignore every path containing `node_modules` as a "section" (directory name or file name). It ignores:

- `node_modules/code.js`
- `src/node_modules/code.js`
- `src/node_modules`

It does _not_ ignore:

- `src/node_modules_2/code.js`
- `env/node_modules_3`
- `src/node_modules.js`

This will also ignore the `.env` file preventing you from committing sensitive environment variables (like API keys, DB credentials, etc.) ...cause that would be bad.


# Nested Gitignore
Your `.gitignore` file does _not_ necessarily need to be at the root of your project.

It's fairly common to have multiple `.gitignore` files in different directories throughout a project. A nested `.gitignore` file only applies to the directory it's in and its subdirectories.

Let's say you have the following setup:

```
src/
├── assets/
│   ├── .gitignore
|   ├── cover_art.jpg
│   └── onlydevs.png
├── main.py
├── tests.py
├── venv/
│   └── bin/
|       ├── activate
│       └── python
.gitignore
```

Here are the contents of `src/assets/.gitignore`:

```
onlydevs.png
main.py
```

Here are the contents of the root `.gitignore`:

```
venv/bin/activate
```

