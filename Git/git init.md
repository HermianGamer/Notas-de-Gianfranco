
create a new [[Git]] [[repositorio]]
```bash
git init
```

You should now have a hidden `.git` directory in your directory. This means you've successfully created a new Git repository! List (`ls -a`) the contents of the directory to confirm.


 ls .git
    - Expecting exit code: 0
    - Expecting stdout to contain all of:
        - HEAD
        - config
        - hooks
        - objects
        - refs