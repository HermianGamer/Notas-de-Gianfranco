It would be _rough_ if `.gitignore` files only accepted exact filepath section names. Luckily, they don't! [[Gitignore]]

Let's go over some of the most common patterns.

## Wildcards

The `*` character matches any number of characters except for a slash (`/`). For example, to ignore _all_ `.txt`files, you could use the following pattern:

```
*.txt
```

This would ignore files like `/princess_diaries.txt` and `/contacts/your_mom.txt` since they're both `.txt` files.

## Rooted Patterns

Patterns starting with a `/` are anchored to the directory containing the `.gitignore` file. For example, this would ignore a `main.py` in the root directory, but not in any subdirectories:

```
/main.py
```

This ignores `/main.py` but not `/src/main.py` since `/src` is a subdirectory.

## Negation

You can negate a pattern by prefixing it with an exclamation mark (`!`). For example, to ignore all `.txt` files _except_ for `important.txt`, you could use the following pattern:

```
*.txt
!/important.txt
```

This would _not_ ignore `/important.txt`, but _would_ ignore `/self_affirmations/important.txt`.

## Comments

You can add comments to your `.gitignore` file by starting a line with a `#`. For example:

```
# Ignore all .txt files
*.txt
```

Comments are especially helpful when doing something unconventional or complex, especially when collaborating.

## Order Matters

The order of patterns in a `.gitignore` file determines their effect, and patterns can override each other. For example:

```
temp/*
!temp/instructions.md
```

Everything in the `temp/` directory would be ignored _except_ for `instructions.md`. If the order were reversed, `instructions.md` would be ignored.

You can read more about the patterns that are available in the [official documentation](https://git-scm.com/docs/gitignore#_pattern_format).

## Assignment

Use this `.gitignore` file (located at the project root) to answer the question:

```
# *.js

*.txt
!names.txt

/src/main.py

content.md
```