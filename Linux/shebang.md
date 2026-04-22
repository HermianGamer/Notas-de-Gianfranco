what about scripts that need to be [[Interpreted]] by another program? The computer needs to be told what program to use to interpret the [[file]].

A ["shebang"](https://en.wikipedia.org/wiki/Shebang_\(Unix\)) is a special line at the top of a script that tells your shell which program to use to execute the file.

The format of a shebang is:

```bash
#! interpreter [optional-arg]
```

For example, if your script is a Python script and you want to use Python 3, your shebang might look like this:

```zsh
#!/usr/bin/python3
```

This tells the system to use the Python 3 interpreter located at `/usr/bin/python3` to run the script.