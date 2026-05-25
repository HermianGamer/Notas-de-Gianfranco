It would be a _massive_ pain if we had to fit all of our code into a single file. So, let's organize our code into separate [modules](https://docs.python.org/3/tutorial/modules.html).

Since each `.py` [[File]] is a module, we can group related [[Function]], variables, and classes together in a module. Then, other modules can [[Import]] them using the syntax:

```py
from directory_name.module_name import my_function
# or import everything: from module_name import *
```
