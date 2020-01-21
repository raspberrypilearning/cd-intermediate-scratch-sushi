## Linii mai interesante

Este timpul să adaugi culoare! Chiar acum, linia ta are o culoare, dar **Stilou** are blocuri care pot schimba culoarea. Iar cu blocul **Operator** potrivit, poți chiar schimba culoarea aleatoriu!

Blocul de schimbare a culorii **Stilou** este `schimbă culoarea stiloului cu`{:class="block3extensions"}:

```blocks3
    schimbă culoarea stiloului cu (10)
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    repetă până când <atinge [marginea v] ?>
+        schimbă culoarea stiloului cu (10)
        mergi (pași) pași
        rotește-te cw (grade ::variables) grade
        modifică [pași v] cu (creștere ::variables)
    end
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    repetă până când <atinge [marginea v] ?>
+        schimbă culoarea stiloului cu (alege aleator între (1) și (100))
        mergi (pași) pași
        rotește-te cw (grade ::variables) grade
        modifică [pași v] cu (creștere ::variables)
    end
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---