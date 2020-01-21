## Demande d'entrée

Ok, ça devient plutôt cool, mais c'est un peu ennuyeux de devoir modifier ton code à chaque fois que tu veux dessiner un motif différent. Ne serait-il pas bon de demander au programme de te demander des valeurs à utiliser? Tu peux le faire!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    répéter jusqu'à <touching [edge v] ?> 
        déplacer (étapes) pas
        tourner cw (degrés :: variables) degrés
        changer [étapes v] de (augmenter :: variables)
    fin
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    lorsque le drapeau vert est cliqué 
    définir [étapes v] sur [0]
+ demandez [Par combien d’étapes dois-je le grossir?] et attendre
    relever le stylo
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    demander [Par combien d'étapes dois-je le grossir?] et attendre
+ définir [augmenter v] sur (répondre)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    définir [augmenter v] sur (réponse)
+ demander [Combien de degrés dois-je tourner?] et attendre
+ définir [degrés v] sur (réponse)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

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