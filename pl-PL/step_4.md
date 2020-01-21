## Pytanie o dane wejściowe

Ok, robi się całkiem fajnie, ale nudne jest edytowanie kodu za każdym razem, gdy chcesz narysować inny wzór. Czy nie byłoby dobrze, gdyby program poprosił cię o podanie wartości? Możesz to zrobić!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    powtarzaj aż <touching [edge v] ?> 
        przesuń o (kroki) kroków
        obróć w prawo o (stopnie ::zmienne) stopni
        zmień [kroki v] o (powiększenie ::zmienne)
    koniec
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [kroki v] na [0]
+ zapytaj [o ile kroków powinienem się powiększyć?] i czekaj
    podnieś pisak
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    zapytaj [o ile kroków powinienem się powiększyć?] i czekaj
+ ustaw [powiększenie v] na (odpowiedź)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    ustaw [powiększenie v] na (odpowiedź)
+ zapytaj [o ile stopni powinienem się obrócić?] i czekaj
+ ustaw [stopnie v] na (odpowiedź)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [kroki v] na [0]
    zapytaj [o ile kroków powinienem się powiększyć?] i czekaj
    ustaw [powiększenie v] na (odpowiedź)
    zapytaj [o ile stopni powinienem się obrócić?] i czekaj
    ustaw [stopnie v] na (odpowiedź)
    podnieś pisak
    ukryj
    wyczyść wszystko
    idź do x: (0) y: (0)
    ustaw kolor pisaka na [#4a6cd4]
    przyłóż pisak
    powtarzaj aż <touching [edge v] ?> 
        przesuń o (kroki) kroki
        obróć w prawo o (stopnie) stopni
        zmień [kroki v] o (powiększenie)
    koniec
```

\--- /task \---