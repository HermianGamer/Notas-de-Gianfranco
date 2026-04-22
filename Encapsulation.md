[Encapsulation](https://en.wikipedia.org/wiki/Encapsulation_\(computer_programming\)) is the practice of hiding complexity inside a ["black box"](https://en.wikipedia.org/wiki/Black_box) so that it's easier to focus on the problem at hand.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/8gu3Y0s-964x544.png)

The simplest example of encapsulation is a function. The caller of a function doesn't need to worry too much about what happens inside, they just need to understand the inputs and outputs.

```py
# who even knows how this function works???
# I sure don't, I just call it and assume
# it calculates the acceleration correctly
acceleration = calc_acceleration(initial_speed, final_speed, time)
```

To _use_ the `calc_acceleration` function, we don't need to think about each line of code inside the function definition. We just need to know that if we give it the inputs:

- `initial_speed`
- `final_speed`
- `time`

It will produce the correct `acceleration` as an output.

[[Public vs Private]]


# Not Security

Encapsulation is all about making code easy to work with by "hiding" complicated code within a ["black box"](https://en.wikipedia.org/wiki/Black_box). It makes it so that we don't have to worry about details of how a function or method works... we just _use_ it.

It's kinda like how the inner workings of your car's power steering are hidden from you. You don't need to be an expert on hydraulic systems to turn the wheel from side to side.

Let me say this next part loud and clear:

_Encapsulation and the concepts of private and public members have **NOTHING** to do with security_. This really confused me as a new developer. Just as the casing on your computer hides its inner workings but doesn't _stop_ you from opening the case and looking inside, encapsulation doesn't stop anyone from knowing how your code works, it just puts it all in one easy to find place.

**Encapsulation is about organization, not security.**

Encapsulation is like storing folders in an _unlocked_ filing cabinet. The cabinet doesn't stop anyone from peeking inside, but it does keep everything tidy and easy to find.

