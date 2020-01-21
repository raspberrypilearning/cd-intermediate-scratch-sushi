## Ciekawsze linie

Czas dodać kolor! W tej chwili twoja linia ma jeden kolor, ale sekcja **Pióro** posiada bloki, które mogą zmienić jej kolor. A dzięki odpowiedniemu blokowi **Wyrażenie** możesz nawet losowo zmieniać kolor!

Blok do zmiany koloru **Pióra** to `zmień kolor pisaka o`{:class="block3extensions"}:

```blocks3
    zmień kolor pisaka o (10)
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    powtarzaj aż <touching [edge v] ?> 
+ zmień kolor pisaka o (10)
        przesuń o (kroki) kroki
        obróć cw o (stopnie ::zmienne) stopni
        zmień [kroki v] o (powiększenie ::zmienne)
    koniec
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    powtarzaj aż <touching [edge v] ?> 
+ zmień kolor pisaka o (wybierz losowy (1) do (100))
        przesuń o (kroki) kroki
        obróć cw o (stopnie ::zmienne) stopni
        zmień [kroki v] o (powiększenie ::zmienne)
    koniec
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---