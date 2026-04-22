1. [ ] Edit the [[File]] you believe to be your shell configuration file. You can use the `nano`command to edit files in your [[Terminal]]:

```bash
nano ~/.bashrc ##bash
nano ~/.zshrc ##zsh
```

2. [ ] Add the following line to the bottom:

```zsh
echo "Hello from the shell!"
```

You can use `Ctrl+O` to save the file (confirm any prompts with "enter"), and then `Ctrl+X` to exit the editor. (There should be a list of commands at the bottom of the screen.)

3. [ ] Close your terminal and open a new one. If you see the message "Hello from the shell!", you've found the right file!
4. [ ] Edit `~/.bashrc` again to remove the line you added to the file so that you don't see that message every time you open a new shell.

