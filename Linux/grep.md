You might be used to nice graphical interfaces that allow you to search for text in files, usually with `ctrl+f` or `cmd+f`. But what about when you're working on a terminal?

As it turns out, once you're used to it, searching for text in [[File]] on a CLI can be much faster than using a GUI.

## The grep Command

The [grep command](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix) allows you to search for text in files. It has a _ton_ of capability, and we'll only be scratching the surface of its true power.

### Basic Usage

The most basic use for `grep` is to search for a string in a file. For example, if we wanted to search for the word "hello" in the file `words.txt`, we could run:

```bash
grep "hello" words.txt
```

This will print out every line in `words.txt` that contains the word "hello". It's a case-sensitive search, so it will only match "hello", not "Hello" or "HELLO".

# grep Multiple Files

You can also search multiple files at once. For example, if we wanted to search for the word "hello" in `hello.txt` and `hello2.txt`, we could run:

```bash
grep "hello" hello.txt hello2.txt
```

## Recursive Search

You can also search an entire directory, including all subdirectories. For example, to search for the word "hello" in the current directory and all subdirectories:

```bash
grep -r "hello" .
```

_The `.` is a special alias for the current directory._


You'll want to include all of the files in the `worldbanc/private/transactions`directory, but _not_ the files in the `backups` directory. Use the [`--exclude-dir`](https://www.gnu.org/software/grep/manual/grep.html#index-_002d_002dexclude_002ddir) flag:

```bash
grep -R "Bob" PATH_TO_TRANSACTIONS_DIR --exclude-dir="backups"
```