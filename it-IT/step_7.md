## Aiutare il computer

Ti ricordi alcuni passi indietro, in cui ti ho detto di scrivere alcuni dei tuoi valori preferiti per `incrementa`{: class = "block3variables"} e `Gradi`{: class = "block3variables"}, quelli che hanno dato i modelli più belli? Se non l'hai fatto, non ti preoccupare: puoi solo guardare il programma random per un po' di tempo e annotare le combinazioni che danno ottimi risultati.

Insegnerai a Scratch quelle combinazioni di valori, in modo che possa usarli per creare solo immagini fantastiche!

Per fare ciò, avrai bisogno di una **lista**. Troverai le liste con le variabili nella sezione **Variabili**. Proprio come hai fatto con le tue variabili, devi prima creare la tua lista!

\--- task \---

Click **Make a List**, and enter `Degrees List`{:class="block3variables"} as the name.

![](images/makeAList.png)

\--- /task \---

Your list, which is empty at the moment, will appear on the Stage, and you'll see a bunch of blocks for it in **Variables**.

![](images/listBlocks.png)

\--- task \---

Make another list called `Increase List`{:class="block3variables"}

\--- /task \---

\--- task \---

Now, by clicking on the little plus sign (**+**) at the bottom of the lists, add in the first pair of values of `increase`{:class="block3variables"} and `degrees`{:class="block3variables"} you liked, each value into the right list. Do this again to add the second pair of values. This will be enough for now — you'll add the rest of the value pairs you like later!

![](images/helping2.png)

Make sure that the `degrees`{:class="block3variables"} value and the `increase`{:class="block3variables"} value that worked well together are at the same position in the `Degrees List`{:class="block3variables"} and the `Increase List`{:class="block3variables"}. They need to be there so your program can match them up again using their position!

\--- /task \---

Now you have the lists, you just need to get your code to read them and loop over them! To do this, you’re going to use a new variable to act as a counter, some **incrementing**, and an `if then`{:class="block3control"} **Control** block.

## \--- collapse \---

## titolo: Cosa significa incremento?

To increment something means to add something to it.

You will use a variable to act as a counter to keep track of what position you're at in your lists. To move through the lists, you'll keep incrementing the counter by `1` (so, adding `1` to it) until you get to the end of the list.

\--- /collapse \---

\--- task \---

Create a new variable called `counter`{:class="block3variables"}, and update your code to look like this:

```blocks3
    when green flag clicked
    set [counter v] to [0]
    forever 
+        if <(counter) = (length of [Increase List v] :: list)> then 
+            set [counter v] to [0]
        end
+        change [counter v] by (1)
        set [steps v] to [0]
+        set [incrementa v] to (item (counter) of [Lista Incrementi v] :: list)
+        set [Gradi v] to (item (counter) of [Lista Gradi v] :: list)
        pen up
        hide
        clear
        go to x: (0) y: (0)
        set pen color to [#4a6cd4]
        pen down
        repeat until <touching [edge v] ?> 
            move (steps) steps
            turn cw (Gradi ) degrees
            change [steps v] by (incrementa)
        end
    end
```

\--- /task \---

Notice the new blocks that:

1. Imposta `counter`{: class = "block3variables"} a `0`, fuori da tutti i loop.
2. Verifica se il numero memorizzato in `counter`{: class = "block3variables"} è pari alla lunghezza dell'elenco e, in tal caso, imposta `counter`{: class = "block3variables"} a `0`. Ciò significa che questa variabile sarà sempre al massimo pari al numero di posizioni negli elenchi e non più grande.
3. Aggiungi `1` a `counter`{: class = "block3variables"}.
4. Scegli l'oggetto da `Lista Incrementi`{: class = "block3variables"} che è nella posizione descritta da `counter`{: class = "block3variables"}, e inseriscilo nella variabile `incrementa`{: class = "block3variables"}. Fai lo stesso per `Lista Gradi`{: class = "block3variables"} e la variabile `Gradi`{: class = "block3variables"}.

## \--- collapse \---

## titolo: Come funziona il codice?

This is what happens when you run your program:

1. Imposta `counter`{: class = "block3variables"} a `0`.
2. Avvia il ciclo `forever`{: class = "block3control"}.
3. Controlla se `counter`{: class = "block3variables"} (`0`) è uguale alla lunghezza di `Lista Incrementi`{: class = "block3variables"} (`2`). Non lo è.
4. Cambia `counter`{: class = "block3variables"} di `1`. Ora `counter`{: class = "block3variables"} = `1`.
5. Imposta `steps`{: class = "block3variables"} a `0`.
6. Ottieni l'oggetto nella posizione indicata dal `counter`{: class = "block3variables"} (`1`) nel `Lista Incrementi`{: class = "block3variables"}, e mettilo in `incrementa`{: class = "block3variables"}.
7. Ottieni l'oggetto nella posizione indicata da `counter`{: class = "block3variables"} (`1`) nella `Lista Gradi`{: class = "block3variables"}, e inseriscilo in `Gradi`{: class = "block3variables"}.
8. Fai tutte le cose relative al disegno delle forme.
9. Riavvia il ciclo `forever`{: class = "block3control"}:
10. Controlla se `counter`{: class = "block3variables"} (`1`) è uguale alla lunghezza di `Lista Incrementi`{: class = "block3variables"} (`2`). Non lo è.
11. Cambia `counter`{: class = "block3variables"} di `1`. Ora `counter`{: class = "block3variables"} = `2`.
12. Imposta `steps`{: class = "block3variables"} a `0`.
13. Ottieni l'oggetto nella posizione denominata da `counter`{: class = "block3variables"} (`2`) nella `Lista Incrementi`{: class = "block3variables"}, e mettilo in `incrementa`{: class = "block3variables"}.
14. Ottieni l'oggetto nella posizione indicata da `counter`{: class = "block3variables"} (`2`) nella `Lista Gradi`{: class = "block3variables"}, e inseriscilo in `Gradi`{: class = "block3variables"}.
15. Fai tutte le cose relative al disegno delle forme.
16. Riavvia il ciclo `forever`{: class = "block3control"}:
17. Controlla se `counter`{: class = "block3variables"} (`2`) è uguale alla lunghezza del `Lista Incrementi`{: class = "block3variables"} (`2`). Lo è!
18. Imposta `counter`{: class = "block3variables"} a `0`.
19. Continua dal **passo 4** di questa lista, in un ciclo senza fine!

\--- /collapse \---

\--- task \---

Once you're happy with the code, go ahead and add the rest of the pairs of values you noted down to the `Degrees List`{:class="block3variables"} and the `Increase List`{:class="block3variables"}.

\--- /task \---

That's it! Sit back and watch your program keep drawing lovely patterns in a never-ending loop! If you want to add more patterns, you can: just add more pairs of numbers to the two lists and restart the program.