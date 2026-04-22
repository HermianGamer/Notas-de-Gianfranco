  
The [`touch`](https://man7.org/linux/man-pages/man1/touch.1.html) command updates the access and modification timestamps of a [[File]]. By default, if the specified file does not exist, `touch` will create an empty file with the given filename. Because of this side-effect, you’ll often see this command used to quickly create new empty files.

```bash
touch new_file.txt
```

You can also create multiple files at once by listing them:

```bash
touch some_file.txt some_other_file.txt
```