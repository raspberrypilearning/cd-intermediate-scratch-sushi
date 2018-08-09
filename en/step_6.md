## Cooler lines

Time to add colour! Right now, your line is one colour, but the **Pen** has blocks that can change its colour. And with the right **Operator** block, you can even change the colour randomly!

The block for changing the **Pen** colour is `change pen color by `{:class="blockpen"}: 

```blocks
    change pen color by (10)
```

+ Grab one of those and put it into your `repeat until`{:class="blockcontrol"} loop, like this: 

```blocks
    repeat until <touching [edge v] ?> 
        change pen color by (10)
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly. 

+ Just put the random number **Operator** block into the `change pen color by `{:class="blockpen"} block and pick some values to go in it. I'd try `1` and `100` to start. 

```blocks
    repeat until <touching [edge v] ?> 
        change pen color by (pick random (1) to (100))
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

+ Try running it again, and watch the random rainbow!
