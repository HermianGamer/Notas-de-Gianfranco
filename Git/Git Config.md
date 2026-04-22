We need to configure [[Git]] to contain _your_ information. Whenever code changes, Git tracks _who_ made the change. To ensure you get proper credit (or more likely, blame) for all the code you write, you need to set your name and email.

Git comes with a [configuration](https://git-scm.com/docs/git-config) both at the global and the repo (project) level. Most of the time, you'll just use the global config.

## Assignment

Let's set your identity. Check if your `user.name` and `user.email` are already set using [`config get`](https://git-scm.com/docs/git-config#Documentation/git-config.txt-get):

```sh
git config get user.name
```

```sh
git config get user.email
```

If they aren't, set them using [`config set`](https://git-scm.com/docs/git-config#Documentation/git-config.txt-set). I recommend using your GitHub username and email.

```sh
git config set --global user.name "github_username_here"
git config set --global user.email "email@example.com"
```

Finally, let's set a default branch (we'll talk more about configs and branches later) so that we're all on the same page. Run:

```sh
git config set --global init.defaultBranch master
```

We're using `master` for now because it is Git's default, but later we'll change it to `main`, which is GitHub's default. Just bear with us for a second.

## Make Sure It Worked

Your `~/.gitconfig` file is the file that stores your global Git configuration. View it:

```bash
cat ~/.gitconfig
```




Git stores author information so that when you're making a commit it can track _who_ made the change. Here's how you might update your global [Git configuration](https://git-scm.com/docs/git-config) (don't do this yet):

```sh
git config set --global user.name "ThePrimeagen"
git config set --global user.email "the.primeagen@aol.com"
```

Let's take the command apart:

- `git config`: The command to interact with your Git configuration.
- `set`: The subcommand to _set_ a value – i.e., to add it if it doesn't already exist, or update it if it does.
- `--global`: Flag stating you want this configuration to be stored globally in your `~/.gitconfig`. The opposite is `--local`, which stores the configuration in the current repository only.
- `user`: The section.
- `name`: The key within the section.
- `"ThePrimeagen"`: The value you want to set for the key.

Again, this course requires a `git version` of at least `2.46.0`. See [chapter 1, lesson 2](https://www.boot.dev/lessons/0552b1c3-49d9-4d4b-b44d-e91188a79c92) for instructions.

In earlier versions of the Git CLI, the config interface used flags like `--get`, `--set`, and `--list`. Those older-style commands still work, but you may see deprecation warnings.

## Assignment

You can actually store any old data in your Git configuration. Granted, only certain keys are _used_ by Git, but you can store whatever you want.

Set the following useless key/value pairs in your _local_ Git configuration for the Webflyx repository (omit the `--global` flag to set them locally):

- `webflyx.ceo` `"ThePrimeagen"`
- `webflyx.cto` `"TheLaneagen"`
- `webflyx.valuation` `"mid"`

Git has a command to view the contents of your config:

```sh
git config list --local
```

You can also just view the contents of your local config file directly:

```sh
cat .git/config
```