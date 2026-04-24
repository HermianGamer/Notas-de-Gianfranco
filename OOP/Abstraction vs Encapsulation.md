- [[Abstraction]] is about _creating a simple interface for complex behavior._ It focuses on what's exposed (public).
- [[Encapsulation]] is about _hiding internal state._ It focuses on tucking away the implementation details (private).

Click to hide video

Abstraction is more about reducing complexity, encapsulation is more about maintaining the integrity of system internals.

In my personal opinion, it's a bit of a distinction without a difference... but "abstraction" is a more broadly used term, and in my view at least, it's also a more general term for "making something easier to use by adding a layer on top".

## Are We Encapsulating or Abstracting?

Both. We are almost always doing both. Here's an example of using the `random` library to generate a random number:

```py
import random

attack_damage = random.randrange(5)
```

[Generating random numbers](https://www.boot.dev/blog/computer-science/what-is-entropy-in-cryptography/) is a _really hard_ problem. The operating system uses the physical hardware of the computer to create a [seed](https://en.wikipedia.org/wiki/Random_seed) for the randomness. However, the developers of the `random` library have _abstracted_ that complexity away and _encapsulated_ it within the simple `randrange` function. We just say "I want a random number from 0 to 4" and the library does it.

When writing libraries for other developers to use, getting the abstractions right is _critical_ because changing them later can be disastrous. Imagine if the maintainers of the `random` module changed the input parameters to the `randrange` function! It would break code used by thousands of applications around the world.



The terms "abstraction" and "encapsulation" mostly just emphasize different aspects of the same concept:

- Abstraction focuses on exposing essential features while hiding complexity
- Encapsulation focuses on bundling data with methods and restricting direct access to implementation details

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/WOSsjXl-364x400.png)

Creating good abstractions is particularly crucial when you're developing libraries for other developers to use. For example, the built-in [`pow`](https://docs.python.org/3/library/functions.html#pow) function in Python is an abstraction that hides the complexity of calculating [exponents](https://www.mathplanet.com/education/pre-algebra/discover-fractions-and-factors/powers-and-exponents).

`pow` isn't magic. Somewhere, code that does _something like this_ exists and is called when you use `pow`:

```py
def pow(base, exponent):
    result = 1
    for _ in range(exponent):
        result *= base
    return result
```