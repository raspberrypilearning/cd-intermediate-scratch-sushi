## Ustaw wszystko losowo

Możesz użyć liczb losowych, aby cały program był uruchamiany w kółko, zmieniając wzór za każdym razem! Będzie to wyglądało trochę jak wygaszacze ekranu w latach 90.... których prawdopodobnie nie pamiętasz, ale zapytaj jednego z rodziców!

Potrzebujesz kilku zmian, aby tak się stało. Pierwszą z nich jest to, że musisz ustawić zmienne `powiększenie`{:class="block3variables"} i `stopnie`{:class="block3variables"} na losowe wartości, zamiast pytać o nie użytkownika. Więc musisz zmienić niektóre bloki kodu.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [kroki v] na [0]
- zapytaj [o ile kroków powinienem powiększyć się?] i czekaj
+ ustaw [powiększenie v] na (losuj liczbę od (1) do (10))
- zapytaj [o ile stopni powinienem się obrócić?] i czekaj
+ ustaw [stopnie v] na (losuj liczbę od (1) do (180))
    podnieś pisak
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    kiedy kliknięto zieloną flagę
+ zawsze 
        ustaw [kroki v] na [0]
        ustaw [powiększenie v] na (losuj liczbę od (1) do (10))
        ustaw [stopnie v] na (losuj liczbę od (1) do (180))
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
    koniec
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!