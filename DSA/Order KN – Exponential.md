`O(K^N)` – where `K` represents a constant [branching factor](https://en.wikipedia.org/wiki/Branching_factor), e.g. `3^N` – is the first Big O class that we've dealt with that falls into the scary _exponential_ category of algorithms.

Algorithms that grow at an exponential rate become impossible to compute after so little scale-up that they're usually almost worthless in practicality.

## Letter Combinations of a Phone Number

LockedIn's advertising team wants to help influencers launch paid campaigns using vanity phone numbers (think `1-800-FLOWERS`).

In order for this to work, we need to be able to take a phone number and calculate all possible sequences of letters that it could represent. Then the ad team can give influencers numbers that make brand-friendly words.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/x1LzolZ-768x621.jpg)

Each digit can represent three or four different letters. For this reason, the number of letter sequences associated with a string of digits grows very quickly as the number of digits increases. The possibilities either triple (`3^N`) or quadruple (`4^N`) with each additional digit.

|Example number|Possible letter sequences|
|---|---|
|"6"|3 (m, n, o)|
|"67"|12 (mp, mq, mr...)|
|"678"|36 (mpt, mpu, mpv...)|
|"6789"|144 (mptw, mptx...)|
|"345-6789"|3,888|

A 7-digit phone number will produce between 2,187 (`3^7`) and 16,384 (`4^7`) letter sequences – though usually closer to the low end of that range.

It's a good thing phone numbers are short! If you had a 32-digit phone number, it could form **at least ~1.85 quadrillion** letter sequences (assuming `3^N`).

Unfortunately, if we want to check all the possible combinations from a given number, there's no real shortcut for us to take – we're stuck with an exponential-class algorithm.

## Assignment

**Complete the `letter_combinations` function using the algorithm outlined below.** It takes a _string of digits_ and returns a _list of strings of letters_.

1. [ ] If the input string is empty, return an empty list.
2. [ ] Define a `result` list to hold the output strings. Have it contain just an _empty string_ to start (we need that one element to build on).
3. [ ] Iterate over the input `digits`. For each of them:
    1. [ ] If the `digit` is any invalid character, i.e. not found in the provided `digit_to_letters` dictionary, raise a `ValueError` to abort the function:
        
        ```py
        raise ValueError(f"invalid digit: {digit}")
        ```
        
    2. [ ] Get the string of `letters` that can be represented by the current digit, from `digit_to_letters`.
    3. [ ] Define a `new_result` list – empty to start with.
    4. [ ] Enter two nested `for` loops:
        - [ ] For each existing letter `combo` in `result`, iterate over each `letter` in the current digit's `letters`.
        - [ ] Append `combo + letter` to `new_result`.
    5. [ ] After the two nested loops, but still inside the main loop over `digits`, set `result` equal to `new_result`.
4. [ ] After the main loop, return the `result`.

## Reality Check

Let's return to the hypothetical 32-digit phone number, which could form ~1.85 quadrillion letter sequences at minimum – assuming the four-letter digits (7 and 9) never appear.

Even if we could process 1 million of those possible combinations per second, getting through all of them would take over **58 years**. And if we wanted to store all those strings, it would be **60+ petabytes** of data!

Though maybe storage will be cheap in the next century...