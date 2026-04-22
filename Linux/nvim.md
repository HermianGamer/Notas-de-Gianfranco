This isn't a course on [Neovim](https://neovim.io/) (we'd need **at least** 420 more lessons for that), but let's at least figure out how to edit a [[File]] and exit the program.

Don't be fooled, exiting Vim (or Neovim) is one of the greatest hurdles you must overcome as a developer. It's a rite of passage. It's a badge of honor.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/EOHr7WG-583x344.jpg)

## Assignment

There's a public file containing a company password!

1. [ ] Use Neovim to open the `worldbanc/public/company_info.md` file.

It's a text file that's using [markdown](https://www.markdownguide.org/) syntax. You can open a file with Neovim by passing in the file path as an argument:

```bash
nvim FILEPATH_HERE
```

Once it's open, you might notice that you can't type anything. That's because you're in "normal" mode, the mode for navigating and manipulating text.

2. [ ] Use the arrow keys (I know, Vim sacrilege) to move your cursor down to the last line.
3. [ ] Enter "insert" mode by pressing the `i` key. You should see `-- INSERT --` appear at the bottom of the screen.
4. [ ] You should now be able to delete the password. Replace just the password with the text `REDACTED` in all caps, no quotes.
5. [ ] When you're done, press the `esc` key to return to normal mode.
6. [ ] Then type `:w` and press enter to save your changes.
7. [ ] Finally, type `:q` and press enter to quit Neovim.

You've successfully edited a file (and escaped from) Neovim!

## Check Installation

Let's make sure we installed it properly. Check your version:

```bash
nvim --version
```

Paste the entire output into the input field and submit it.
