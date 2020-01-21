## Bitte um Eingabe

Ok, das wird ziemlich cool, aber es ist etwas langweilig, wenn du deinen Code jedes Mal ändern musst, wenn du ein anderes Muster zeichnen möchtest. Wäre es nicht gut, wenn das Programm dich nach Werten fragen würde, die es nutzen soll? Das kannst du machen!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    wiederhole bis <wird [Rand v] berührt?>  
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad :: variables) Grad
        ändere [Schritte v] um (erhöhen :: variables)
end
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    Wenn die grüne Flagge angeklickt
    setze [Schritte v] auf [0]
+  frage [Um wie viele Schritte soll ich wachsen?] und warte
    schalte Stift aus
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    frage [Um wie viele Schritte soll ich wachsen?] und warte
+   setze [erhöhen v] auf (Antwort)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    setze [erhöhen v] auf (Antwort)
+   frage [Um wie viel Grad soll ich mich drehen?] und warte
+   setze [Grad v] auf (Antwort)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    Wenn die grüne Flagge angeklickt
    setze [Schritte v] auf [0]
    frage [Um wie viele Schritte soll ich wachsen?] und warte
    setze [erhöhen v] auf (Antwort)
    frage [Um wie viel Grad soll ich mich drehen?] und warte
    setze [Grad v] auf (Antwort)
    schalte Stift aus
    verstecke dich
    lösche alles
    gehe zu x: (0) y: (0)
    setze Stiftfarbe auf [#4a6cd4]
    schalte Stift ein
    wiederhole bis <wird [Rand v] berührt?>  
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad) Grad
        ändere [Schritte v] um (erhöhen)
    end
```

\--- /task \---