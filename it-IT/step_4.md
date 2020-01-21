## Richiesta di immissione

Ok, questo sta diventando piuttosto interessante, ma è un po' noioso dover modificare il codice ogni volta che si desidera disegnare una forma diversa. Non sarebbe bello che il programma ti chieda i valori da usare? Ce la puoi fare!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (gradi::variables) degrees
        change [steps v] by (incrementa::variables)
    end
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [Quanti passi devo fare?] and wait
    pen up
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    ask [Quanti passi devo fare?] and wait
+    set [incrementa v] to (answer)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    set [incrementa v] to (answer)
+    ask [Quanti gradi devo girare?] and wait
+    set [Gradi v] to (answer)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    when green flag clicked
    set [steps v] to [0]
    ask [Quanti passi devo fare?] and wait
    set [incrementa v] to (answer)
    ask [Quanti gradi devo girare?] and wait
    set [Gradi v] to (answer)
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (Gradi) degrees
        change [steps v] by (incrementa)
    end
```

\--- /task \---