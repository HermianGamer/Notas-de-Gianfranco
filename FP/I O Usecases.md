A program that doesn't do _any_ [[Input and Output]] is pretty useless. What's the point of computing something if you can't see the results?

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/5nZy0Kx-430x400.png)

In [[Functional Programming]], i/o is viewed as _dirty_ but _necessary_. We know we can't _eliminate_ i/o from our code, so we just _contain_ it as much as possible. There should be a clear place in your project that does nasty i/o stuff, and the rest of your code can be pure.

For example, a Python program might:

1. Read a file from the hard drive as the program starts
2. Run a bunch of pure functions to analyze the data
3. Write the results of the analysis to a file on the hard drive at the end

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/45emq7q-594x400.png)