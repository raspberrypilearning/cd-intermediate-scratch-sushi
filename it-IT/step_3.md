## Disegnare forme

Ora hai un programma che disegna una linea, ma disegna solo una riga. È un po' noioso! Puoi usare il ciclo `forever`{: class = "block3control"} per disegnare qualcosa più e più volte, ma poi otterrai disegni che escono dallo stage!

Quindi è necessario utilizzare un diverso tipo di ciclo chiamato ripeti fino a quando `repeat until`{: class = "block3control"}, che troverai anche nella sezione **Controllo**. Questo tipo di ciclo farà qualcosa più e più volte, fino a quando **until** una condizione Vero / Falso è soddisfatta.

\--- task \--- Prendi `repeat until`{: class = "block3control"} dalla sezione **Controllo**, e metti i blocchi `move`{: class = "block3motion"} e `turn`{: class = "block3motion"} al suo interno, in questo modo:

```blocks3
+    repeat until <> 
        move (50) steps
        turn cw (15) degrees
    end
```

\--- /task \---

\--- task \--- Fai clic sulla bandiera verde per eseguire il programma alcune volte e vedi cosa succede. Noterai due cose: la penna inizia sempre disegnando una linea verso il centro dello stage e non si ferma sul bordo. \--- /task \---

## \--- collapse \---

## titolo: Perché la penna fa questo?

La penna inizia sempre a disegnare nella direzione del centro, perché il primo blocco **Movimento** che viene eseguito dopo il blocco `pen down`{: class = "block3extensions"} è `go to x: 0 y: 0`{: class = "block3motion"}. Quindi la penna disegnerà una linea mentre si sposta al centro dello schermo.

La penna non si ferma sul bordo dello schermo, perché non hai ancora detto alla ripetizione `repeat until`{: class = "block3control"} quale condizione sta controllando. Ciò significa che la condizione non può mai essere soddisfatta, quindi il ciclo verrà eseguito senza interruzioni. Ciò significa che in questo momento, il ciclo sta lavorando come un ciclo `forever`{: class = "block3control"}.

\--- /collapse \---

\--- task \--- Sposta il blocco `go to x: 0 y: 0`{: class = "block3motion"} prima del blocco `pen down`{: class = "block3extensions"} e aggiungi, dalla sezione **Penna**, un blocco `pen up`{: class = "block3extensions"} all'inizio del tuo codice. \--- /task \---

È ora di correggere la ripetizione `repeat until`{: class = "block3control"} in modo che si fermi quando lo si desidera. Stai cercando di capire se lo sprite (invisibile) sta toccando il bordo dello stage, quindi hai bisogno di un blocco **Sensori** - in questo caso, il blocco `touching ?`{: class = "block3sensing"}.

\--- task \--- aggiungi un `touching ?` {: class = "block3sensing"} nella tua ripetizione `repeat until` {: class = "block3control"}, e seleziona `edge` {: class = "block3sensing"}. Quindi il ciclo verrà eseguito **until** lo sprite (invisibile) tocca il bordo dello schermo.

```blocks3
    pen down
+    repeat until <touching [edge v] ?> 
        move (50) steps
        turn cw (15) degrees
    end
```

\--- /task \---

\--- task \--- Modifica il numero di passaggi nel blocco `move`{: class = "block3motion"} su `5`e verifica che il tuo programma corrisponda a questo prima di testarlo:

```blocks3
    when green flag clicked
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (5) steps
        turn cw (15) degrees
    end
```

\--- /task \---

Se esegui il codice ora, vedrai che il disegno della penna rimane sullo schermo.

Non solo, ma il tuo programma è diventato un programma di disegno cerchi! Quello che sta succedendo qui è che le curve di 15 gradi alla fine diventano 360 gradi, e così la tua penna gira in un cerchio completo. Cambierà il modo in cui si muove per fare un passo leggermente più lungo ogni volta, quindi alla fine si spegne in una spirale. Per questo, avrai bisogno di una **variabile**.

Le variabili sono fondamentalmente luoghi etichettati per memorizzare numeri o altre informazioni che ti interessano. Puoi crearli nella sezione **Variabili**.

\--- task \--- Crea una variabile chiamata `steps`{: class = "block3variables"}, quindi aggiungi `set steps to 0`{: class = "block3variables"} all'inizio del tuo programma.

```blocks3
    when green flag clicked
+   set [steps v] to [0]
    pen up
```

\--- /task \---

\--- task \--- Quindi usa il valore di `steps`{: class = "block3variables"} invece del `5` nel blocco `move`{: class = "block3motion"} e aggiungi `change steps by 1`{: class = "block3variables"} come parte del tuo loop:

```blocks3
    pen down
    repeat until <touching [edge v] ?> 
+       move (steps) steps
        turn cw (76) degrees
+        change [steps v] by (1)
    end
```

\--- /task \---

Pensi che sia importante dove mettere ciclo i passaggi di modifica `change steps by 1`{: class = "block3variables"}?

## \--- collapse \---

## titolo: inserire il codice nell'ordine corretto

Quando decidi in quale ordine inserire i blocchi, pensa a cosa fa ogni blocco e cosa vuoi che faccia il tuo codice.

In questo caso, vuoi spostare la penna, quindi girare, ancora e ancora. Ogni volta che lo fa, vuoi spostarti di un passettino.

Quindi ha senso inserire i passaggi di modifica `change steps by 1`{: class = "block3variables"} **dopo** il blocco `move`{: class = "block3motion"}. Tuttavia, dopo lo spostamento, non importa se la penna gira per prima e poi il numero di passi cambia, o se il numero di passi cambia prima e poi la penna gira.

\--- /collapse \---

\--- task \--- Ora esegui il programma, e prova anche a cambiare il numero di gradi (prova `76` e `120`)! \--- /task \---