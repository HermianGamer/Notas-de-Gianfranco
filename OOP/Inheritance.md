We've made it to the holy grail of [[Object Oriented Programming]]: [inheritance](https://en.wikipedia.org/wiki/Inheritance_\(object-oriented_programming\)).

Non-OOP languages like [Go](https://go.dev/) and [Rust](https://www.rust-lang.org/) support encapsulation and abstraction... almost _every_ language does. Inheritance, on the other hand, is typically unique to class-based languages like Python, Java, and Ruby.

## What Is Inheritance?

Click to hide video

Inheritance allows a "child" [[Class]], to [[Inheritance]] properties and methods from a "parent" class. It's a way to share code between classes. For example, say we have this Aircraft class:

```py
class Aircraft:
    def __init__(self, height, speed):
        self.height = height
        self.speed = speed

    def fly_up(self):
        self.height += self.speed
```

And say we want to also model more specific _kinds_ of aircraft. We could create a more specific `Helicopter` class like this:

```py
class Helicopter:
    def __init__(self, height, speed):
        self.height = height
        self.speed = speed
        self.direction = 0

    def fly_up(self):
        self.height += self.speed

    def rotate(self):
        self.direction += 90
```

Trouble is, we've rewritten a lot of the same code twice... wouldn't it be nice if a `Helicopter` could just take all the behavior from an `Aircraft`, and then just add its own unique behavior on top of that? Well, it can! We'll just make `Helicopter` a child class of `Aircraft`:

```py
class Helicopter(Aircraft):
    def __init__(self, height, speed):
        super().__init__(height, speed)
        self.direction = 0

    def rotate(self):
        self.direction += 90
```

By adding `Aircraft` in parentheses after `Helicopter`, we're saying "make `Helicopter` a child class of `Aircraft`". Now `Helicopter` inherits all the properties and methods of `Aircraft`!

The [super()](https://docs.python.org/3/library/functions.html#super) method returns a proxy of the parent class, meaning we can use it to call the parent class's constructor and other methods. So the `Helicopter`'s constructor says "first, call the `Aircraft`constructor, and then additionally set the `direction` property".

Now, say we want to create a `Jet` class. Again, because all jets are aircraft, we can inherit from `Aircraft`again. One parent class can have as many child classes as you want.

```py
class Jet(Aircraft):
    def __init__(self, speed):
        # Jets always start on the ground
        super().__init__(0, speed)

    def go_supersonic(self):
        self.speed *= 2
```


# When to Inherit

Inheritance is a powerful tool, but _do not_ overuse it (looking at you, Java devs). The rule of thumb is:

> A should only inherit from B if A is _always_ a B.

For example:

- `Cat` should inherit from `Animal` because a cat is always an animal.
- `Truck` should inherit from `Vehicle` because a truck is always a vehicle.
- `Lane` should inherit from `BadDotaPlayers` because Lane is always bad at DotA.

But these are not true, and you'll end up with a mess if you try to force them:

- `Cat` should not inherit from `Dog` because a cat is not always a dog.
- `Animal` should not inherit from `Cat` because an animal is not always a cat.
- `Allan` should not inherit from `Employed` because [Allan is not always employed](https://www.boot.dev/blog/computer-science/ai-taking-programming-jobs/#time-to-fire-my-developers-and-hire-gpt-4).

When a child class inherits from a parent, it inherits _everything_. If you only want to share _some_ functionality, inheritance should **not** be the tool you use. Just share some functions, or maybe make a new parent class that both classes can inherit from.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/drnPz4j-641x502.png)