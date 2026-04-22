  
The [remove command](https://www.ibm.com/docs/en/aix/7.3?topic=files-deleting-rm-command) deletes a [[File]] or empty [[Directory]]:

```bash
rm some_file.txt
```

You can optionally add a `-r` flag to tell the `rm` command to delete a directory and _all_ of its contents recursively. "Recursively" is just a fancy way of saying "do it again on all of the subdirectories and their contents".

```bash
rm -r some_directory
```

For example, `rm` with the `r` and `f` flags run on the root directory (`/`), will **delete all the files on your system**. Don't do that. The `r` flag is for "recursive" (delete everything inside) and the `f` flag is for "force". Most systems will prevent you from doing this, but if you run it with `sudo`, you've just turned your computer into a very expensive paperweight.