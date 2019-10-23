## Motifs de dessin

Tu as maintenant un programme qui trace une ligne, mais il n'en trace qu'une. C'est un peu terne! Tu peux utiliser la boucle `répéter indéfiniment`{:class="block3control"} pour dessiner quelque chose, encore et encore, mais alors tu obtiendras des dessins qui sortent de la scène!

Tu devras donc utiliser un type de boucle différent, appelé `répéter jusqu'à`{:class="block3control"}, que tu trouveras également dans la section **Contrôle**. Ce type de boucle répétera quelque chose encore et encore, **jusqu'à** ce qu'une condition Vrai / Faux est remplie.

--- task --- Prends un bloc `répéter jusqu'à`{:class="block3control"} de la section **Contrôle**, et mets les blocs `déplacer`{:class="block3motion"} et `tourner`{:class="block3motion"} à l'intérieur, comme suit:

```blocks3
+ répéter jusqu'à <> 
        déplacer de (50) pas
        tourner cw (15) degrés
    fin
```

--- /task ---

--- task --- Maintenant, clique sur le drapeau vert pour exécuter le programme plusieurs fois et vois ce qui se passe. Tu remarqueras deux choses: le stylo commence toujours par tracer une ligne vers le milieu de la scène et il ne s’arrête pas au bord. --- /task ---

--- collapse ---
---
title: Pourquoi le stylo fait-il cela?
---

Le stylo commence toujours à dessiner dans la direction du milieu, car le premier bloc **Mouvement** qui s'exécute après le `stylo en position d'écriture`{:class="block3extensions"} est `aller à x: 0 y: 0`{:class="block3motion"}. Ainsi, le stylo tracera une ligne lorsqu'il se déplacera au centre de la scène.

Le stylo ne s'arrête pas au bord de la scène, parce que tu n'as pas encore dit au bloc `répéter jusqu'à`: boucle {:class=block3control"} quelle condition il vérifie. Cela signifie que la condition ne peut jamais être remplie, ainsi la boucle fonctionnera encore et encore. Cela signifie qu’à présent, la boucle fonctionne comme une boucle `répéter indéfiniment`{:class="block3control"}.

--- /collapse ---

--- task --- Déplace le bloc `aller à x: 0 y: 0`{:class="block3motion"} avant le `stylo en position d'écriture`{:class="block3extensions"} et ajoute, à partir de la section **Stylo** , un bloc `relever le stylo`{:class="block3extensions"} au début de ton code. --- /task ---

Il est temps de corriger ta boucle `répéter jusqu'à`{:class ="block3control"} pour qu'elle s'arrête quand tu le désires. Tu cherches à savoir si le sprite (invisible) touche le bord de la scène, tu as donc besoin d'un bloc **Capteur** - dans ce cas, le bloc `touche ?`{:class="block3sensing"}.

--- task --- Ajoute un bloc `touche ?`{:class="block3sensing"} dans ta boucle `répétition jusqu'à`{:class="block3control"} et sélectionne `bord`{:class="block3sensing"}. Ensuite, la boucle va exécuter **jusqu'à** ce que le sprite (invisible) touche le bord de la scène.

```blocks3
    stylo en position d'écriture
+ répétez jusqu'à <touching [edge v] ?> 
        déplacer de (50) pas
        tournez cw (15) degrés
    fin
```

--- /task ---

--- task --- Modifie le nombre de pas dans le bloc `déplacer`{:class="block3motion"} en `5` et vérifie que ton programme correspond à celui-ci avant de le tester:

```blocks3
    lorsque le drapeau vert est cliqué
    relever le stylo
    masquer
    effacer
    aller à x: (0) y: (0)
    définir la couleur du stylo sur [# 4a6cd4]
    stylo en position d'écriture
    répéter jusqu'à <touching [edge v] ?> 
        déplacer de (5) pas
        tourner cw ( 15) degrés
    fin
```

--- /task ---

Si tu exécutes le code maintenant, tu verras que le dessin du stylo reste sur la scène.

Non seulement cela, mais ton programme est devenu un programme de dessin de cercle! Ce qui se passe ici, c'est que ces tournants de 15 degrés totalisent finalement 360 degrés, de sorte que ton stylo tourne en rond. Tu vas changer la façon dont il bouge légèrement pour le rendre légèrement plus long à chaque fois de sorte qu'il fasse des spirales. Pour cela, tu auras besoin d'une **variable**.

Les variables sont essentiellement des emplacements étiquetés pour stocker des numéros ou d’autres informations qui t'intéressent. Tu peux les créer dans la section des blocs **Variables**.

--- task --- Crée une variable appelée `étapes`{:class="block3variables"}, puis ajoute un bloc de `définir étapes à 0`{:class="block3variables"} au début de ton programme.

```blocks3
    lorsque le drapeau vert est cliqué
+ définir [étapes v] sur [0]
    relever le stylo
```

--- /task ---

--- task --- Ensuite, utilise la valeur de `étapes`{:class="block3variables"} au lieu de `5` dans le bloc `déplacer`{:class="block3motion"} et ajoute `changer étapes par 1`{:class="block3variables"} en tant que partie de ta boucle:

```blocks3
    stylo en position d'écriture
    répéter jusqu'à <touching [edge v] ?> 
+ déplacer (étapes) pas
        tourner cw (76) degrés
+ changer [étapes v] par (1)
    fin
```

--- /task ---

Penses-tu qu’il importe de savoir où, dans la boucle, tu mets le bloc `changer étapes par 1`{:class="block3variables"}?

--- collapse ---
---
title: Mettre le code dans le bon ordre
---

Lorsque tu décides dans quel ordre placer des blocs, réfléchis à ce que chaque bloc fait et à ce que tu veux que ton code fasse.

Dans ce cas, tu veux que le stylo bouge, puis tourne, encore et encore. Chaque fois que cela se produit, tu souhaites déplacer d'une étape supplémentaire.

Il est donc logique de placer le bloc `changer étapes par 1`{:class="block3variables"} **après** le `déplacer`{:class="block3motion"}. Cependant, après le déplacement, peu importe si le stylo tourne en premier et ensuite le nombre d'étapes change, ou si le nombre d'étapes change en premier et ensuite le stylo tourne à la place.

--- /collapse ---

--- task --- Exécute maintenant le programme et essaie également de modifier le nombre de degrés autour (essayer `76` et `120`)! --- /task ---