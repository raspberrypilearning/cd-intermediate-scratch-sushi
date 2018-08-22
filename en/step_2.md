## Using the Pen tool

The project you're going to make relies on the **Pen** tool, which is controlled by blocks in the **Pen** group. These blocks draw a line behind the centre of a sprite as it moves. You’re going to learn to use it now!

+ Open a new Scratch file, select the Scratch Cat sprite, and drag in a few of the blocks you’re familiar with from the Beginner Sushi Cards, until it looks like this: 

```blocks
    when green flag clicked
    go to x: (0) y: (0)
    move (50) steps
    turn cw (15) degrees
```

Now, time to test out the pen! 

+ From the **Pen** section, select the `pen down`{:class="blockpen"} block and add it to the start of your program, like this: 

```blocks
    when green flag clicked
    pen down
    go to x: (0) y: (0)
```

+ Now click the green flag a few times and watch what happens.

If you can see the lines behind the cat sprite, then the pen is working and you can start making it draw really cool patterns.

+ First, you should get rid of the sprite. It’s getting in the way of the drawing! Just add a `hide`{:class="blocklooks"} block from **Looks** to the start of the program and it’ll disappear. 

```blocks
    when green flag clicked
    hide
    pen down
```

Now, you can change the colour of the pen with another block from the **Pen** section, but the block is a little different to the others you’ve seen. It’s the `set pen color to `{:class="blockpen"} block and looks like this: 

```blocks
    set pen color to [#4a6cd4]
```

+ Drag one into your sprite panel, and snap it in above of the `pen down`{:class="blockpen"} block. 

```blocks
    when green flag clicked
    hide
    set pen color to [#4a6cd4]
    pen down
```

+ Now, click on the box of colour (in the code above it’s the blue one), and you’ll see the mouse pointer turn into a hand.

+ Move the pointer around the screen and notice how the colour in the box changes to the colour of whatever the pointer hovers over. When you click, Scratch will save that colour as the colour of your pen.

If you’ve been clicking on the green flag to test your code, you’ll have noticed that the drawings the pen makes don’t go away. 

+ Add a `clear`{:class="blockpen"} block from the **Pen** section to the start of your code to take care of that:

```blocks
    when green flag clicked
    clear
    hide
```
