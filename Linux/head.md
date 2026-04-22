The [head](https://www.ibm.com/docs/en/aix/7.3?topic=h-head-command) command prints the first `n` lines of a [[File]]. The `-n` flag specifies `n` as shown:

```bash
head -n 10 file1.txt
```

If you don't specify a number using the `-n` flag, it will default to `10`.