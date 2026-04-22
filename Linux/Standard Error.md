["Standard Error"](https://en.wikipedia.org/wiki/Standard_streams#Standard_error_%28stderr%29), usually called "stderr", is a data stream just like standard output, but is intended to be used for _error_ messages.

It's a separate stream so that you can redirect it to a different place if need be, but by default, it prints to your [[Terminal]] just like stdout.

## Redirecting Streams

You can redirect stdout and stderr to different places using the `>` and `2>` operators. `>` redirects stdout, and `2>` redirects stderr.

### Redirect stdout to a File

```bash
echo "Hello world" > hello.txt
cat hello.txt
# Hello world
```

### Redirect stderr to a File

```bash
cat doesnotexist.txt 2> error.txt
cat error.txt
# cat: doesnotexist.txt: No such file or directory
```

In this example, `cat` is used to intentionally generate an error message (since the file doesn't exist), which is then redirected to `error.txt`.
