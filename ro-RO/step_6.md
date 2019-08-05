## Fă totul aleatoriu

De fapt, poți utiliza numere aleatorii pentru a face întreg programul să ruleze încontinuu, schimbând șablonul de fiecare dată! O să arate precum screensaver-ele realizate în anii 1990... pe care, probabil, nu ți le vei aminti, dar întreabă-l pe unul dintre părinții tăi!

Ai nevoie de câteva modificări pentru a face acest lucru să se întâmple. Prima dintre ele este că trebuie să setezi variabilele `creștere`{:class="block3variables“} și `grade`{:class="block3variables"} cu valori adăugate în mod aleatoriu, în locul introducerii manuale de la tastatură de către utilizator. Deci, trebuie să schimbi unele dintre blocurile de cod.

--- task --- Elimină întrebările din codul tău și actualizează-l pentru a utiliza numere aleatorii în schimb.

```blocks3
    când se dă click pe stegulețul verde
    setează [pași v] la [0]
-    întreabă [Cu câți pași trebuie să crească?] și așteaptă
+    setează [creștere v] la (alege aleator între (1) și (10))
-    întreabă [Cu câte grade trebuie să mă întorc?] și așteaptă
+   setează [grade v] la (alege aleator între (1) și (180))
    stilou sus
```

--- /task ---

Dacă rulezi programul tău acum, vei observa că desenează un șablon aleatoriu, dar o singură dată. De ce crezi că se întâmplă asta?

Asta se datorează faptului că bucla rulează numai până când ajunge la marginea Scenei.

--- task --- Ai nevoie de o altă buclă care rulează încontinuu (deci, un bloc `la infinit`{:class="block3control"}) în afara buclei curente pentru a o menține în mișcare mereu. Doar trage una din secțiunea **Control** și adaugă tot codul tău în ea.

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

--- /task ---

Acum ai într-adevăr ceva minunat la care să te uiți!

Cu toate acestea, poți observa că, din când în când, computerul desenează ceva care arată destul de... rău. Acest lucru se datorează faptului că unele numere pentru unele dintre aceste variabile sunt doar alegeri nepotrivite, iar unele **combinații ale acestor numere** sunt de asemenea alegeri nepotrivite.

Pe următorul card, vei ajuta computer-ul să aleagă numai combinații potrivite!