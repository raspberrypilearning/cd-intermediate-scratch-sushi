## Vragen om input

Ok, dit wordt best gaaf, maar het is wel een beetje saai om elke keer je code aan te passen als je een ander patroon wilt tekenen. Zou het niet handig zijn om het programma om input te laten vragen? Dat kun je!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    herhaal tot <raak ik [rand v] ?>
neem (stappen) stappen
draai cw (graden ::variables) graden
verander [stappen v] met (toename ::variables)
end
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    wanneer groene vlag wordt aangeklikt
maak [stappen v] [0]
+ vraag [Hoeveel stappen moet ik nemen?] en wacht
pen op
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    vraag [Hoeveel stappen  moet ik nemen?] en wacht
+ maak [toename v] (antwoord)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    maak [toename v] (antwoord)
+ vraag [Hoeveel graden moet ik draaien?] en wacht
+ maak [graden v] (antwoord)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    wanneer groene vlag wordt aangeklikt
maak [stappen v] [0]
vraag [Hoeveel stappen moet ik nemen?] en wacht
maak [toename v] (antwoord)
vraag [Hoeveel graden moet ik draaien?] en wacht
maak [graden v] (antwoord)
pen op
verdwijn
wis alles
ga naar x: (0) y: (0)
maak penkleur [#4a6cd4]
pen neer
herhaal tot <raak ik [rand v] ?>
neem (stappen) stappen
draai cw (graden) graden
verander [stappen v] met (toename)
end
```

\--- /task \---