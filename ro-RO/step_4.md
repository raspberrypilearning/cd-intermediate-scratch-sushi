## Obținerea datelor de intrare

Ok, acest lucru este destul de interesant, dar este un pic plictisitor faptul că trebuie să-ți editezi codul de fiecare dată când vrei să desenezi un șablon diferit. Nu ar fi mai bine ca programul să-ți ceară ce valori să folosești? Poți să faci asta!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    repetă până când <atinge [marginea v] ?> 
        mergi (pași) pași
        rotește-te cw (grade ::variables) grade
        modifică [pași v] cu (creștere ::variables)
    end
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    când se dă click pe stegulețul verde
    modifică [pași v] cu [0]
+    întreabă [Cu câți pași trebuie să crească?] și așteaptă
    stilou sus
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    întreabă [Cu câți pași ar trebui să crească?] și așteaptă
+    setează [creștere v] la (răspuns)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    setează [creștere v] la (răspuns)
+    întreabă [Câte grade trebuie să mă întorc?] și așteaptă
+    setează [grade v] la (răspuns)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    când se dă click pe stegulețul verde
    setează [pași v] la [0]
    întreabă [Cu câți pași ar trebuie să crească?] și așteaptă
    setează [creștere v] la (răspuns)
    întreabă [Câte grade ar trebui să mă întorc?] și așteaptă
    setează [grade v] la (răspuns)
    stilou sus
    ascunde
    șterge tot
    mergi la x: (0) y: (0)
    setează culoarea stiloului la [#4a6cd4]
    stilou jos
    repetă până când <atinge [marginea v] ?>
        mergi (pași) pași
        rotește-te cw (grade) grade
        modifică [pași v] cu (creștere)
    end
```

\--- /task \---