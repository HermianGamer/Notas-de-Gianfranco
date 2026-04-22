_This is one of the most important lessons in this entire course!_ **Listen up**.

There are [[Enviroment Variable]]s that are sort of "built-in" to your [[Shell]]. By "built-in" I just mean that different programs and parts of your system know about them and use them. The `PATH` variable is one of those.

## Why Do We Care About the `PATH`?

If it weren't for the `PATH`, you'd have to remember the filesystem path of every executable you wanted to run in your shell. Instead of just running `ls`, you'd have to run `/bin/ls` (or whatever the location of the `ls` executable is on your system). That's not very convenient.

The `PATH` variable is a list of directories that your shell will look into when you try to run a command. If you type `ls`, your shell will look in each directory listed in your `PATH` variable for an executable called `ls`. If it finds one, it will just run it. If it doesn't, it will give you an error like: "command not found".

## What's in the `PATH` Variable?

Take a look at your current `PATH` variable:

```bash
echo $PATH
```

You should see a giant list of directories separated by colons (`:`). Each of those directories is a place where your shell will look for executables. For example, with a `PATH` like this:

```
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Your shell will look for executables in the following directories:

- `/usr/local/bin`
- `/usr/bin`
- `/bin`
- `/usr/sbin`
- `/sbin`


A common problem you'll run into in the future is that you install a new program on your machine, but when you try to run it from your terminal, you get an error like:

```bash
$ my-new-program
-bash: my-new-program: command not found
```

Nine times out of ten, it's because the program is installed in a directory that's not in your `PATH`variable. Oftentimes when you install a program using the CLI, it will print a message during the installation process that tells you where the command was installed. **Don't let your eyes glaze over when your terminal prints important messages!** Sometimes you just gotta [rtfm](https://www.dictionary.com/browse/rtfm).


agregar ruta a PATH
```bash
export PATH="$PATH:/path/to/new"
```

## Change PATH permanently

you changed your `PATH` variable for your current shell session. Trouble is, the next time you restart your shell, it will be reset to its default value. You won't be able to use the `worldbanc.sh` CLI Tool from anywhere unless you change your `PATH` variable _permanently_.

The most common way to do this is to add the same `export` command that you used in the last lesson to your shell's configuration file.


/Users/gianfrancoscarpati/worldbanc/private/bin/worldbanc.sh

Edit your `.zshrc` / `.bashrc` file (whatever your shell config file is) and add an `export` command to the end of the file that adds the `worldbanc/private/bin` directory to your `PATH` variable.