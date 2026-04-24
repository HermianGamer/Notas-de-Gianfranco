In Python, each `.py` file is a **module**, and we can import [[Functions]], variables, and classes from one module into another with the [`import`](https://docs.python.org/3/reference/simple_stmts.html#import) statement. The name of a module is the filename (without the `.py`extension).

For example, pretend we had a `database.py` file with a top-level function called `connect` and a variable called `db_version`. We could _import_ those into another file (like a `main.py` file) like this:

```py
# Import the `connect` function and `db_version` variable from the `database.py` file
from database import connect, db_version
```

Or, if we want to import _everything_ from a module, we can use the `*` character:

```py
# Import everything from the `database.py` file into the current file
from database import *
```

I recommend [avoiding "wildcard imports" (using the `*`)](https://peps.python.org/pep-0008/#imports), because they make your code harder to read. It's better to be explicit when possible.