## Coolere Linien

Zeit, Farbe hinzuzufügen! Im Moment hat deine Linie eine Farbe, aber der **Malstift** hat Blöcke, die seine Farbe ändern können. Und mit dem richtigen **Operatoren** Block kannst du die Farbe sogar zufällig ändern!

Der Block zum Ändern der **Malstift**-Farbe ist `ändere Stift Farbe um`{:class="block3extensions"}:

```blocks3
    ändere Stiftfarbe um (10)
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    wiederhole bis <wird [Rand v] berührt?> 
+      ändere Stiftfarbe um (10)
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad :: variables) Grad
        ändere [Schritte v] um (erhöhen :: variables)
    end
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    wiederhole bis <wird [Rand v] berührt?> 
+      ändere Stiftfarbe um (Zufallszahl von (1) bis (100))
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad :: variables) Grad
        ändere [Schritte v] um (erhöhen :: variables)
    end
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---