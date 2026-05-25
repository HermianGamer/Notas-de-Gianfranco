  
Here are some standard library functions you'll find helpful:

- [`os.path.abspath()`](https://docs.python.org/3/library/os.path.html#os.path.abspath): Get an absolute path from a relative path
- [`os.path.join()`](https://docs.python.org/3/library/os.path.html#os.path.join): Join two paths together safely (handles slashes)
- [`os.path.normpath()`](https://docs.python.org/3/library/os.path.html#os.path.normpath): Normalize a path (handles things like `..`)
- [`os.path.commonpath()`](https://docs.python.org/3/library/os.path.html#os.path.commonpath): Get the common sub-path shared by multiple paths
- [`os.path.isdir()`](https://docs.python.org/3/library/os.path.html#os.path.isdir): Check if a path points to an existing directory
- [`os.listdir()`](https://docs.python.org/3/library/os.html#os.listdir): List the contents of a directory
- [`os.path.getsize()`](https://docs.python.org/3/library/os.path.html#os.path.getsize): Get the size of a file (in bytes)
- [`os.path.isfile()`](https://docs.python.org/3/library/os.path.html#os.path.isfile): Check if a path points to an existing regular file
- [`open()`](https://docs.python.org/3/library/functions.html#open): Open a file for reading or writing
- [`.read()`](https://docs.python.org/3/library/io.html#io.TextIOBase.read): Read a text file to a string, optionally specifying a maximum number of characters
- [`os.makedirs()`](https://docs.python.org/3/library/os.html#os.makedirs): Create a directory, along with any necessary parent directories (note the optional `exist_ok` argument)
- [`os.path.dirname()`](https://docs.python.org/3/library/os.path.html#os.path.dirname): Get the parent directory of a given path
- [`.write()`](https://docs.python.org/3/library/io.html#io.TextIOBase.write): Write a string to a text file