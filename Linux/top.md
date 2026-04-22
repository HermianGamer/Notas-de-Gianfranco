The [`top`](https://man7.org/linux/man-pages/man1/top.1.html) command is a powerful tool that allows you to see which programs are using the most resources on your computer.

I use the [`top`](https://man7.org/linux/man-pages/man1/top.1.html) command _all the time_, both on my local machine and on remote servers to diagnose performance issues. If you've ever opened up your task manager on Windows or Activity Monitor on macOS, `top` is similar, but for the command line.

## Assignment

1. [ ] Open your terminal and run the `top` command.

Notice that the `top` command runs in a loop, updating the information every few seconds.

By default, `top` sorts the processes by CPU usage, with the most CPU-intensive processes at the top. Another useful resource to sort by is memory (RAM) usage. To sort by memory usage, press `M` (uppercase) while `top` is running. On macOS, you can either start `top` sorted by memory with `top -o mem` from the [[Shell]], or, while `top` is running, press `o`, then type `mem` and press Enter to sort by memory. muestra tambien el [[PID]]

What programs on your computer are using the most CPU and memory? Poke around a bit and see what you can find.

2. [ ] Copy the column names from your terminal (the header row of the `top` command's output, which contains the column titles) and paste them into the text box on the right. **Note: if your terminal window is too narrow, you might be missing some columns.**

Don't submit yet.

3. [ ] Exit the `top` command by pressing `q`.

Submit the column names you copied in the text box on the right.

## Troubleshooting

- `top` might _not_ print some columns if your terminal window isn't wide enough to fit them. Try to resize your window or zoom out (reduce font size) and **ensure that you print all columns.** Otherwise, your submission might fail.
    
- If you resize your terminal window while `top` is running, make sure to quit and restart the `top` command to ensure all columns are displayed correctly.
    
- If your system is set up with a non-English locale, make sure that your printed output matches the expected by running this instead:
    

```sh
LANG=C top
```