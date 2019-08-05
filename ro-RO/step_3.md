## Șabloane de desen

Acum, ai un program care desenează o linie, dar desenează o singură linie. E un pic plictisitor! Ai putea folosi bucla `la infinit`{:class="block3control"} pentru a desena ceva încontinuu, dar apoi vei obține desene care ies din Scenă!

Deci, ai nevoie să utilizezi un tip diferit de bucle de tip `repetă până când`{:class="block3control"}, pe care îl vei găsi în secțiunea **Control**. Acest tip de buclă va repeta o acțiune, **până când** o condiție adevărat/fals este îndeplinită.

--- task --- Alege un bloc `repetă până când`{:class="block3control"} din secțiunea **Control** și apoi pune blocurile `mergi`{:class="block3motion"} și `rotește-te`{:class="block3motion"} în interiorul acestuia, astfel:

```blocks3
+    repetă până când <> 
        mergi (50) pași
        rotește-te cw (15) grade
    end
```

--- /task ---

--- task --- Acum, dă click pe steagul verde pentru a rula programul de câteva ori și a vedea ce se întâmplă. Vei observa două lucruri: stiloul începe întotdeauna prin trasarea unei linii spre mijlocul scenei și nu se oprește la margine. --- /task ---

--- collapse ---
---
title: De ce stiloul face acest lucru?
---

Stiloul începe întotdeauna să deseneze în direcția de mijloc, deoarece primul bloc de **Mișcare** care se execută după blocul `stilou jos`{:class="block3extensions"} este de tip `mergi la x: 0 y: 0`{:class="block3motion"}. Așadar, stiloul va desena o linie pe măsură ce se va deplasa spre centrul scenei.

Stiloul nu se oprește la marginea scenei, pentru că nu a fost încă adaugată în bucla `repeta până când`{:class="block3control"} condiția ce trebuie verificată. Asta înseamnă că acea condiția nu poate fi îndeplinită, astfel încât buclă va rula încontinuu. Acest lucru înseamnă că acum, bucla funcționează ca o buclă `la infinit`{:class="block3control"}.

--- /collapse ---

--- task --- Mută blocul `mergi la x: 0 y: 0`{:class="block3motion"} înainte de blocul `stilou jos`{:class="block3extensions"} și adaugă, din secțiunea **Stilou**, un bloc `stilou sus`{:class="block3extensions"} chiar la începutul codului. --- /task ---

Este timpul să rezolvi bucla `repetă până când`{:class="block3control"} astfel încât să se oprească atunci când dorești. Încearcă să îți dați seama dacă personajul (invizibil) atinge marginea scenei, iar dacă este cazul vei folosi un bloc din secțiunea **Detectare** , blocul `atinge ?`{:class="block3sensing"}.

--- task --- Adaugă blocul `atinge ?`{:class="block3sensing"} în bucla ta `repetă până când`{:class="block3control"} și selectează `marginea`{:class="block3sensing"}. Apoi bucla va rula **până când** personajul (invizibil) atinge marginea Scenei.

```blocks3
    stilou jos
+    repeta până când <atinge [marginea v] ?> 
        mergi (50) pași
        rotește-te cw (15) grade
    end
```

--- /task ---

--- task --- Modifică numărul de pași din blocul `mergi`{:class="block3motion"} la `5` și verifică dacă programul tău se potrivește cu acesta înainte de a-l testa:

```blocks3
    când se dă click pe stegulețul verde
    stilou sus
    ascunde
    șterge tot
    mergi la x: (0) y: (0)
    setează culoarea stiloului la [#4a6cd4]
    stilou jos
    repeta până când <atinge [marginea v] ?>
        mergi (5) pași
        rotește-te cw (15) grade
    end
```

--- /task ---

Dacă rulezi codul acum, vei vedea că desenul stiloului se află întotdeauna pe Scenă.

Nu numai asta, dar programul tău s-a transformat într-un program de desenat cercuri! Ce se întâmplă aici este faptul că acele rotiri de 15 grade se cumuleaza până la 360 de grade, astfel încât stiloul tău se transformă într-un cerc complet. Vei schimba modul în care se mișcă acum pentru a face un pas să dureze mai mult de fiecare dată, pentru a ieși în spirală. Pentru aceasta, vei avea nevoie de o **variabilă**.

Variabilele sunt în general locuri etichetate pentru a stoca numere sau alte informații care te interesează. Poți să le creezi în secțiunea de blocuri **Variabile**.

--- task --- Fă o variabilă numită `pași`{:class="block3variables"}, apoi adaugă un bloc de `setează pași la 0`{:class="block3variables"} la începutul programului.

```blocks3
    când se dă click pe stegulețul verde
+   setează [pași v] la [0]
    stilou sus
```

--- /task ---

--- task --- Apoi, folosește valoarea `pași`{:class="block3variables"} în loc de `5` în blocul `mergi`{:class="block3motion"} și adaugă `modifică pași cu 1`{:class="block3variables"} ca parte din bucla ta:

```blocks3
    stilou jos
    repeta până când <touching [edge v] ?> 
+       mergi (pași) pași
        rotește-te cw (76) grade
+        modifică [pași v] cu (1)
    end
```

--- /task ---

Crezi că contează unde ai pus în buclă blocul `modifică pașii cu 1`{:class="block3variables"}?

--- collapse ---
---
title: Introducerea codului în ordinea corectă
---

Când decizi în ce ordine să introduci blocurile, gândește-te la ceea ce face fiecare bloc și la ce dorești să facă codul tău.

În acest caz, dorești ca stiloul să se miște, apoi să se întoarcă, din nou și din nou. De fiecare dată când face acest lucru, vrei să mergi un pas în plus.

Așadar, este logic să pui blocul `modifică pași cu 1`{:class="block3variables"} **după** blocul `mergi`{:class="block3motion"}. Cu toate acestea, după mutare, nu contează dacă stiloul se întoarce mai întâi și apoi se modifică numărul de pași sau dacă numărul de pași se schimbă mai întâi și apoi se schimbă stiloul.

--- /collapse ---

--- task --- Acum, rulează programul și încearcă, de asemenea, să schimbi numărul de grade (încearcă `76` și `120`)! --- /task ---