## Das Stiftwerkzeug verwenden

Das Projekt, das Du erstellen wirst, basiert auf dem **Malstift**-Werkzeug, das eine Linie hinter der Mitte einer Figur zieht, während sie sich bewegt. Du wirst jetzt lernen, es zu benutzen!

--- task ---

Öffne eine neue Scratch-Datei, wähle die Scratch Katzen Figur aus und ziehe einige Blöcke hinein, die du vielleicht bereits gesehen hast, bis es so aussieht:

```blocks3
    Wenn die grüne Flagge angeklickt
gehe zu x: (0) y: (0)
gehe (50) er Schritt
drehe dich nach rechts um (15) Grad
```

--- /task ---

Zeit, den Stift auszuprobieren!

Um die Malstiftblöcke in Scratch zu verwenden, musst du die **Malstift-Erweiterung** hinzufügen.

--- task ---

Klicke auf die **Erweiterung hinzufügen** Schaltfläche in der unteren linken Ecke.

![Erweiterungstaste hervorgehoben](images/add-extension-annotated.png)

Klicke auf die Erweiterung **Malstift**, um sie hinzuzufügen.

![Malstift Erweiterung hervorgehoben](images/click-pen-annotated.png)

Der Malstiftbereich wird dann unten im Blockmenü angezeigt.

![Malstift-Erweiterungs-Blöcke](images/pen-extension-blocks.png)

Wähle, aus dem **Malstift** Bereich, den Block `schalte Stift ein`{:class="block3extensions"} und füge ihn, wie folgt, zum Anfang deines Programms hinzu:

```blocks3
    Wenn die grüne Flagge angeklickt
+ schalte Stift ein
gehe zu x: (0) y: (0)
```

--- /task ---

--- task ---

Klicke jetzt einige Male auf die grüne Flagge und beobachte, was passiert.

--- /task ---

Wenn Du die Linien hinter der Figur der Katze sehen kannst, funktioniert der Stift und du kannst damit beginnen, wirklich coole Muster zu zeichnen.

Zuerst solltest du die Figur loswerden. Sie steht der Zeichnung im Weg!

--- task ---

Füge einen `verstecke dich`{:class="block3looks"} -Block aus **Aussehen** zum Start des Programms hinzu und sie wird verschwinden.

```blocks3
    Wenn die grüne Flagge angeklickt
+ verstecke dich
schalte Stift ein
```

--- /task ---

Jetzt kannst Du die Farbe des Stiftes, mit einem anderen Block aus dem **Malstift**-Bereich ändern, der Block unterscheidet sich jedoch ein wenig von den anderen, die du gesehen hast. Es ist der `setze Stiftfarbe auf`{:class="block3extensions"}-Block und sieht so aus:

```blocks3
    setze Stiftfarbe auf [#4a6cd4]
```

--- task ---

Ziehe einen `setze Stiftfarbe auf`{:class="block3extensions"}-Block in dein Figuren-Panel und lasse ihn über dem `schalte Stift ein`{:class="block3extensions"}-Block einrasten.

```blocks3
    Wenn die grüne Flagge angeklickt
verstecke dich
+ setze Stiftfarbe auf [#4a6cd4]
schalte Stift ein
```

Klicke nun auf die Farbbox (im Code oben ist es die blaue) und wähle eine Farbe aus.

--- /task ---

Wenn Du auf die grüne Flagge geklickt hast, um deinen Code zu testen, wirst du festgestellt haben, dass die vom Stift angefertigten Zeichnungen nicht verschwinden.

--- task ---

Füge einen `lösche alles`{:class="block3extensions"}-Block aus dem **Malstift**-Bereich, zum Anfang deines Codes hinzu, um sich darum zu kümmern:

```blocks3
    Wenn die grüne Flagge angeklickt
+ lösche alles
verstecke dich
```

--- /task ---