## Mache das Ganze zufällig

Du kannst tatsächlich Zufallszahlen verwenden, um das gesamte Programm immer wieder laufen zu lassen und das Muster jedes Mal zu ändern! Es wird ein bisschen wie Bildschirmschoner in den 1990ern aussehen... an die du dich wahrscheinlich nicht erinnern wirst, aber frag einen deiner Eltern!

Du brauchst einige Änderungen, um dies zu ermöglichen. Die erste ist, dass Du die `erhöhen`{:class=„block3variables“} und `Grad`{:class=„block3variables“} Variablen zufällig festlegen musst anstatt den Benutzer danach zu fragen. Du musst also ein paar deiner Codeblöcke ändern.

\--- task \---

Entferne die Fragen aus deinem Code und aktualisiere ihn, um stattdessen Zufallszahlen zu verwenden.

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

Wenn du dein Programm jetzt ausführst, wirst du feststellen, dass es ein zufälliges Muster zeichnet, aber nur einmal. Warum denkst Du, ist das so?

Das liegt daran, dass die Schleife nur so lange läuft, bis sie den Bühnenrand erreicht.

\--- task \---

Du benötigst eine weitere Schleife, die fortlaufend läuft (also dann einen `fortlaufend`{:class="block3control"}-Block!) und zwar außerhalb der aktuellen, damit sie immer weiter läuft. Ziehe einfach einen aus dem **Steuerung** Bereich und füge den gesamten anderen Code hinzu.

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

Jetzt hast du wirklich etwas Großartiges zum Ansehen!

Möglicherweise stellst du jedoch fest, dass der Computer ab und zu etwas zeichnet, das ziemlich... schlecht aussieht. Das liegt daran, dass einige Zahlen für einige dieser Variablen einfach eine schlechte Wahl sind und dass einige **Kombinationen dieser Zahlen** auch eine schlechte Wahl sind.

Auf der nächsten Karte hilfst du dem Computer, nur gute Kombinationen auszuwählen!