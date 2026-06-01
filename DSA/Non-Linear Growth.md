Exponents are important to understand when it comes to the _execution speed_ of an algorithm. If the number of operations grows quickly as the amount of input data increases, the algorithm will become slower and slower.

|Linear|Quadratic|
|---|---|
|`2 * 2 = 4`|`2 ** 2 = 4`|
|`3 * 2 = 6`|`3 ** 2 = 9`|
|`4 * 2 = 8`|`4 ** 2 = 16`|
|`5 * 2 = 10`|`5 ** 2 = 25`|
|`6 * 2 = 12`|`6 ** 2 = 36`|
|`7 * 2 = 14`|`7 ** 2 = 49`|
|`8 * 2 = 16`|`8 ** 2 = 64`|
|`9 * 2 = 18`|`9 ** 2 = 81`|

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/HV3CXvi-560x400.png)

- The doubling formula, `2*x`, results in _linear_ or _straight_ growth.
- The quadratic formula, `x^2`, keeps growing _faster and faster_.

## What Does This Have to Do With Code?

Generally we try to avoid writing code that causes the usage of a resource to grow quadratically (with an exponent).

- Sometimes that's a lot of computations (CPU utilization / slowness).
- Sometimes that's a lot of memory usage (RAM utilization)
- Sometimes that's a large storage requirement (disk space)

_A notable exception is in cryptography and security: we want to force attackers to waste resources trying to get at our information._