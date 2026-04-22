The [chmod command](https://www.ibm.com/docs/en/aix/7.3?topic=c-chmod-command) lets you change the [[permissions]] of a [[File]] or [[Directory]]. It's short for "change mode" (I wish it was called "change permissions", but alas).
```bash
chmod -R u=rwx,g=,o= DIRECTORY
```

In the command above, `u` means "user" (aka "owner"), `g` means "group", and `o`means "others". The `=` means "set the permissions to the following", and the `rwx` means "read, write and execute". The `g=` and `o=` mean "set group and other permissions to nothing". The `-R` means "recursively", which means "do this to all of the contents of the directory as well".

Be sure to replace `DIRECTORY` with the path to the `private` directory.

_Remember, `.` is a special alias for the current directory._

There seems to be a suspicious script in the `worldbanc/private/bin`directory called `genids.sh`. It looks like it generates some type of identifier... First, let's **remove our ability to run it**, just to see what happens. The `chmod`command has a convenient `-x` flag that will simply remove the executable permission from the file.

1. [ ] Run the following commands in `worldbanc/private/bin`:

```bash
chmod -x genids.sh
```

2. [ ] Let's test those permission changes. Try to run the script:

```bash
./genids.sh
```

You should get an error like this:

```bash
permission denied
```

3. [ ] That error occurs because the executable permission has been removed. Let's re-add the executable permission for the owner:

```bash
chmod u+x <filename>
```

4. [ ] Once you've done that, try running the `./genids.sh` script again.