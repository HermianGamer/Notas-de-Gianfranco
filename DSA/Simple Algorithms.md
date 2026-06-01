If you've heard (usually exaggerated) stories about Leetcode and whiteboarding interviews, you might hear the word "algorithm" and think it's synonymous with "hard problem." That's really not the case, and believing it will only psych you out.

> We suffer more often in imagination than in reality
> 
> -- Seneca

Algorithms, like anything else, can be understood by breaking them down piece by piece. Take a look at the following algorithm for adding two numbers--it's dead simple:

1. Start with input variables `a` and `b`
2. Add `a` and `b` using the `+` operator, and assign the result to a new variable, `sum`
3. Return the `sum` variable

## Assignment

For the LockedIn influencer dashboard, we need to calculate the total reach of a group of influencers to estimate how many views a post will get if they all share it.

Complete the `summed` function. It's a slightly modified version of the algorithm above. Instead of just two numbers, `a` and `b`, it accepts a _list_ of numbers and returns the sum of _all of them_.

The [sum of an empty list](https://en.wikipedia.org/wiki/Empty_sum) should be 0.