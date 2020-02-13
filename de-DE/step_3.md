## Muster zeichnen

Jetzt hast du ein Programm, das eine Linie zeichnet, aber es zeichnet nur eine Linie. Das ist ein bisschen langweilig! Du könntest `fortlaufende`{:class="block3control"} Schleifen verwenden, um etwas immer wieder und wieder zu zeichnen, aber dann erhälst du Zeichnungen, die über die Bühne hinaus gehen!

Du musst also eine andere Schleife verwenden die `wiederhole, bis`{:class="block3control"} heißt, die du auch im Bereich **Steuerung** findest. Diese Art von Schleife führt etwas immer wieder aus, **bis** eine Wahr/Falsch-Bedingung erfüllt ist.

\--- task \---

Nimm einen `wiederhole bis`{:class="block3control"} - Block aus dem **Steuerungs** - Bereich und packe die `gehen`{:class="block3motion"} und `drehen`{:class="block3motion"} -Blöcke dort hinein, wie folgt:

```blocks3
+ wiederhole bis <>  
  gehe (50) er Schritt
  drehe dich nach rechts um (15) Grad
end
```

\--- /task \---

\--- task \---

Klicke jetzt einige Male auf die grüne Flagge, um dein Programm zu starten, und beobachte, was passiert. Du wirst zwei Dinge bemerken: Der Stift beginnt immer damit eine Linie zur Bühnenmitte zu zeichnen und er hört am Rand nicht auf.

\--- /task \---

## \--- collapse \---

## title: Warum macht der Stift das?

Der Stift beginnt immer in Richtung der Mitte zu zeichnen, da der erste **Bewegungs**-Block, der nach dem `schalte Stift ein`{:class="block3extensions"}-Block ausgeführt wird, `gehe zu x: 0 y: 0`{:class="block3motion"} ist. Der Stift zeichnet also eine Linie, während er sich in die Mitte der Bühne bewegt.

Der Stift endet nicht am Rand der Bühne, weil du der `wiederhole, bis`{:class=„block3control“}-Schleife noch nicht gesagt hast, welche Bedingung sie überprüft. Das bedeutet, dass die Bedingung niemals erfüllt werden kann, sodass die Schleife immer weiter läuft. Das bedeutet, dass die Schleife im Moment wie eine `fortlaufend`{:class="block3control"}-Schleife arbeitet.

\--- /collapse \---

\--- task \---

Verschiebe den `gehe zu x: 0 y: 0`{:class="block3motion"} -Block vor den `schalte Stift ein`{:class="block3extensions"} -Block und füge einen `schalte Stift aus`{:class="block3extensions"} -Block, aus dem **Malstift**-Bereich, direkt an den Anfang deines Skripts hinzu.

\--- /task \---

Zeit, um deine `wiederhole bis`{:class="block3control"}-Schleife zu reparieren, damit sie stoppt, wenn du es wünscht. Du möchtest herausfinden, ob die (unsichtbare) Figur den Rand der Bühne berührt, also benötigst du einen **fühlen** Block — in diesem Fall den `wird ( ) berührt?`{:class="block3sensing"}-Block.

\--- task \---

Füge einen `wird ( ) berührt?`{:class="block3sensing"}-Block in deine `wiederhole bis`{:class="block3control"}-Schleife ein und wähle `Rand`{:class="block3sensing"} aus. Dann läuft die Schleife **bis** die (unsichtbare) Figur den Bühnenrand berührt.

```blocks3
    schalte Stift ein
+    wiederhole bis <wird [Rand v] berührt?> 
  gehe (50) er Schritt
  drehe dich nach rechts um (15) Grad
end
```

\--- /task \---

\--- task \---

Ändere die Anzahl der Schritte im Block `gehe`{:class="block3motion"}-Block auf `5` und überprüfe, ob dein Programm mit diesem übereinstimmt, bevor du es testest:

```blocks3
    Wenn die grüne Flagge angeklickt
schalte Stift aus
verstecke dich
lösche alles
gehe zu x: (0) y: (0)
setze Stiftfarbe auf [#4a6cd4]
schalte Stift ein
wiederhole bis <wird [Rand v] berührt?> 
  gehe (5) er Schritt
  drehe dich nach rechts um (15) Grad
end
```

\--- /task \---

Wenn du den Code jetzt ausführst, wirst du feststellen, dass die Zeichnung des Stiftes auf der Bühne bleibt.

Nicht nur das, dein Programm hat sich zu einem Programm zum Zeichnen von Kreisen entwickelt! Was hier passiert, ist, dass sich diese 15-Grad-Drehungen letztendlich auf 360 Grad summieren, sodass sich der Stift in einem vollen Kreis bewegt. Du wirst die Art und Weise, in der er sich bewegt, leicht ändern, damit er jedes Mal einen etwas größeren Schritt macht, sodass er sich in einer Spirale nach außen dreht. Dafür benötigst du eine **Variable**.

Variablen sind im Grunde benannte Orte zum Speichern von Zahlen oder anderen Informationen, die dich interessieren. Du kannst sie im Bereich der **Variablen**-Blöcke erstellen.

\--- task \---

Erstelle eine Variable mit dem Namen `Schritte`{:class="block3variables"} und füge am Anfang deines Programms einen `setze Schritte auf 0`{:class="block3variables"}-Block hinzu.

```blocks3
    Wenn die grüne Flagge angeklickt
+   setze [Schritte v] auf [0]
    schalte Stift aus
```

\--- /task \---

\--- task \---

Verwende dann den Wert von `Schritte`{:class="block3variables"} anstelle von `5` im `gehe`{:class="block3motion"}-Block und füge `ändere Schritte um 1`{:class="block3variables"} als Teil deiner Schleife hinzu:

```blocks3
    schalte Stift ein
    wiederhole bis <wird [Rand v] berührt?> 
+       gehe (Schritte) er Schritt
         drehe dich nach rechts um (76) Grad
+       ändere [Schritte v] um (1)
end
```

\--- /task \---

Glaubst du, es ist wichtig, an welcher Stelle in der Schleife du den `ändere Schritte um 1`{:class="block3variables"}-Block setzt?

## \--- collapse \---

## title: Den Code in die richtige Reihenfolge bringen

Wenn du entscheidest, in welcher Reihenfolge die Blöcke eingefügt werden sollen, musst du darüber nachdenken, was jeder Block tut und was dein Code tun soll.

In diesem Fall willst du, dass der Stift sich bewegt und sich dann dreht, immer wieder und wieder. Jedes Mal, wenn er das tut, möchtest du einen zusätzlichen Schritt gehen.

Es ist also sinnvoll, den `ändere Schritte um 1`{:class="block3variables"}-Block **hinter** den `gehe`{:class="block3motion"}-Block zu setzen. Nach dem Gehen spielt es jedoch keine Rolle, ob der Stift zuerst gedreht wird und sich dann die Anzahl der Schritte ändert oder ob sich stattdessen zuerst die Anzahl der Schritte ändert und sich dann der Stift dreht.

\--- /collapse \---

\--- task \---

Führe das Programm nun aus und versuche auch die Gradzahl zu ändern (versuche es mit `76` und `120`)!

\--- /task \---