[Object-Oriented Programming](https://en.wikipedia.org/wiki/Object-oriented_programming), or "OOP", is a pattern for (allegedly) writing **clean and maintainable code**.

Admittedly, not everyone _agrees_ that object-oriented programming is the best way to write code, but, to be a good engineer, you should at least _understand_ it.

Throughout this course, we'll be coding small bits of a [real-time strategy game](https://en.wikipedia.org/wiki/Real-time_strategy) called "Age of Dragons". Players control armies of humans, elves, orcs, and dragons in top-down battles. It's similar to Age of Empires or StarCraft.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/LmOR0sn-960x720.jpeg)

## Assignment

One of the greatest sins when trying to write "clean code" is using misleading variable and function names. Take a look at the `destroy_wall` function. It takes a list of numbers as input (each representing the health of a wall) and returns a new list with each entry of `0` or less removed.

Based on its name, you might assume that `destroy_wall` destroys a _single_ wall, but if you look closely, you'll see that it handles _multiple_ walls.

1. [ ] The test suite expects a different function name. Take a look at the `main_test.py` file to see what it's looking for, and rename the function accordingly.
2. [ ] Bonus: rename the variables _inside_ the function to be more descriptive.

## Solution

```
def destroy_walls(wall_healths):
	new_wall_healths = []
    for wall_health in wall_healths:
        if wall_health > 0:
            new_wall_healths.append(wall_health)
    return new_wall_healths
```
