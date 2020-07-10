## Richiesta di immissione

Ok, questo sta diventando piuttosto interessante, ma è un po' noioso dover modificare il codice ogni volta che si desidera disegnare una forma diversa. Non sarebbe bello che il programma ti chieda i valori da usare? Ce la puoi fare!

--- task ---

Prima cosa, vai alla sezione **Variabili** e crea le variabili chiamate `Gradi`{:class="block3variables"} e `incrementa`{:class="block3variables"}.

--- /task ---

--- task ---

Ora aggiungi le nuove variabili al tuo codice in questo modo:

```blocks3
    repeat until <touching [edge v] ?> 
        move (passi) steps
        turn cw (Gradi ::variables) degrees
        change [passi v] by (incrementa ::variables)
    end
```

--- /task ---

Ora devi chiedere i valori per queste due variabili e memorizzarle. Lo fai usando un blocco **Sensori** chiamato `Chiedi e aspetta`{:class="block3sensing"}, in cui puoi inserire una domanda.

--- task ---

Trascina il blocco `Chiedi e aspetta`{:class="block3sensing"} nel tuo pannello sprite e cambia la domanda in `Quanti passi devo fare?`{:class="block3sensing"}

Quindi aggiungilo al tuo programma, subito dopo aver impostato `passi`{:class="block3variables"} a `0`, come questo:

```blocks3
    when green flag clicked
    set [passi v] to [0]
+    ask [Quanti passi devo fare?] and wait
    pen up
```

--- /task ---

Ora hai il tuo programma che fa una domanda, ne hai bisogno per ricordare la risposta! Salta fuori che Scratch ha una variabile speciale chiamata `risposta`{:class="block3sensing"}, dove memorizza la risposta più recente che ha ricevuto. È possibile trovare questa variabile tra i blocchi **Sensori**.

--- task ---

Usando un blocco `porta...a`{:class="block3variables"} da **Variabili**, prendi il valore di `risposta`{:class="block3sensing"} e memorizzalo in `incrementa`{:class="block3variables"} in questo modo:

```blocks3
    ask [Quanti passi devo fare?] and wait
+    set [incrementa v] to (answer)
```

--- /task ---

--- task ---

Ora, fai la stessa cosa con `Gradi`{:class="block3variables"}, chiedendo `Quanti gradi dovrei girare?`{:class="block3sensing"} e memorizzando il valore di `risposta`{:class="block3sensing"} in `Gradi`{:class="block3variables"}:

```blocks3
    set [incrementa v] to (answer)
+    ask [Quanti gradi devo girare?] and wait
+    set [Gradi v] to (answer)
```

--- /task ---

--- task ---

Controlla che il tuo programma ora assomigli a quello sotto, ed eseguilo alcune volte con numeri diversi. Annota le risposte che creano i disegni più belli. Ne avrai bisogno in un secondo momento!

```blocks3
    when green flag clicked
    set [passi v] to [0]
    ask [Quanti passi devo fare?] and wait
    set [incrementa v] to (answer)
    ask [Quanti gradi devo girare?] and wait
    set [Gradi v] to (answer)
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
```

--- /task ---