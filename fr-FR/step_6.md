## Randomiser le tout

Tu peux utiliser des nombres aléatoires pour que tout le programme se répète, en modifiant le motif à chaque fois! Cela ressemblera un peu aux écrans de veille des années 90 ... dont tu ne te souviens probablement pas, mais demande à l'un de tes parents!

Tu as besoin de quelques modifications pour y arriver. La première consiste à définir les variables `augmenter`{:class="block3variables"} et `degrés`{:class="block3variables"} aléatoirement plutôt que de les demander à l'utilisateur. Tu dois donc modifier certains de tes blocs de code.

\--- task \---

Supprime les questions de ton code et mets-le à jour afin qu'il utilise des nombres aléatoires.

```blocks3
    lorsque le drapeau vert est cliqué
    définir [étapes v] sur [0]
- demandez à [Par combien d'étape devrais-je le grossir?] et attendre
+ définir [augmenter v] sur (choisis au hasard de (1) à (10))
- demander [Combien de degrés dois-je tourner?] et attendre
+ définir [degrés v] sur (choisir au hasard de (1) à (180))
    relever le stylo
```

\--- /task \---

Si tu exécutes ton programme maintenant, tu constateras qu'il dessine un motif aléatoire, mais une seule fois. Pourquoi penses-tu que c'est le cas ?

C'est parce que la boucle s’exécute seulement jusqu'à ce qu'elle atteigne le bord de la scène.

\--- task \---

Tu as besoin d'une autre boucle qui tourne pour toujours (donc un bloc `répéter indéfiniment`{:class="block3control"}!) en dehors de la boucle actuelle pour qu'elle continue encore et encore. Il suffit de faire glisser l’un des éléments de la section **Contrôle** et d’y ajouter tous tes autres codes.

```blocks3
    lorsque le drapeau vert est cliqué 
+ répéter indéfiniment 
        définir [étapes v] sur [0]
        définir [augmenter v] sur (choisir au hasard de (1) à (10))
        définir [degrés v] sur (choisir au hasard de (1) à (180) )
        relever le stylo
        masquer
        effacer
        aller à x: (0) y: (0)
        définir la couleur du stylo sur [# 4a6cd4]
        stylo en position d'écriture
        répéter jusqu'à <touching [edge v] ?> 
            déplacer (étapes) pas
            tourner cw de (degrés) degrés 
            changer [étapes v] sur (augmenter)
        fin
    fin
```

\--- /task \---

Maintenant, tu as vraiment quelque chose de génial à regarder !

Cependant, tu remarqueras peut-être que de temps en temps, l'ordinateur dessine quelque chose qui a l'air plutôt… bizarre. En effet, certains nombres pour certaines de ces variables ne sont que de mauvais choix, et certaines **combinaisons** sont également de mauvais choix.

Sur la carte suivante, tu aideras l'ordinateur à choisir uniquement les bonnes combinaisons !