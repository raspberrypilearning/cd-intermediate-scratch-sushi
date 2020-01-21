## Fă totul aleatoriu

De fapt, poți utiliza numere aleatorii pentru a face întreg programul să ruleze încontinuu, schimbând șablonul de fiecare dată! O să arate precum screensaver-ele realizate în anii 1990... pe care, probabil, nu ți le vei aminti, dar întreabă-l pe unul dintre părinții tăi!

Ai nevoie de câteva modificări pentru a face acest lucru să se întâmple. Prima dintre ele este că trebuie să setezi variabilele `creștere`{:class="block3variables“} și `grade`{:class="block3variables"} cu valori adăugate în mod aleatoriu, în locul introducerii manuale de la tastatură de către utilizator. Deci, trebuie să schimbi unele dintre blocurile de cod.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    când se dă click pe stegulețul verde
    setează [pași v] la [0]
-    întreabă [Cu câți pași trebuie să crească?] și așteaptă
+    setează [creștere v] la (alege aleator între (1) și (10))
-    întreabă [Cu câte grade trebuie să mă întorc?] și așteaptă
+   setează [grade v] la (alege aleator între (1) și (180))
    stilou sus
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    când se dă click pe stegulețul verde
+    la infinit 
        setează [pași v] la [0]
        setează [creștere v] la (alege aleator între (1) și (10))
        setează [grade v] la (alege aleator între (1) și (180))
        stilou sus
        ascunde
        șterge tot
        mergi la x: (0) y: (0)
        setează culoarea stiloului la [#4a6cd4]
        stilou jos
        repeta până când <atinge [marginea v] ?> 
            mergi (pași) pași
            rotește-te cw (grade) grade
            modifică [pași v] cu (creștere)
        end
    end
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!