We're manually calling `.update()` and `.draw()` on the `player` object at the moment, which means our game [[Loop]] is going to get more and more cluttered as we add additional objects to the game. Fortunately, Pygame has a solution!

The [Group](https://www.pygame.org/docs/ref/sprite.html#pygame.sprite.Group) class is a container that holds and manages multiple game [[Object]]s. We can organize our objects into various groups to track them more easily.

You can think of them as a sort of [Venn diagram](https://en.wikipedia.org/wiki/Venn_diagram). An object can be in multiple groups at the same time! Eventually, our game's groups will look something like this:

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/sEC3wDu-758x448.png)

## Examples of Using Groups

Create a new empty group called `my_group`:

```py
my_group = pygame.sprite.Group()
```

Add all future instances of a `Player` class to two different groups (`group_a` and `group_b`):

```py
# Player is the name of the class, not an instance of it
# This must be done before any Player objects are created
Player.containers = (group_a, group_b)
```

You can iterate over objects in a group just like any other collection in Python:

```py
for thing in group:
    thing.do_something(some_value)
```

You may also call the `.update()` method for every member of a group by calling it on the group itself:

```py
group.update(dt)
```