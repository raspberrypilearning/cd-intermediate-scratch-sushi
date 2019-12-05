## Rysowanie wzorów

Teraz masz program, który rysuje linię, ale tylko jedną linię. To trochę nudne! Możesz użyć pętli `zawsze`{:class="block3control"}, żeby rysować coś w kółko, ale wtedy otrzymasz rysunki, które wyjdą poza scenę!

Musisz więc użyć innego typu pętli o nazwie `powtarzaj aż`{:class="block3control"}, którą znajdziesz w sekcji **Kontrola**. Ten rodzaj pętli będzie robił coś w kółko, **aż** spełniony zostanie warunek Prawda/Fałsz.

--- task --- Weź blok `powtarzaj aż`{:class="block3control"} z sekcji **Kontrola** i umieść wewnątrz niego bloki `przesuń o`{:class="block3motion"} oraz `obróć o`{:class="block3motion"}, w taki sposób:

```blocks3
+ powtarzaj aż <> 
        przesuń o (50) kroków
        obróć w prawo o (15) stopni
    koniec
```

--- /task ---

--- task --- Teraz kliknij kilka razy zieloną flagę, aby uruchomić program i zobacz, co się stanie. Zauważysz dwie rzeczy: pióro zawsze zaczyna rysowanie linii w kierunku środka sceny i nie zatrzymuje się na krawędzi. --- /task ---

--- collapse ---
---
title: Dlaczego pióro tak się zachowuje?
---

Pióro zawsze zaczyna rysować w kierunku środka, ponieważ pierwszy blok **Ruch**, który wykonuje się po bloku `przyłóż pisak`{:class="block3extensions"} to `idź do x: 0 y: 0`{:class="block3motion"}. Tak więc pióro narysuje linię, przesuwając się do środka sceny.

Pióro nie zatrzymuje się na krawędzi sceny, ponieważ jeszcze nie powiedziałaś pętli `powtarzaj aż`{:class="block3control"}, jaki warunek ma sprawdzać. Oznacza to, że warunek nigdy nie zostanie spełniony, więc pętla będzie działać w nieskończoność. To znaczy, że teraz pętla działa jak pętla `zawsze`{:class="block3control"}.

--- /collapse ---

--- task --- Przesuń blok `idź do x: 0 y: 0`{:class="block3motion"} przed blok `Przyłóż pisak`{:class="block3extensions"} i dodaj, z sekcji **Pióro** blok `Podnieś pisak`{:class="block3extensions"} na samym początku kodu. --- /task ---

Czas naprawić Twoją pętlę `powtarzaj aż`{:class="block3control"}, aby się zatrzymała, kiedy tego chcesz. Chcesz dowiedzieć się, czy (niewidzialny) duszek dotyka krawędzi sceny, więc potrzebujesz bloku **Czujniki** - w tym przypadku bloku `dotyka ?`{:class="block3sensing"}.

--- task --- Dodaj blok `dotyka ?`{:class="block3sensing"} do pętli `powtarzaj aż`{:class="block3control"} i wybierz `krawędź`{:class="block3sensing"}. Następnie pętla będzie działała **aż** (niewidoczny) duszek dotknie krawędzi sceny.

```blocks3
    przyłóż pisak
+ powtarzaj aż <dotyka [krawędź v] ?> 
        przesuń o (50) kroków
        obróć w prawo o (15) stopni
    koniec
```

--- /task ---

--- task --- Zmień liczbę kroków w bloku `przesuń o`{:class="block3motion"} na `5` i sprawdź, czy twój program wygląda jak ten poniżej, zanim go przetestujesz:

```blocks3
    kiedy kliknięto zieloną flagę
    podnieś pisak
    ukryj
    wyczyść wszystko
    idź do x: (0) y: (0)
    ustaw kolor pisaka na [#4a6cd4]
    przyłóż pisak
    powtarzaj aż <dotyka [krawędź v] ?> 
        przesuń o (50) kroków
        obróć w prawo o (15) stopni
    koniec
```

--- /task ---

Jeśli uruchomisz kod teraz to zobaczysz, że rysunek wykonany za pomocą pióra pozostaje na scenie.

Nie tylko to, ale twój program stał się również programem do rysowania kół! Dzieje się tak dlatego, że te 15-stopniowe obroty ostatecznie sumują się do 360 stopni, a więc twoje pióro zatacza pełen okrąg. Zmienisz nieco sposób, w jaki się porusza tak, aby za każdym razem krok był nieco dłuższy, na tyle, że wymknie się spod kontroli. W tym celu będziesz potrzebował **zmiennej**.

Zmienne są oznaczonymi miejscami do przechowywania numerów lub innych informacji, na których Ci zależy. Możesz je utworzyć w sekcji bloków **Zmienne**.

--- task --- Utwórz zmienną o nazwie `kroki`{:class="block3variables"}, a następnie dodaj blok `ustaw kroki na 0`{:class="block3variables"} na początku programu.

```blocks3
    kiedy kliknięto zieloną flagę
+ ustaw [kroki v] na [0]
    podnieś pisak
```

--- /task ---

--- task --- Następnie użyj wartości `kroki`{:class="block3variables"} zamiast `5` w bloku `przesuń o`{:class="block3motion"} i dodaj `zmień kroki o 1`{:class="block3variables"} jako część pętli:

```blocks3
    przyłóż pisak
    powtarzaj aż <dotyka [krawędź v] ?> 
+       przesuń o (kroki) kroków
        obróć w prawo o (76) stopni
+           zmień [kroki v] o (1)
    koniec
```

--- /task ---

Czy uważasz, że to ma znaczenie, gdzie w pętli umieścisz blok `zmień kroki o 1`{:class="block3variables"}?

--- collapse ---
---
title: Ustawianie kodu we właściwej kolejności
---

Kiedy decydujesz, w jakiej kolejności umieścić bloki, pomyśl o tym, co robi każdy blok i co chcesz, żeby Twój program robił.

W tym przypadku chcesz, aby pióro się poruszało, a następnie obracało w kółko. Za każdym razem, gdy to robi, chcesz przejść o jeden dodatkowy krok.

Zatem sensowne jest umieszczenie bloku `zmień kroki o 1`{:class="block3variables"} **po** bloku `przesuń o`{:class="block3motion"}. Jednak po przesunięciu tak naprawdę nie ma znaczenia, czy pióro obróci się najpierw, a następnie zmieni się liczba kroków, czy najpierw liczba kroków zmieni się, a następnie pióro obróci się.

--- /collapse ---

--- task --- Teraz uruchom program, a także spróbuj zmienić liczbę stopni (spróbuj `76` i `120`)! --- /task ---