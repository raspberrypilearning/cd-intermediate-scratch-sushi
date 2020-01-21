## Ajută computer-ul

Îți amintești când ți-am spus câțiva pași înapoi că trebuie să notezi unele dintre valorile tale preferate pentru `creștere`{:class="block3variables"} și `grade`{:class="block3variables"}, acelea care au generat cele mai faine șabloane? Dacă nu ai făcut acest lucru, nu îți fă griji: poți doar să urmărești programul la întâmplare pentru o vreme și să notezi combinațiile care dau rezultate excelente.

O să înveți Scratch aceste combinații de valori, astfel încât să le poată folosi pentru a face doar imagini grozave!

Pentru a face acest lucru, vei avea nevoie de o **listă**. Vei găsi listele cu variabile în secțiunea **Variabile**. La fel ca și în cazul variabilelor tale, va trebui să îți creezi prima listă!

\--- task \---

Click **Make a List**, and enter `Degrees List`{:class="block3variables"} as the name.

![](images/makeAList.png)

\--- /task \---

Your list, which is empty at the moment, will appear on the Stage, and you'll see a bunch of blocks for it in **Variables**.

![](images/listBlocks.png)

\--- task \---

Make another list called `Increase List`{:class="block3variables"}

\--- /task \---

\--- task \---

Now, by clicking on the little plus sign (**+**) at the bottom of the lists, add in the first pair of values of `increase`{:class="block3variables"} and `degrees`{:class="block3variables"} you liked, each value into the right list. Do this again to add the second pair of values. This will be enough for now — you'll add the rest of the value pairs you like later!

![](images/helping2.png)

Make sure that the `degrees`{:class="block3variables"} value and the `increase`{:class="block3variables"} value that worked well together are at the same position in the `Degrees List`{:class="block3variables"} and the `Increase List`{:class="block3variables"}. They need to be there so your program can match them up again using their position!

\--- /task \---

Now you have the lists, you just need to get your code to read them and loop over them! To do this, you’re going to use a new variable to act as a counter, some **incrementing**, and an `if then`{:class="block3control"} **Control** block.

## \--- collapse \---

## title: Ce înseamnă incrementare?

To increment something means to add something to it.

You will use a variable to act as a counter to keep track of what position you're at in your lists. To move through the lists, you'll keep incrementing the counter by `1` (so, adding `1` to it) until you get to the end of the list.

\--- /collapse \---

\--- task \---

Create a new variable called `counter`{:class="block3variables"}, and update your code to look like this:

```blocks3
    când se dă click pe stegulețul verde
    setează [contor v] la [0]
    la infinit 
+        dacă <(contor) = (lungimea lui [Listă creștere v] :: list)> atunci 
+        setează [contor v] la [0]
        end
+        modifică [contor v] cu (1)
        setează [pași v] la [0]
+        setează [creștere v] la (element (contor) din [Listă creștere v] :: list)
+        setează [grade v] la (element (contor) din [Listă grade v] :: list)
        stilou sus
        ascunde
        șterge tot
        mergi la x: (0) y: (0)
        setează culoarea stiloului la [#4a6cd4]
        stilou jos
        repeta pana când < atinge [marginea v] ?>
            mergi (pași) pași
            rotește-te cw (grade) grade
            modifică [pași v] cu (creștere)
        end
    end
```

\--- /task \---

Notice the new blocks that:

1. Setează `contor`{:class="block3variables"} la `0`, în afara tuturor buclelor.
2. Verifică dacă numărul stocat în `counter`{:class="block3variables"} este egal cu lungimea listei și, dacă da, setează blocul `counter`{:class="block3variables"} la `0`. Asta înseamnă că această variabilă va avea întotdeauna numărul unei poziții din liste și nu va fi mai mare ca aceasta.
3. Adaugă `1` la `contor`{:class="block3variables"}.
4. Alege elementul din `Listă creștere`{:class="block3variables"} care este în poziția descrisă de `contor`{:class="block3variables"} și îl pune în în variabila `creștere`{:class="block3variables"}. Același lucru îl face și pentru `Listă grade`{:class="block3variables"} și variabila `grade`{:class="block3variables"}.

## \--- collapse \---

## title: Cum funcționează codul?

This is what happens when you run your program:

1. Setează blocul `contor`{:class="block3variables"} la `0`.
2. Pornește bucla `la infinit`{:class="block3control"}.
3. Verifică dacă `contor`{:class="block3variables"} (`0`) este egal cu lungimea listei `Listă creștere`{:class="block3variables"} (`2`). Nu este.
4. Schimbă `contorul`{:class="block3variables"} cu `1`. Acum, `contor`{:class="block3variables"} = `1`.
5. Setează `pași`{:class="block3variables"} la `0`.
6. Ia elementul din poziția indicată de `contor`{:class="block3variables"} (`1`) din `Listă creștere`{:class="block3variables"} și îl pune în `creștere`{:class="block3variables"}.
7. Ia elementul din poziția indicată de `contor`{:class="block3variables"} (`1`) din `Listă grade`{:class="block3variables"} și îl pune în `grade`{:class="block3variables"}.
8. Face toate lucrurile legate de desenarea șabloanelor.
9. Repornește bucla `la infinit`{:class="block3control"}:
10. Verifică dacă `contor`{:class="block3variables"} (`1`) este egal cu lungimea listei `Listă creștere`{:class="block3variables"} (`2`). Nu este.
11. Schimbă `contorul`{:class="block3variables"} cu `1`. Acum, `contor`{:class="block3variables"} = `2`.
12. Setează `pași`{:class="block3variables"} la `0`.
13. Ia elementul din poziția indicată de `contor`{:class="block3variables"} (`2`) din `Listă creștere`{:class="block3variables"} și îl pune în `creștere`{:class="block3variables"}.
14. Ia elementul din poziția indicată de `contor`{:class="block3variables"} (`2`) din `Listă grade`{:class="block3variables"} și îl pune în `grade`{:class="block3variables"}.
15. Face toate lucrurile legate de desenarea șabloanelor.
16. Repornește bucla `la infinit`{:class="block3control"}:
17. Verifică dacă `contor`{:class="block3variables"} (`2`) este egal cu lungimea listei `Listă creștere`{:class="block3variables"} (`2`). Este!
18. Setează `contor`{:class="block3variables"} la `0`.
19. Continuă de la **pasul 4** din această listă, într-o buclă care rulează la infinit!

\--- /collapse \---

\--- task \---

Once you're happy with the code, go ahead and add the rest of the pairs of values you noted down to the `Degrees List`{:class="block3variables"} and the `Increase List`{:class="block3variables"}.

\--- /task \---

That's it! Sit back and watch your program keep drawing lovely patterns in a never-ending loop! If you want to add more patterns, you can: just add more pairs of numbers to the two lists and restart the program.