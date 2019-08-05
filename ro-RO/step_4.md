## Obținerea datelor de intrare

Ok, acest lucru este destul de interesant, dar este un pic plictisitor faptul că trebuie să-ți editezi codul de fiecare dată când vrei să desenezi un șablon diferit. Nu ar fi mai bine ca programul să-ți ceară ce valori să folosești? Poți să faci asta!

--- task --- Mai întâi, mergi la secțiunea **Variabile** și creează variabilele numite `grade`{:class="block3variables"} și `creștere`{:class="block3variables"}. --- /task ---

--- task --- Acum, adaugă variabilele noi în codul tău astfel:

```blocks3
    repetă până când <atinge [marginea v] ?> 
        mergi (pași) pași
        rotește-te cw (grade ::variables) grade
        modifică [pași v] cu (creștere ::variables)
    end
```

--- /task ---

Acum, trebuie să soliciți valorile pentru aceste două variabile și să le păstrezi. Fă acest lucru utilizând un bloc **Detectare** numit `Întreabă și așteaptă`{:class="block3sensing"}, la care poți introduce o întrebare.

--- task --- Trage blocul `Întreabă și așteaptă`{:class="block3sensing"} în panoul personajului tău și schimbă întrebarea cu `Cu câți pași trebuie să crească?`{:class="block3sensing"}

Apoi adaug-o în programul tău, imediat după ce ai setat `pași`{:class="block3variables"} la `0`, astfel:

```blocks3
    când se dă click pe stegulețul verde
    modifică [pași v] cu [0]
+    întreabă [Cu câți pași trebuie să crească?] și așteaptă
    stilou sus
```

--- /task ---

Acum că ai programul tău de întrebat, trebuie să-ți amintești răspunsul! Se pare că Scratch are o variabilă specială numită `răspuns`{:class="block3sensing"}, unde stochează cel mai recent răspuns pe care l-a primit. Poți găsi această variabilă în blocurile **Detectare**.

--- task --- Folosind un bloc `setează la`{:class="block3variables"} din **Variabile**, ia valoarea lui `răspuns`{:class="block3sensing"} și păstreaz-o în variabila `creștere`{:class="block3variables"}, astfel:

```blocks3
    întreabă [Cu câți pași ar trebui să crească?] și așteaptă
+    setează [creștere v] la (răspuns)
```

--- /task ---

--- task --- Fă același lucru cu `grade`{:class="block3variables"}, întrebând `Câte grade trebuie să mă întorc?`{:class="block3sensing"} și stochează valorile din `răspuns`{:class="block3sensing"} în `grade`{:class="block3variables"}:

```blocks3
    setează [creștere v] la (răspuns)
+    întreabă [Câte grade trebuie să mă întorc?] și așteaptă
+    setează [grade v] la (răspuns)
```

--- /task ---

--- task --- Verifică programul tău dacă arată precum cel de mai jos și execută-l de câteva ori cu numere diferite. Scrie răspunsurile care fac cele mai tari poze. Vei avea nevoie de ele într-un pas ulterior!

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

--- /task ---