## Demande d'entrée

Ok, ça devient plutôt cool, mais c'est un peu ennuyeux de devoir modifier ton code à chaque fois que tu veux dessiner un motif différent. Ne serait-il pas bon de demander au programme de te demander des valeurs à utiliser? Tu peux le faire!

\--- task \---

Tout d'abord, va à la section **Variables** et crée des variables nommées `degrés`{:class="block3variables"} et `augmenter`{:class="block3variables"}.

\--- /task \---

\--- task \---

Ajoute maintenant les nouvelles variables à ton code comme ceci :

```blocks3
    répéter jusqu'à <touching [edge v] ?> 
        déplacer (étapes) pas
        tourner cw (degrés :: variables) degrés
        changer [étapes v] de (augmenter :: variables)
    fin
```

\--- /task \---

Maintenant, tu dois demander des valeurs pour ces deux variables et les stocker. Pour ce faire, utilise un bloc **Capteur** appelé `Demander et attendre`{:class="block3sensing"}, dans lequel tu peux taper une question.

\--- task \---

Tire le bloc `Demander et attendre`{:class="block3sensing"} dans le panneau sprite et change la question sur `Par combien d'étapes dois-je le grossir?`{:class="block3sensing"}

Puis ajoute-le à ton programme, juste après avoir défini `étapes`{:class=block3variables"} sur `0`, comme ceci:

```blocks3
    lorsque le drapeau vert est cliqué 
    définir [étapes v] sur [0]
+ demandez [Par combien d’étapes dois-je le grossir?] et attendre
    relever le stylo
```

\--- /task \---

Maintenant que ton programme pose une question, tu as besoin qu'il retienne la réponse ! Il s'avère que Scratch a une variable spéciale appelée `réponse`{:class="block3sensing"}, où il stocke la réponse la plus récente reçue. Tu peux trouver cette variable parmi les blocs **Capteur**.

\--- task \---

En utilisant un bloc `définir sur `{:class="block3variables"} de **Variables**, prends la valeur de `réponse`{:class="block3sensing"} et stocke la dans la variable `augmenter`{:class="block3variables"} comme ceci :

```blocks3
    demander [Par combien d'étapes dois-je le grossir?] et attendre
+ définir [augmenter v] sur (répondre)
```

\--- /task \---

\--- task \---

Maintenant, fais la même chose avec `degrés`{:class="block3variables"}, demandant `Combien de degrés dois-je tourner?`{:class="block3sensing"} et mémoriser la valeur de `demander`{:class="block3sensing"} dans `degrés`{:class="block3variables"}:

```blocks3
    définir [augmenter v] sur (réponse)
+ demander [Combien de degrés dois-je tourner?] et attendre
+ définir [degrés v] sur (réponse)
```

\--- /task \---

\--- task \---

Vérifie que ton programme ressemble maintenant à celui ci-dessous et exécute-le plusieurs fois avec des numéros différents. Écris les réponses qui rendent les images les plus cool. Tu en auras besoin dans une étape ultérieure !

```blocks3
    lorsque le drapeau vert est cliqué
    définir [étapes v] sur [0]
    demander [Par combien d'étapes dois-je le grossir?] et attendre
    définir [augmentez v] sur (réponse)
    demander [Combien de degrés devrais-je tourner?] et attendre
    définir [degrés v] sur (répondre)
    relever le stylo
    masquer
    effacer
    aller à x: (0) y: (0)
    définir la couleur du stylo sur [# 4a6cd4]
    stylo en position d'écriture
    répéter jusqu'à <touching [edge v] ?> 
        déplacer (étapes) pas
        tourner cw (degrés) degrés
        changer [étapes v] par (augmenter)
    fin
```

\--- /task \---