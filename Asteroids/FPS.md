  
As it stands, our game is re-drawing the screen as fast as it possibly can. This causes it to use a lot more CPU than it actually needs!

## Delta Time

The Greek letter delta (Δ) is often used to represent a change in a value in mathematics. In game development, we use "delta time" to represent the amount of time that has passed since the last frame was drawn. This value is useful to **decouple** the game's speed from the speed it's being drawn to the screen.

If your computer's CPU _speeds up_ (its speed is not constant, like a sprinter running as fast as they can), the asteroids shouldn't _also_ speed up. Conversely, if your computer _slows down_, the asteroids shouldn't also slow down: they may just move less smoothly.