## Linii mai interesante

Este timpul să adaugi culoare! Chiar acum, linia ta are o culoare, dar **Stilou** are blocuri care pot schimba culoarea. Iar cu blocul **Operator** potrivit, poți chiar schimba culoarea aleatoriu!

Blocul de schimbare a culorii **Stilou** este `schimbă culoarea stiloului cu`{:class="block3extensions"}:

```blocks3
    schimbă culoarea stiloului cu (10)
```

--- task --- Ia unul din acele blocuri și pune-l în bucla `repetă până când`{:class="block3control"}, astfel:

```blocks3
    repetă până când <atinge [marginea v] ?>
+        schimbă culoarea stiloului cu (10)
        mergi (pași) pași
        rotește-te cw (grade ::variables) grade
        modifică [pași v] cu (creștere ::variables)
    end
```

--- /task ---

E minunat, dar cam previzibil. Poți face un pic mai distractiv dacă adaugi un număr aleatoriu în ea, astfel încât culoarea să se schimbe aleatoriu.

--- task --- Introdu blocul **Operator** pentru număr aleator în blocul `schimbă culoarea stiloului cu`{:class="block3extensions"} și alege câteva valori pentru vedea ce se întâmplă. Aș încerca `1` și `100` pentru început.

```blocks3
    repetă până când <atinge [marginea v] ?>
+        schimbă culoarea stiloului cu (alege aleator între (1) și (100))
        mergi (pași) pași
        rotește-te cw (grade ::variables) grade
        modifică [pași v] cu (creștere ::variables)
    end
```

--- /task ---

--- task --- Încearcă să-l rulezi din nou, și urmărește curcubeul aleator! --- /task ---