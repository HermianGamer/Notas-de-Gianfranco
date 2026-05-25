A [symbolic link](https://en.wikipedia.org/wiki/Symbolic_link), usually called a **symlink** for short, is a special kind of file that points to another file or directory.
[[CLI]]
It's a lot like a shortcut in a GUI. The symlink has its own path, but when you use it, the operating system follows the link to the target.

## Link Command

The [`ln` command](https://www.ibm.com/docs/en/aix/7.3.0?topic=l-ln-command) creates links. To create a _symbolic_ link, use the `-s` flag:

```sh
ln -s target_path link_path
```

Note, **the path to the target comes first**, then the path where the symlink will be created. For example:

```sh
ln -s documents/important.txt important.txt
```

That creates a symlink in the current directory named `important.txt`, which points to `documents/important.txt`.

You can use either a relative or an absolute path for the target. Both options have tradeoffs!

If you use an absolute path, you can usually move the symlink without a problem, but moving the target will _break_ the symlink. If you use a relative path, the symlink will continue to work as long as its position _relative to the target_ stays the same. For example, you could move a parent directory containing both the symlink and the target.

## Symlinks vs. Copies

A symlink is _not_ the same as a _copy_: it doesn't duplicate the file's contents. It just creates **another path that points to the original**. That means:

- If the target file changes, the symlink shows the new contents.
- If you delete the symlink, the target file still exists.
- If you delete the target file, the symlink breaks.

You can use `ls -l` to see where a symlink points:

```text
important.txt -> documents/important.txt
```