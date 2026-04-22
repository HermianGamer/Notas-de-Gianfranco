A package manager is a software tool that helps you install other software. Its primary functions include:

- Downloading software from official sources
- Installing software
- Updating software
- Removing software
- Managing dependencies

As a developer, you'll frequently use package managers to get access to the software you need to get your work done.

## APT (Ubuntu)

APT, or "Advanced Package Tool", is the primary package manager for Ubuntu. To be fair, you can use other package managers on Ubuntu, but APT is the default and most common.

If you're on WSL and Ubuntu, you'll be using APT. If you're on another Linux setup, I pray you already know what package manager you're using. If you're on WSL or Ubuntu, check to make sure you have APT installed by running the following command:

```bash
apt --version
```

## Brew (macOS)

There isn't a "default" package manager for macOS. The most popular (but unofficial) package manager is [Homebrew](https://brew.sh/).

If you're on macOS, and you don't have [[Homebrew]] installed, you can install it by running the following command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

See the [Homebrew](https://brew.sh/) site for more information if needed.

## Assignment

Let's install something! [Neovim](https://neovim.io/) is a hyperextensible (and newer) version of Vim, which is a "new" version of Vi, which is a popular command line text editor.

### WSL/Ubuntu Instructions

First, make sure that `apt` itself is up to date and will install the latest version of Neovim. Run the following command:

```bash
sudo apt update
```

This command only updates `apt`, it doesn't upgrade anything.

Next, install Neovim:

```bash
sudo apt install neovim
```
### macOS Instructions

If you're using Homebrew, on Mac, you can install Neovim by running the following command:

```bash
brew install neovim
```

### Other Installation Methods

If the above methods don't work, you can try [other installation methods](https://github.com/neovim/neovim/blob/master/INSTALL.md).


Apt and Brew aren't the only package managers out there. There are many, many more, though they do happen to be two of the most popular, especially on Linux and macOS.

## How Does a Package Manager Work?

When you type a command like `apt install neovim`, the package manager will:

1. Check to see if the package is already installed.
2. If it's not installed, it will download the package from a repository.
3. It will install the package on your computer.
4. It will install any dependencies that the package needs to run.
5. It will (hopefully) add the package to your PATH if it should be there.

Good package managers keep track of what packages you have installed, and what versions of those packages you have installed. They keep your filesystem nice and tidy, making sure you haven't installed 10 different instances of the same package or application.

For your edification, take a look at where your package manager installed `nvim` on your filesystem. The `which` command will help:

```bash
which nvim
```