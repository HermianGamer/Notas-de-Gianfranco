[Means](https://en.wikipedia.org/wiki/Mean) and [medians](https://en.wikipedia.org/wiki/Median) are two of the most common ways to "summarize" a group of numbers.

Click to hide video

## Mean

> The [mean (or "average")](https://en.wikipedia.org/wiki/Mean) of a group of numbers is the _sum_ divided by the _count_ of those numbers.

For example, say we have the numbers `2, 5, 1, 6, 75`:

```
2 + 5 + 1 + 6 + 75 = 89
89 / 5 = 17.8
```

The mean is `17.8`.

## Median

> The [median](https://en.wikipedia.org/wiki/Median) of a group of numbers is the _middle number_ after sorting them.

For example, say we have the numbers `2, 5, 1, 6, 75`:

1. Sort the numbers: `1, 2, 5, 6, 75`
2. The middle number is `5`, so the median is `5`.

If there is an even count of numbers, the _median_ is the _mean_ of the two middle numbers.

## Which Is Usually Best?

It feels like everyone always talks about averages... so you _might_ think that the mean is the more useful "representative" value from a group of numbers. The problem is, as you can see above, a big outlier like `75` skews the mean, while the median is less affected by it.

As a rule of thumb, the median is often a more accurate representative number of a group, especially if there are outliers in the data. It can just be a bit more work to calculate because it involves sorting instead of simple arithmetic.

## Assignment

We now need a way to show our LockedIn influencers the average (mean) follower count of the people they follow. This will help them know if they're following people who are more or less popular than them.

**Complete the `average_followers` function**.

- It should return the [average](https://en.wikipedia.org/wiki/Average) of the given list of numbers.
- If the list is empty, it should return `None`.