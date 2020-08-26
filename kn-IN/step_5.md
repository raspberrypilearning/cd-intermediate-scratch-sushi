## ಚೆನ್ನಾಗಿರುವ ರೇಖೆಗಳು

ಬಣ್ಣವನ್ನು ಸೇರಿಸುವ ಸಮಯ! ಇದೀಗ, ನಿಮ್ಮ ರೇಖೆ ಒಂದೇ ಬಣ್ಣ ಹೊಂದಿದೆ. ಆದರೆ **Pen** ಅದರ ಬಣ್ಣವನ್ನು ಬದಲಾಯಿಸಬಲ್ಲ ಬ್ಲಾಕ್ಗಳನ್ನು ಹೊಂದಿದೆ. ಮತ್ತು ಸರಿಯಾದ **Operator** ಬ್ಲಾಕ್ ಒಂದಿಗೆ, ನೀವು ಬಣ್ಣವನ್ನು ಯಾದೃಚ್ಕವಾಗಿ ಬದಲಾಯಿಸಬಹುದು!

**Pen** ಬಣ್ಣವನ್ನು ಬದಲಾಯಿಸುವ ಬ್ಲಾಕ್ `change pen color by`{:class="block3extensions"}:

```blocks3
    change pen color by (10)
```

\--- task \---

ಆ ಬ್ಲಾಕ್‌ಗಳಲ್ಲಿ ಒಂದನ್ನು ಪಡೆದುಕೊಳ್ಳಿ ಮತ್ತು ಅದನ್ನು ನಿಮ್ಮ `repeat until`{:class="block3control"} ಲೂಪ್, ಈ ರೀತಿಯಾಗಿ:

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

ಅದು ಚೆನ್ನಾಗಿದೆ, ಆದರೆ ಇದೆಲ್ಲ ಸುಲಭದಲ್ಲಿ ಊಹಿಸಬಹುದಾಗಿದೆ. ನೀವು ಯಾದೃಚ್ ಸಂಖ್ಯೆಯನ್ನು ಸೇರಿಸಿದರೆ ನೀವು ಅದನ್ನು ಸ್ವಲ್ಪ ಹೆಚ್ಚು ಮೋಜು ಮಾಡಬಹುದು, ಆದ್ದರಿಂದ ಬಣ್ಣವು ಯಾದೃಚ್ಕವಾಗಿ ಬದಲಾಗುತ್ತದೆ.

\--- task \---

ಯಾದೃಚ್ಕ ಸಂಖ್ಯೆಯನ್ನು ಇರಿಸಿ **Operator** ಅನ್ನು `change pen color by`{:class="block3extensions"} ಬ್ಲಾಕ್‌ ಒಳಗೆ ಇರಿಸಿ, ಅದರಲ್ಲಿ ಹೋಗಲು ಕೆಲವು ಮೌಲ್ಯಗಳನ್ನು ಆರಿಸಿ. ನಾನು ಶುರು ಮಾಡಲು ` 1` ಮತ್ತು ` 100 `ಅನ್ನು ಪ್ರಯತ್ನಿಸುತ್ತೇನೆ.

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (pick random (1) to (100))
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

\--- task \---

ಅದನ್ನು ಮತ್ತೆ ಚಲಾಯಿಸಲು ಪ್ರಯತ್ನಿಸಿ, ಮತ್ತು ಯಾದೃಚ್ಕ ಮಳೆಬಿಲ್ಲು ನೋಡಿ!

\--- /task \---