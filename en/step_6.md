## Cooler lines

Time to add colour! Right now, your line is one colour, but the **pen** has blocks that can change its colour. With the right **operator** blocks, you can change it randomly.

The colour changing block you’re looking for is `change pen color by ` {:class="blockpen"}: 

```blocks
    change pen color by (10)
```

+ Grab one of those and put it into your `repeat until` {:class="blockcontrol"} loop, like this: 

```blocks
    repeat until <touching [edge v] ?> 
        change pen color by (10)
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly. 

+ Just put the random number operator into the `change pen color by ` {:class="blockpen"} block and pick some values to go in it. I'd try `1` and `100` to start. 

```blocks
    repeat until <touching [edge v] ?> 
        change pen color by (pick random (1) to (100))
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

+ Try running it again, watch the random rainbow!

You can actually use random numbers to make the whole program run itself over and over, changing the pattern each time! It'll look a bit like screen savers did in the 1990s... which you won't remember, but ask one of your Dojo Mentors!

You need a few changes to make this happen. The first one is that you need to set the `increase` {:class="blockdata"} and `degrees` {:class="blockdata"} variables randomly, rather than asking for them from the user. So you need to change some of your code blocks. 

+ Find this bit:

```blocks
    when green flag clicked
    set [steps v] to [0]
    ask [How many steps should I grow by?] and wait
    set [increase v] to (answer)
    ask [How many degrees should I turn?] and wait
    set [degrees v] to (answer)
    pen up
```

+ Change it to:

```blocks
    when green flag clicked
    set [steps v] to [0]
    set [increase v] to (pick random (1) to (10))
    set [degrees v] to (pick random (1) to (180))
    pen up
```

+ If you run that, you’ll find that the program does draw randomly, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the **stage**. 

+ You need another loop, that runs forever (so a `forever` {:class="blockcontrol"} block then!) outside the current one to keep it going over and over! Just drag one out of **control** and wrap your code in it. 

```blocks
    when green flag clicked
    forever 
        set [steps v] to [0]
        set [increase v] to (pick random (1) to (10))
        set [degrees v] to (pick random (1) to (180))
        pen up
        hide
        clear
        go to x: (0) y: (0)
        set pen color to [#4a6cd4]
        pen down
        repeat until <touching [edge v] ?> 
            move (steps) steps
            turn cw (degrees) degrees
            change [steps v] by (increase)
        end
    end
```


