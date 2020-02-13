## Linee più accattivanti

È ora di aggiungere colore! In questo momento, la linea è un colore, ma **Penna** ha dei blocchi che possono cambiare il suo colore. E con il giusto blocco **Operatori**, puoi persino cambiare il colore in modo casuale!

Il blocco per cambiare il colore **Penna** è `cambia colore penna di`{: class = "block3extensions"}:

```blocks3
    cambia colore penna di (10)
```

\--- task \---

Prendi uno di quei blocchi e mettilo nella tua `ripeti fino a quando`{: class = "block3control"}, come questo:

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

È bello, ma un po' prevedibile. Puoi renderlo un po' più divertente se aggiungi un numero casuale, quindi il colore cambia casualmente.

\--- task \---

Metti il blocco generatore di numeri casuali **Operatore** nel colore della penna a `cambia colore penna di`{: class = "block3extensions"} e seleziona alcuni valori da inserire in esso. Proverei `1` e `100` per iniziare.

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (pick random (1) to (100))
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

\--- task \---

Prova a eseguirlo di nuovo, e guarda l'arcobaleno casuale!

\--- /task \---