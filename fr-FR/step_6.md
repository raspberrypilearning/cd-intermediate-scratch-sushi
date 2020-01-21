## Randomiser le tout

Tu peux utiliser des nombres aléatoires pour que tout le programme se répète, en modifiant le motif à chaque fois! Cela ressemblera un peu aux écrans de veille des années 90 ... dont tu ne te souviens probablement pas, mais demande à l'un de tes parents!

Tu as besoin de quelques modifications pour y arriver. La première consiste à définir les variables `augmenter`{:class="block3variables"} et `degrés`{:class="block3variables"} aléatoirement plutôt que de les demander à l'utilisateur. Tu dois donc modifier certains de tes blocs de code.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

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

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

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

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!