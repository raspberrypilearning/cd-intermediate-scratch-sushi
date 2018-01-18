## Drawing loops

Now you’ve got a program that draws a line, but it only draws one line. That’s a bit dull! You can use a loop, like `forever`{:class="blockcontrol"}, to draw over and over again. Of course, if you just use `forever`{:class="blockcontrol"} then you’ll get drawings that go off the stage!

+ So you want to use a different loop, which you’ll also find in the **control** section, called `repeat until`{:class="blockcontrol"} which will do something over and over again, until a true/false condition becomes true. Wrap it around your `move`{:class="blockmotion"} and `turn`{:class="blockmotion"} blocks like so: 

```blocks
    repeat until <> 
        move (50) steps
        turn cw (15) degrees
    end
```

+ Now click the green flag to run the program a few times and see what happens! You’ll notice two things: It always starts by drawing a line into the middle of the **stage** and it doesn’t stop at the edge .

The first is because the first **motion** block that runs after the `pen down`{:class="blockpen"} is `go to x: 0 y: 0`{:class="blockmotion"}. You can fix this just by moving the `go to x: 0 y: 0`{:class="blockmotion"} block before the `pen down`{:class="blockpen"} block and adding, from **pen**, a `pen up`{:class="blockpen"} block right at the start of your code.

The second is because you haven’t yet told it what it’s checking, so the answer will never be true. Basically, right now, it’s working like a `forever`{:class="blockcontrol"} loop.

+ Time to fix your `repeat until`{:class="blockcontrol"}. You’re looking to figure out if the (invisible) sprite is touching the edge of the **stage**, so you need a **sensing** block. In this case, the `touching ?`{:class="blocksensing"} block. Snap it into your `repeat until`{:class="blockcontrol"} and select `edge`. 

```blocks
    pen down
    repeat until <touching [edge v] ?> 
        move (50) steps
        turn cw (15) degrees
    end
```

+ Change the number of steps in your program to 5 and check that it matches this one: 

```blocks
    when green flag clicked
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (5) steps
        turn cw (15) degrees
    end
```

When you run the program now you’ll see that it has turned into a circle drawing program! At least it stays on the **stage**! The problem here is that those 15 degree turns eventually add up to 360 and you turn a full circle. What needs to happen is that you take slightly longer steps each time, so you spiral out. For this, you’re going to need a **variable**.

You’ve seen **variables** before, in the Beginner series. They're basically labeled places to store numbers that you care about. You can create them in the **data** blocks category and then find their associated blocks there too.

+ Make a **variable** called `steps`{:class="blockdata"} and use its value instead of the `5` in `move 5 steps`{:class="blockmotion"}, then add `set steps to 0`{:class="blockdata"} at the start of your program and `change steps by 1`{:class="blockdata"} as part of your loop (does it matter where you put it?). 

```blocks
    when green flag clicked
    set [steps v] to [0]
    pen up
```
```blocks
    pen down
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (76) degrees
        change [steps v] by (1)
    end
```

+ Now run it, and try changing the number of degrees around (try `76` and `120`)!


