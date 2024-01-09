## Lignes plus cool

Il est temps d'ajouter de la couleur! Pour l'instant, ta ligne a une couleur, mais le **Stylo** contient des blocs qui peuvent changer de couleur. Et avec le bloc droit **Opérateur**, tu peux même changer la couleur au hasard!

Le bloc pour changer la couleur **Stylo** est`changer la couleur du stylo par`{:class="block3extensions"}:

```blocks3
    changer la couleur du stylo par (10)
```

\--- task \---

Prends un de ces blocs et mets-le dans ta boucle `répéter jusqu'à`{:class="block3control"}, comme ceci :

```blocks3
    répéter jusqu'à <touching [edge v] ?> 
+ changer la couleur du stylo par (10)
        déplacer (étapes) pas
        tourner cw (degrés :: variables) degrés
        changer [étapes v] par (augmenter :: variables)
    fin
```

\--- /task \---

C'est cool, mais un peu prévisible. Tu peux le rendre un peu plus amusant si tu ajoutes un nombre aléatoire, de sorte que la couleur change de manière aléatoire.

\--- task \---

Mets le bloc numéro aléatoire **Opérateur** dans le bloc `changer la couleur du stylo par`{:class="block3extensions"} et sélectionne quelques valeurs à utiliser. Je voudrais essayer `1` et `100` pour commencer.

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

Essaie de l'exécuter à nouveau et observe l'arc-en-ciel aléatoire !

\--- /task \---