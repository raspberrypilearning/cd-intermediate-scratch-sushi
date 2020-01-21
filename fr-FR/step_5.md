## Lignes plus cool

Il est temps d'ajouter de la couleur! Pour l'instant, ta ligne a une couleur, mais le **Stylo** contient des blocs qui peuvent changer de couleur. Et avec le bloc droit **Opérateur**, tu peux même changer la couleur au hasard!

Le bloc pour changer la couleur **Stylo** est`changer la couleur du stylo par`{:class="block3extensions"}:

```blocks3
    changer la couleur du stylo par (10)
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    répéter jusqu'à <touching [edge v] ?> 
+ changer la couleur du stylo par (10)
        déplacer (étapes) pas
        tourner cw (degrés :: variables) degrés
        changer [étapes v] par (augmenter :: variables)
    fin
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    répéter jusqu'à <touching [edge v] ?> 
+        changer la couleur du stylo (choisir au hazard de (1) à (100))
        déplacer (steps) pas
        tourner cw (degrés ::variables) degrés
        changer [étapes v] par (augmenter ::variables)
    fin
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---