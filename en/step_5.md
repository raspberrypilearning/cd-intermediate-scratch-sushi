## Asking for input

Ok, this is getting pretty cool, but it’s a bit boring to have to edit your code every time you want to draw a different pattern. Wouldn’t it be good to get the program to ask you for values to use? You can do that!

+ First, go to the **Data** section and create variables called `degrees`{:class="blockdata"} and `increase`{:class="blockdata"}.

+ Now add the new variables to your code like this: 

```blocks
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="blocksensing"}, which you can type a question into. 

+ Pull the `Ask and wait`{:class="blocksensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="blocksensing"}

+ Then add it to your program, just after you set `steps`{:class="blockdata"} to `0`, like this: 

```blocks
    when green flag clicked
    set [steps v] to [0]
    ask [How many steps should I grow by?] and wait
    pen up
```

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="blocksensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks. 

+ Using a `set to`{:class="blockdata"} block from **Data**, take the value of `answer`{:class="blocksensing"} and store it in the `increase`{:class="blockdata"} variable like so: 

```blocks
    ask [How many steps should I grow by?] and wait
    set [increase v] to (answer)
```

+ Now, do the same thing with `degrees`{:class="blockdata"}, asking `How many degrees should I turn?`{:class="blocksensing"} and storing the value of `answer`{:class="blocksensing"} in `degrees`{:class="blockdata"}: 

```blocks
    set [increase v] to (answer)
    ask [How many degrees should I turn?] and wait
    set [degrees v] to (answer)
```

+ Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them on a later card! 

```blocks
    when green flag clicked
    set [steps v] to [0]
    ask [How many steps should I grow by?] and wait
    set [increase v] to (answer)
    ask [How many degrees should I turn?] and wait
    set [degrees v] to (answer)
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
```

