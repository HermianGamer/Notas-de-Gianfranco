In previous courses, we've written our [[Python]] code in the _browser_, but now we're going to install Python on our local machine, and use it just like you will as a professional developer.

## Assignment

There are two versions of this lesson, one for WSL/Linux users, and one for macOS users.

### for Windows (WSL 2) / Linux Users

If you're on Linux (or Windows WSL 2), you may already have Python installed. You can verify this by running:

```bash
python3 --version
```

If that worked, you can skip ahead!

If it didn't, we'll use the default package manager, `apt`, to download python.

1. [ ] Run this command to install python3:

```bash
sudo apt update
sudo apt install -y python3
```

**Make sure to read the installation logs in case there's some step you're missing!**

2. [ ] Restart your shell to make sure the changes have taken effect.
3. [ ] Verify the installation:

```bash
python3 --version
```

You should get back a valid Python 3.x version.

**Submit** the CLI tests. There's no penalty on failure for this lesson.

### for macOS

We'll use the [Homebrew](https://brew.sh/) package manager to install Python.

1. [ ] If you don't already have [[Homebrew]], install it by running the following command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. [ ] Open your `~/.zshrc` / `~/.bashrc` file (or whatever your shell config file is) and add this line to the bottom:

```bash
export PATH="/opt/homebrew/bin:$PATH"
```

3. [ ] Restart your shell to make sure the changes have taken effect.
4. [ ] With `brew` now in your `PATH`, install Python:

```bash
brew install python3
```

5. [ ] Verify the installation:

```bash
python3 --version
```

You should get back a valid Python 3.x version.

**Submit** the CLI tests. There's no penalty on failure for this lesson.