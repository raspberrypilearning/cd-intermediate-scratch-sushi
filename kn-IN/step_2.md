## ಪೆನ್ ಉಪಕರಣವನ್ನು ಬಳಸುವುದು

ನೀವು ಮಾಡಲು ಹೊರಟಿರುವ ಪ್ರಾಜೆಕ್ಟ್ ** ಪೆನ್** ಅನ್ನು (Pen tool) ಅವಲಂಬಿಸಿರುವ ಉಪಕರಣ, ಅದು ಚಲಿಸುವಾಗ ಸ್ಪ್ರೈಟ್‌ನ ಮಧ್ಯದಿಂದ ಒಂದು ರೇಖೆಯನ್ನು ಸೆಳೆಯುತ್ತದೆ. ನೀವು ಈಗ ಅದನ್ನು ಬಳಸಲು ಕಲಿಯಲಿದ್ದೀರಿ!

\--- task \---

ಹೊಸ ಸ್ಕ್ರ್ಯಾಚ್ ಯೋಜನೆಯನ್ನು ತೆರೆಯಿರಿ.

**ಆನ್‌ಲೈನ್:** ಹೊಸ ಆನ್‌ಲೈನ್ ತೆರೆಯಿರಿ Scratch ನಲ್ಲಿ ಯೋಜನೆ [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

** ಆಫ್‌ಲೈನ್: ** ಆಫ್‌ಲೈನ್ ಸಂಪಾದಕದಲ್ಲಿ ಹೊಸ ಯೋಜನೆಯನ್ನು ತೆರೆಯಿರಿ.

ನೀವು ಸ್ಕ್ರ್ಯಾಚ್ ಆಫ್‌ಲೈನ್ ಸಂಪಾದಕವನ್ನು ಡೌನ್‌ಲೋಡ್ ಮಾಡಿ ಸ್ಥಾಪಿಸಬೇಕಾದರೆ, ನೀವು ಅದನ್ನು [ rpf.io/scratchoff ನಲ್ಲಿ ಕಾಣಬಹುದು ](http://rpf.io/scratchoff) {:target="_blank"}.

\--- /task \---

\--- task \---

Select the Scratch Cat sprite, and drag in a few blocks you may have already seen, until it looks like this:

```blocks3
    when green flag clicked
    go to x: (0) y: (0)
    move (50) steps
    turn cw (15) degrees
```

\--- /task \---

ಈಗ, ಪೆನ್ನು ಪರೀಕ್ಷಿಸುವ ಸಮಯ!

Scratch‌ನಲ್ಲಿ ಪೆನ್ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಬಳಸಲು, ನೀವು **Pen extension** ಸೇರಿಸಬೇಕು.

\--- task \---

ಕ್ಲಿಕ್ ಮಾಡಿ **Add extension** ಬಟನ್ ಕೆಳಗಿನ ಎಡಗೈ ಮೂಲೆಯಲ್ಲಿ.

![ಹೈಲೈಟ್ ಮಾಡಿದ add extension (ಆಡ್ ಎಕ್ಸಟೆನ್ಶನ್) ಬಟನ್ ಸೇರಿಸಿ](images/add-extension-annotated.png)

ಕ್ಲಿಕ್ ಮಾಡಿ **Pen** ವಿಸ್ತರಣೆ ಅದನ್ನು ಸೇರಿಸಲು.

![ಪೆನ್ ವಿಸ್ತರಣೆಯನ್ನು ಹೈಲೈಟ್ ಮಾಡಲಾಗಿದೆ](images/click-pen-annotated.png)

ಪೆನ್ ವಿಭಾಗವು ಬ್ಲಾಕ್ಗಳ ಮೆನುವಿನ ಕೆಳಭಾಗದಲ್ಲಿ ಕಾಣಿಸಿಕೊಳ್ಳುತ್ತದೆ.

![ಪೆನ್ ವಿಸ್ತರಣೆ blocks](images/pen-extension-blocks.png)

**Pen** ವಿಭಾಗದಿಂದ, `pen down`{:class="block3extensions"} ಬ್ಲಾಕ್ ಮತ್ತು ಅದನ್ನು ನಿಮ್ಮ ಪ್ರೋಗ್ರಾಮ್ ನ ಪ್ರಾರಂಭಕ್ಕೆ ಸೇರಿಸಿ, ಈ ರೀತಿಯಾಗಿ:

```blocks3
    when green flag clicked
+    pen down
    go to x: (0) y: (0)
```

\--- /task \---

\--- task \---

ಈಗ ಹಸಿರು ಧ್ವಜವನ್ನು ಕೆಲವು ಬಾರಿ ಕ್ಲಿಕ್ ಮಾಡಿ ಮತ್ತು ಏನಾಗುತ್ತದೆ ಎಂಬುದನ್ನು ನೋಡಿ.

\--- /task \---

ಬೆಕ್ಕಿನ sprite ಹಿಂದಿನ ರೇಖೆಗಳನ್ನು ನೀವು ನೋಡಬಹುದಾದರೆ, ಪೆನ್ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತಿದೆ ಮತ್ತು ನೀವು ಅದನ್ನು ನಿಜವಾಗಿಯೂ ಚೆನ್ನಾಗಿರುವ ಮಾದರಿಗಳನ್ನು ಸೆಳೆಯಲು ಪ್ರಾರಂಭಿಸಬಹುದು.

ಮೊದಲಿಗೆ, ನೀವು sprite ಅನ್ನು ತಡೆದುಹಾಕಬೇಕು. ಇದು ರೇಖಾಚಿತ್ರದ ಅಡ್ಡಿಯಲ್ಲಿದೆ!

\--- task \---

`hide`{:class="block3looks"}ಬ್ಲಾಕ್ ನಿಂದ **Looks** ಪ್ರೋಗ್ರಾಮ್ ನ ಪ್ರಾರಂಭಕ್ಕೆ ಸೇರಿಸಿ, ಕಣ್ಮರೆಯಾಗುತ್ತದೆ.

```blocks3
    when green flag clicked
+    hide
    pen down
```

\--- /task \---

ಈಗ, ನೀವು ಪೆನ್ನ ಬಣ್ಣವನ್ನು **Pen** ವಿಭಾಗದಿಂದ ಮತ್ತೊಂದು ಬ್ಲಾಕ್ನೊಂದಿಗೆ ಬದಲಾಯಿಸಬಹುದು, ಆದರೆ ನೀವು ನೋಡಿದ ಇತರರಿಗೆ ಬ್ಲಾಕ್ ಸ್ವಲ್ಪ ಭಿನ್ನವಾಗಿರುತ್ತದೆ. ಇದು `set pen color to`{:class="block3extensions"} block ಮತ್ತು ಈ ರೀತಿ ಕಾಣುತ್ತದೆ:

```blocks3
    set pen color to [#4a6cd4]
```

\--- task \---

`set pen color to`{:class="block3extensions"} ಬ್ಲಾಕ್ ಅನ್ನು ಎಳೆಯಿರಿ ನಿಮ್ಮ sprite ಪ್ಯಾನೆಲ್‌ಗೆ, ಮತ್ತು ಅದನ್ನು `pen down`{:class="block3extensions"} ಬ್ಲಾಕ್ ಮೇಲೆ ಅಂಟಿಸಿ.

```blocks3
    when green flag clicked
    hide
+    set pen color to [#4a6cd4]
    pen down
```

ಈಗ, ಬಣ್ಣದ ಪೆಟ್ಟಿಗೆಯ ಮೇಲೆ ಕ್ಲಿಕ್ ಮಾಡಿ (ಮೇಲಿನ code‌ ನಲ್ಲಿ ಅದು ನೀಲಿ ಬಣ್ಣದ್ದಾಗಿದೆ), ಮತ್ತು ಬಣ್ಣವನ್ನು ಆರಿಸಿ.

\--- /task \---

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಪರೀಕ್ಷಿಸಲು ನೀವು ಹಸಿರು ಧ್ವಜದ ಮೇಲೆ ಕ್ಲಿಕ್ ಮಾಡುತ್ತಿದ್ದರೆ, ಪೆನ್ ಮಾಡುವ ರೇಖಾಚಿತ್ರಗಳು ಹೋಗುವುದಿಲ್ಲ ಎಂದು ನೀವು ಗಮನಿಸಿದ್ದೀರಿ.

\--- task \---

ನಿಮ್ಮ code ಅನ್ನು ಪ್ರಾರಂಭದಿಂದ ನೋಡಿಕೊಳ್ಳಲು `clear`{:class="block3extensions"} ಬ್ಲಾಕ್ ಅನ್ನು **Pen** ವಿಭಾಗದಿಂದ ಸೇರಿಸಿ:

```blocks3
    when green flag clicked
+    clear
    hide
```

\--- /task \---