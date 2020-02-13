## Bitte um Eingabe

Ok, das wird ziemlich cool, aber es ist etwas langweilig, wenn du deinen Code jedes Mal ändern musst, wenn du ein anderes Muster zeichnen möchtest. Wäre es nicht gut, wenn das Programm dich nach Werten fragen würde, die es nutzen soll? Das kannst du machen!

--- task ---

Gehe zuerst zum Abschnitt **Variablen** und erstelle Variablen mit den Namen `Grad`{:class="block3variables"} und `erhöhen`{:class="block3variables"}.

--- /task ---

--- task ---

Füge die neuen Variablen nun wie folgt in deinen Code ein:

```blocks3
    wiederhole bis <wird [Rand v] berührt?>  
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad :: variables) Grad
        ändere [Schritte v] um (erhöhen :: variables)
end
```

--- /task ---

Jetzt musst du nach Werten für diese beiden Variablen fragen und diese speichern. Dazu verwendest du einen **Fühlen**-Block mit dem Namen `frage und warte`{:class="block3sensing"}, in den du eine Frage eingeben kannst.

--- task ---

Ziehe den `frage und warte`{:class="block3sensing"}-Block in dein Figur-Panel und ändere die Frage zu `Um wie viele Schritte soll ich wachsen?`{:class="block3sensing"}

Füge ihn dann zu deinem Programm hinzu, direkt nachdem du die `Schritte`{:class="block3variables"} auf `0` setzt, wie folgt:

```blocks3
    Wenn die grüne Flagge angeklickt
    setze [Schritte v] auf [0]
+  frage [Um wie viele Schritte soll ich wachsen?] und warte
    schalte Stift aus
```

--- /task ---

Jetzt da du dein Programm eine Frage stellen lässt, musst dafür sorgen, dass es sich die Antwort merkt! Es stellt sich heraus, dass Scratch eine spezielle Variable namens `Antwort`{:class="block3sensing"} hat, in der die letzte Antwort gespeichert wird, die es erhalten hat. Du kannst diese Variable unter den **Fühlen** Blöcken finden.

--- task ---

Nimm den Wert von `Antwort`{:class="block3sensing"} und speichere ihn in der `erhöhen`{:class="block3variables"} Variable, indem du einen `setze auf`{:class="block3variables"}-Block aus dem **Variablen**-Bereich verwendest, wie folgt:

```blocks3
    frage [Um wie viele Schritte soll ich wachsen?] und warte
+   setze [erhöhen v] auf (Antwort)
```

--- /task ---

--- task ---

Mache jetzt dasselbe mit `Grad`{:class="block3variables"}, frage `Um wie viel Grad soll ich mich drehen?`{:class="block3sensing"} und speichere den Wert von `Antwort`{:class="block3sensing"} in `Grad`{:class="block3variables"}:

```blocks3
    setze [erhöhen v] auf (Antwort)
+   frage [Um wie viel Grad soll ich mich drehen?] und warte
+   setze [Grad v] auf (Antwort)
```

--- /task ---

--- task ---

Überprüfe, ob dein Programm jetzt aussieht wie das unten dargestellte, und führe es einige Male mit unterschiedlichen Zahlen aus. Schreibe die Antworten auf, die die coolsten Bilder ergeben. Du wirst sie in einem späteren Schritt brauchen!

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

--- /task ---