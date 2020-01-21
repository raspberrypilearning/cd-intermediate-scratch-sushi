## Mache das Ganze zufällig

Du kannst tatsächlich Zufallszahlen verwenden, um das gesamte Programm immer wieder laufen zu lassen und das Muster jedes Mal zu ändern! Es wird ein bisschen wie Bildschirmschoner in den 1990ern aussehen... an die du dich wahrscheinlich nicht erinnern wirst, aber frag einen deiner Eltern!

Du brauchst einige Änderungen, um dies zu ermöglichen. Die erste ist, dass Du die `erhöhen`{:class=„block3variables“} und `Grad`{:class=„block3variables“} Variablen zufällig festlegen musst anstatt den Benutzer danach zu fragen. Du musst also ein paar deiner Codeblöcke ändern.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    Wenn die grüne Flagge angeklickt
    setze [Schritte v] auf [0]
-   frage [Um wie viele Schritte soll ich wachsen?] und warte
+  setze [erhöhen v] auf (Zufallszahl von (1) bis (10))
-   frage [Um wie viel Grad soll ich mich drehen?] und warte
+  setze [Grad v] auf (Zufallszahl von (1) bis (180))
    schalte Stift aus
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    Wenn die grüne Flagge angeklickt
+   wiederhole fortlaufend 
        setze [Schritte v] auf [0]
        setze [erhöhen v] auf (Zufallszahl von (1) bis (10))
        setze [Grad v] auf (Zufallszahl von (1) bis (180))
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
    end
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!