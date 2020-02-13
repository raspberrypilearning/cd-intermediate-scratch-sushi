## Coolere Linien

Zeit, Farbe hinzuzufügen! Im Moment hat deine Linie eine Farbe, aber der **Malstift** hat Blöcke, die seine Farbe ändern können. Und mit dem richtigen **Operatoren** Block kannst du die Farbe sogar zufällig ändern!

Der Block zum Ändern der **Malstift**-Farbe ist `ändere Stift Farbe um`{:class="block3extensions"}:

```blocks3
    ändere Stiftfarbe um (10)
```

--- task ---

Nimm einen dieser Blöcke und setze ihn in deine `wiederhole bis`{:class=„block3control“}-Schleife, wie folgt:

```blocks3
    wiederhole bis <wird [Rand v] berührt?> 
+      ändere Stiftfarbe um (10)
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad :: variables) Grad
        ändere [Schritte v] um (erhöhen :: variables)
    end
```

--- /task ---

Das ist cool, aber ein bisschen vorhersehbar. Du kannst es ein bisschen spaßiger machen, indem du eine Zufallszahl hinzufügst, sodass sich die Farbe zufällig ändert.

--- task ---

Setze den Zufallszahl **Operatoren**-Block in den `ändere Stift Farbe um`{:class="block3extensions"}-Block ein und wähle ein paar Werte die in den Block kommen. Ich würde es zu Beginn mit `1` und `100` versuchen.

```blocks3
    wiederhole bis <wird [Rand v] berührt?> 
+      ändere Stiftfarbe um (Zufallszahl von (1) bis (100))
        gehe (Schritte) er Schritt
        drehe dich nach rechts um (Grad :: variables) Grad
        ändere [Schritte v] um (erhöhen :: variables)
    end
```

--- /task ---

--- task ---

Versuche es noch einmal laufen zu lassen und beobachte den zufälligen Regenbogen!

--- /task ---