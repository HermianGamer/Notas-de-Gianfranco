The [move command](https://www.ibm.com/docs/en/aix/7.3?topic=files-moving-renaming-mv-command) moves a file or [[Directory]] from one location to another. You can use it to rename a [[File]] or to move it to a different [[Directory]] altogether. Your working directory can't be the directory you're moving.

Renaming a file:

```bash
mv some_file.txt some_other_name.txt
```

Moving a file from the current directory to another nested directory:

```bash
mv some_file.txt some_directory/some_file.txt
```

Moving a file from the current directory, to the parent directory:

```bash
mv some_file.txt ../some_file.txt
```

If you don't want to rename the file and you're just moving it to a different directory, you can omit the filename:

```bash
mv some_file.txt some_directory/
```