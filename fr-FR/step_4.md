## Demande d'entrée

Ok, ça devient plutôt cool, mais c'est un peu ennuyeux de devoir modifier ton code à chaque fois que tu veux dessiner un motif différent. Ne serait-il pas bon de demander au programme de te demander des valeurs à utiliser? Tu peux le faire!

--- task --- Tout d'abord, va à la section **Variables** et crée des variables nommées `degrés`{:class="block3variables"} et `augmenter`{:class="block3variables"}. --- /task ---

--- task --- Ajoute maintenant les nouvelles variables à ton code comme ceci:

```blocks3
    répéter jusqu'à ce que <touche le [bord v] ?> 
        avancer de (étapes) pas
        tourner droite de (degrees :: variables) degrés
        ajouter (augmenter :: variables) à [étapes v]
```

--- /task ---

Maintenant, tu dois demander des valeurs pour ces deux variables et les stocker. Pour ce faire, utilise un bloc **Capteur** appelé `demander et attendre`{:class="block3sensing"}, dans lequel tu peux taper une question.

--- task --- Tire le bloc `demander et attendre`{:class="block3sensing"} dans le panneau sprite et change la question sur `Par combien d'étapes dois-je le grossir?`{:class="block3sensing"}

Puis ajoute-le à ton programme, juste après avoir défini `étapes`{:class=block3variables"} sur `0`, comme ceci:

```blocks3
    quand le drapeau vert pressé
    mettre [étapes v] à [0]
+    demander [Par combien d’étapes dois-je le grossir?] et attendre
    relever le stylo
```

--- /task ---

Maintenant que ton programme pose une question, tu en as besoin pour retenir la réponse! Il s'avère que Scratch a une variable spéciale appelée `réponse`{:class="block3sensing"}, où il stocke la réponse la plus récente reçue. Tu peux trouver cette variable parmi les blocs **Capteur**.

--- task --- En utilisant un bloc `mettre à`{:class="block3variables"} de **Variables**, prends la valeur de `réponse`{:class="block3sensing"} et stocke la dans la variable `augmenter`{:class="block3variables"} comme ceci:

```blocks3
    demander [Par combien d’étapes dois-je le grossir?] et attendre
+    mettre [augmenter v] à (réponse)
```

--- /task ---

--- task --- Maintenant, fais la même chose avec `degrés`{:class="block3variables"}, demandant `Combien de degrés dois-je tourner?`{:class="block3sensing"} et mémoriser la valeur de `réponse`{:class="block3sensing"} dans `degrés`{:class="block3variables"}:

```blocks3
    mettre [augmenter v] à (réponse)
+    demander [Combien de degrés dois-je tourner?] et attendre
+    mettre [degrés v] à (réponse)
```

--- /task ---

--- task --- Vérifie que ton programme ressemble maintenant à celui ci-dessous et exécute-le plusieurs fois avec des numéros différents. Écris les réponses qui rendent les images les plus cool. Tu en auras besoin dans une étape ultérieure!

```blocks3
    quand le drapeau vert pressé
    mettre [étapes v] à [0]
    demander [Par combien d'étapes dois-je le grossir?] et attendre
    mettre [augmenter v] à (réponse)
    demander [Combien de degrés devrais-je tourner?] et attendre
    mettre [degrés v] à (réponse)
    relever le stylo
    cacher
    effacer tout
    aller à x: (0) y: (0)
    mettre la couleur du stylo à [#4a6cd4]
    stylo en position d'écriture
    répéter jusqu'à ce que <touche le [bord v] ?> 
        avancer de (étapes) pas
        tourner droite de (degrés) degrés
        ajouter (augmenter) à [étapes v]
```

--- /task ---