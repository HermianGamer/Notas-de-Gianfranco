  
An absolute path is a path that starts at the root of the  [[Filesystem]]. On [Unix-like systems](https://en.wikipedia.org/wiki/Unix-like) (macOS/Linux), the root is denoted by a forward slash `/`. So, if the `vehicles` directory is in the filesystem root, the absolute path to the `mustang.txt` file is

```
/vehicles/cars/fords/mustang.txt
```

So, when inside the `fords` directory, you can use either this [[Filepath]]:

``` absolute
/vehicles/cars/fords/mustang.txt
```

or

``` relative
mustang.txt
```

to refer to the same file.