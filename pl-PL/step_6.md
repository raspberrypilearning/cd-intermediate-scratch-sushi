## Ustaw wszystko losowo

Możesz użyć liczb losowych, aby cały program był uruchamiany w kółko, zmieniając wzór za każdym razem! Będzie to wyglądało trochę jak wygaszacze ekranu w latach 90.... których prawdopodobnie nie pamiętasz, ale zapytaj jednego z rodziców!

Potrzebujesz kilku zmian, aby tak się stało. Pierwszą z nich jest to, że musisz ustawić zmienne `powiększenie`{:class="block3variables"} i `stopnie`{:class="block3variables"} na losowe wartości, zamiast pytać o nie użytkownika. Więc musisz zmienić niektóre bloki kodu.

--- task --- Usuń pytania z kodu i zaktualizuj je, aby zamiast nich używać liczb losowych.

```blocks3
    kiedy kliknięto zieloną flagę
    ustaw [kroki v] na [0]
- zapytaj [o ile kroków powinienem powiększyć się?] i czekaj
+ ustaw [powiększenie v] na (losuj liczbę od (1) do (10))
- zapytaj [o ile stopni powinienem się obrócić?] i czekaj
+ ustaw [stopnie v] na (losuj liczbę od (1) do (180))
    podnieś pisak
```

--- /task ---

Jeśli teraz uruchomisz program, przekonasz się, że rysuje losowy wzór, ale tylko raz. Jak myślisz, dlaczego tak jest?

To dlatego, że pętla działa tylko do momentu, kiedy dojdzie do krawędzi sceny.

--- task --- Potrzebujesz kolejnej pętli, która działa wiecznie (a więc blok `zawsze`{:class="block3control"}) na zewnątrz bieżącej pętli, aby ciągle się powtarzała. Po prostu przeciągnij jedną z sekcji **Kontrola** i dodaj do niej cały swój kod.

```blocks3
    kiedy kliknięto zieloną flagę
+ zawsze 
        ustaw [kroki v] na [0]
        ustaw [powiększenie v] na (losuj liczbę od (1) do (10))
        ustaw [stopnie v] na (losuj liczbę od (1) do (180))
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
    koniec
```

--- /task ---

Teraz naprawdę masz coś niesamowitego do oglądania!

Jednak możesz zauważyć, że od czasu do czasu komputer rysuje coś, co wygląda kiepsko. Dzieje się tak, ponieważ czasami wartości dla niektórych z tych zmiennych są po prostu złymi wyborami, a niektóre **kombinacje tych wartości** to także zły wybór.

Na następnej karcie pomożesz komputerowi wybrać tylko dobre kombinacje!