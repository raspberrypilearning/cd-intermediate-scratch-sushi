## Rimescolare il tutto

Puoi effettivamente usare numeri casuali per far girare l'intero programma più e più volte, cambiando il modello ogni volta! Assomiglierà agli screen saver degli anni '90 ... che probabilmente non ricorderai, ma chiedi a uno dei tuoi genitori!

Hai bisogno di alcune modifiche per fare ciò. Il primo è che è necessario impostare le variabili `incrementa`{:class="block3variables"} e `gradi`{:class="block3variables"} a caso piuttosto che chiederle all'utente. Quindi è necessario modificare alcuni dei blocchi di codice.

--- task ---

Rimuovi le domande dal tuo codice e aggiornalo per usare numeri casuali.

```blocks3
    when green flag clicked
    set [passi v] to [0]
-    ask [Quanti passi devo fare?] and wait
+    set [incrementa v] to (pick random (1) to (10))
-    ask [Quanti gradi devo girare?] and wait
+    set [Gradi v] to (pick random (1) to (180))
    pen up
```

--- /task ---

Se esegui il tuo programma ora, scoprirai che disegna uno schema casuale, ma solo una volta. Quale pensi che sia la ragione?

È perché il ciclo viene eseguito solo finché raggiunge il bordo dello stage.

--- task ---

Per mantenerlo vivo, hai bisogno di un altro ciclo che funzioni per sempre (quindi un blocco `per sempre`{:class="block3control"}) al di fuori di quello corrente. Basta trascinarne uno fuori dalla sezione **Controllo** e aggiungigli tutto il tuo codice.

```blocks3
    when green flag clicked
+    forever 
        set [passi v] to [0]
        set [incrementa v] to (pick random (1) to (10))
        set [Gradi v] to (pick random (1) to (180))
        pen up
        hide
        clear
        go to x: (0) y: (0)
        set pen color to [#4a6cd4]
        pen down
        repeat until <touching [edge v] ?> 
            move (passi) steps
            turn cw (Gradi) degrees
            change [passi v] by (incrementa)
        end
    end
```

--- /task ---

Ora hai davvero qualcosa di fantastico da guardare!

Tuttavia, potresti notare che, di tanto in tanto, il computer disegna qualcosa che sembra abbastanza... brutto. Questo perché alcuni numeri per queste variabili sono inadatti, e alcune **combinazioni di quei numeri** sono altrettanto inadatti.

Sulla prossima scheda, aiuterai il computer a scegliere solo buone combinazioni!