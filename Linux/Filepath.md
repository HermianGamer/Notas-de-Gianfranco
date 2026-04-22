The output of `pwd` is a _filepath_. A filepath is a string that describes the location of a file or directory on your computer. Yours should look _something_ like this:

## Linux/Windows WSL

```
/home/wagslane
```

- The first slash (`/`) represents the _root directory_. It's the tippy-top of the filesystem tree.
- The next part (`home`) is the name of a directory inside the root directory.
- Finally, the last part (`wagslane`) is the name of a directory inside the `home` directory.

So this path represents a directory 2 levels down from the root directory:

```
root
  └── home
        └── wagslane
```
## macOS

```
/Users/wagslane
```

- The first slash (`/`) represents the _root directory_. It's the tippy-top of the filesystem tree.
- The next part (`Users`) is the name of a directory inside the root directory.
- Finally, the last part (`wagslane`) is the name of a directory inside the `Users` directory.

So this path represents a directory 2 levels down from the root directory:

```
root
  └── Users
        └── wagslane
```