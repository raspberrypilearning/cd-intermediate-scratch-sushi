## Pytanie o dane wejściowe

Ok, robi się całkiem fajnie, ale nudne jest edytowanie kodu za każdym razem, gdy chcesz narysować inny wzór. Czy nie byłoby dobrze, gdyby program poprosił cię o podanie wartości? Możesz to zrobić!

\--- task \---

Najpierw przejdź do sekcji **Zmienne** i utwórz zmienne o nazwie `stopnie`{:class="block3variables"} i `powiększenie`{:class="block3variables"}.

\--- /task \---

\--- task \---

Teraz dodaj nowe zmienne do swojego kodu w następujący sposób:

```blocks3
    powtarzaj aż <touching [edge v] ?> 
        przesuń o (kroki) kroków
        obróć w prawo o (stopnie ::zmienne) stopni
        zmień [kroki v] o (powiększenie ::zmienne)
    koniec
```

\--- /task \---

Teraz musisz poprosić o wartości dla tych dwóch zmiennych i zapisać je. Robisz to za pomocą bloku z sekcji **Czujniki** o nazwie `Zapytaj i czekaj`{:class="block3sensing"}, do którego możesz wpisać pytanie.

\--- task \---

Przeciągnij blok `Zapytaj i czekaj`{:class="block3sensing"} do panelu duszka i zmień pytanie na `O ile kroków powinienem się powiększyć?`{:class="block3sensing"}

Następnie dodaj go do swojego programu, zaraz po ustawieniu `kroki`{:class="block3variables"} na `0`, tak:

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [kroki v] na [0]
+ zapytaj [o ile kroków powinienem się powiększyć?] i czekaj
    podnieś pisak
```

\--- /task \---

Teraz twój program potrafi zadać pytanie, potrzebujesz jeszcze, żeby zapamiętał odpowiedź! Okazuje się, że Scratch ma specjalną zmienną o nazwie `odpowiedź`{:class="block3sensing"}, w której przechowuje najnowszą odpowiedź, którą otrzymał. Możesz znaleźć tę zmienną wśród bloków w sekcji **Czujniki**.

\--- task \---

Używając bloku `ustaw na`{:class="block3variables"} z sekcji **Zmienne**, weź wartość `odpowiedź`{:class="block3sensing"} i zapisz ją w zmiennej `powiększenie`{:class="block3variables"} tak jak poniżej:

```blocks3
    zapytaj [o ile kroków powinienem się powiększyć?] i czekaj
+ ustaw [powiększenie v] na (odpowiedź)
```

\--- /task \---

\--- task \---

Zrób teraz to samo ze zmienną `stopnie`{:class="block3variables"}, pytając `Ile stopni powinienem się obrócić?`{:class="block3sensing"} i przechowaj wartość `odpowiedź`{:class="block3sensing"} w zmiennej `stopnie`{:class="block3variables"}:

```blocks3
    ustaw [powiększenie v] na (odpowiedź)
+ zapytaj [o ile stopni powinienem się obrócić?] i czekaj
+ ustaw [stopnie v] na (odpowiedź)
```

\--- /task \---

\--- task \---

Sprawdź, czy twój program wygląda teraz tak jak ten poniżej i uruchom go kilka razy używając różnych wartości. Zapisz odpowiedzi, które robią najfajniejsze obrazki. Będziesz ich potrzebować w późniejszym kroku!

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [kroki v] na [0]
    zapytaj [o ile kroków powinienem się powiększyć?] i czekaj
    ustaw [powiększenie v] na (odpowiedź)
    zapytaj [o ile stopni powinienem się obrócić?] i czekaj
    ustaw [stopnie v] na (odpowiedź)
    podnieś pisak
    ukryj
    wyczyść wszystko
    idź do x: (0) y: (0)
    ustaw kolor pisaka na [#4a6cd4]
    przyłóż pisak
    powtarzaj aż <touching [edge v] ?> 
        przesuń o (kroki) kroki
        obróć w prawo o (stopnie) stopni
        zmień [kroki v] o (powiększenie)
    koniec
```

\--- /task \---