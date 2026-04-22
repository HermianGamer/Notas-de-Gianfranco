
Sometimes a program is in _such_ a bad state (or is so malicious) that it doesn't respond to the `SIGINT`, cany [[Interrumpt]], in which case the best option is to use another [[Shell]] session (new terminal window) to manually [kill](https://www.ibm.com/docs/en/aix/7.3?topic=k-kill-command) the program.
## Syntax

```bash
kill <PID>
```
`PID` stands for "process ID". Every process that's running on your machine has a unique ID. The [ps](https://www.ibm.com/docs/en/zos/3.1.0?topic=jobs-using-ps-command), "process status" command can be used to list the processes running on your machine, and their IDs:

```bash
ps aux
```
The "aux" options just mean "show all processes, including those owned by other users, and show extra information about each process".