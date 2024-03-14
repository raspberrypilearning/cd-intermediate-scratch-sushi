## Ciekawsze linie

Czas dodać kolor! W tej chwili twoja linia ma jeden kolor, ale sekcja **Pióro** posiada bloki, które mogą zmienić jej kolor. A dzięki odpowiedniemu blokowi **Wyrażenie** możesz nawet losowo zmieniać kolor!

Blok do zmiany koloru **Pióra** to `zmień kolor pisaka o`{:class="block3extensions"}:

```blocks3
    zmień kolor pisaka o (10)
```

--- task --- Chwyć jeden z tych bloków i umieść go w pętli `powtarzaj aż`{:class="block3control"}, tak jak pokazano poniżej:

```blocks3
    powtarzaj aż <dotyka [krawędź v] ?> 
+ zmień kolor pisaka o (10)
        przesuń o (kroki) kroków
        obróć w prawo o (stopnie :: variables) stopni
        zmień [kroki v] o (powiększenie ::variables)
    koniec
```

--- /task ---

To jest fajne, ale trochę przewidywalne. Możesz sprawić, że będzie zabawniej, jeśli dodasz do kodu losową liczbę tak, że kolor zmieni się losowo.

--- task ---

Wstaw blok **Wyrażenie** wybrane przez ciebie losowe numery do bloku `zmień kolor pisaka o`{:class="block3extensions"} i wybierz jakieś wartości. Na początek możesz spróbować `1` i `100`.

```blocks3
    powtarzaj aż <dotyka [krawędź v] ?> 
+        Zmień kolor pisaka o (losuj liczbę od (1) do (100))
        przesuń o (kroki) kroków
        obróć w prawo o (stopnie :: variables) stopni
        zmień [kroki v] o (powiększenie ::variables)
    koniec
```

--- /task ---

--- task --- Spróbuj uruchomić ponownie i obserwuj losową tęczę! --- /task ---