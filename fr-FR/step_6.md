## Randomise the whole thing

You can actually use random numbers to make the whole program run over and over, changing the pattern each time! It'll look a bit like screen savers did in the 1990s...which you probably won't remember, but ask one of your parents!

You need a few changes to make this happen. The first one is that you need to set the `increase`{:class="block3variables"} and `degrees`{:class="block3variables"} variables randomly rather than asking for them from the user. So you need to change some of your code blocks.

\--- task \--- Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    when green flag clicked
    set [steps v] to [0]
-    ask [How many steps should I grow by?] and wait
+    set [increase v] to (pick random (1) to (10))
-    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (pick random (1) to (180))
    pen up
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \--- You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    when green flag clicked
+    forever 
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

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!