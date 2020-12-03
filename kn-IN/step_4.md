## ಇನ್ಪುಟ್ ಕೇಳುತ್ತಿದೆ

ಸರಿ, ಇದು ತುಂಬಾ ಚೆನ್ನಾಗಿದೆ, ಆದರೆ ನೀವು ಬೇರೆ ನಮೂನೆಯನ್ನು ರಚಿಸಲು ಬಯಸಿದಾಗಲೆಲ್ಲಾ ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಬೇಕಾಗಿರುವುದು ಸ್ವಲ್ಪ ಬೇಸರ ತರಿಸಿದೆ. ಬಳಸುವ ಮೌಲ್ಯಗಳನ್ನು ಕೇಳುವ ಪ್ರೋಗ್ರಾಂ ಅನ್ನು ಪಡೆಯುವುದು ಒಳ್ಳೆಯದಲ್ಲವೇ? ನೀವು ಅದನ್ನು ಮಾಡಬಹುದು!

--- task ---

ಮೊದಲು, **Variables** ವಿಭಾಗಕ್ಕೆ ಹೋಗಿ ಮತ್ತು `degrees`{:class="block3variables"}ಎಂದು ಕರೆಯಲ್ಪಡುವ ವೇರಿಯಬಲ್ಸ್ ರಚಿಸಿ ಮತ್ತು ಹೆಚ್ಚಿಸಿ `increase`{:class="block3variables"}.

--- /task ---

--- task ---

ಈಗ ಈ ರೀತಿಯಾಗಿ ನಿಮ್ಮ ಕೋಡ್‌ಗೆ ಹೊಸ ವೇರಿಯಬಲ್ಸ್ಗಳನ್ನು ಸೇರಿಸಿ:

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

--- /task ---

ಈಗ ನೀವು ಈ ಎರಡು ವೇರಿಯಬಲ್ಸ್ಗಳಿಗೆ ಮೌಲ್ಯಗಳನ್ನು ಕೇಳಬೇಕು ಮತ್ತು ಅವುಗಳನ್ನು ಸಂಗ್ರಹಿಸಬೇಕು. ನೀವು ಇದನ್ನು `Ask and wait`{:class="block3sensing"} ಎಂದು ಕರೆಯಲ್ಪಡುವ **Sensing** ಬ್ಲಾಕ್ ಬಳಸಿ ಮಾಡುತ್ತೀರಿ, ಇದನ್ನು ನೀವು ಪ್ರಶ್ನೆಯಾಗಿ ಟೈಪ್ ಮಾಡಬಹುದು.

--- task ---

ನಿಮ್ಮ sprite ಪ್ಯಾನೆಲ್‌ಗೆ `Ask and wait`{:class="block3sensing"} ಬ್ಲಾಕ್ ಅನ್ನು ಎಳೆಯಿರಿ ಮತ್ತು ಪ್ರಶ್ನೆಯನ್ನು `How many steps should I grow by?`{:class="block3sensing"} ಗೆ ಬದಲಾಯಿಸಿ

ನೀವು `steps`{:class="block3variables"} `0` ಗೆ ಹೊಂದಿಸಿದ ನಂತರ ಅದನ್ನು ನಿಮ್ಮ ಪ್ರೋಗ್ರಾಂಗೆ ಸೇರಿಸಿ, ಹೀಗೆ:

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

--- /task ---

ಈಗ ನೀವು ನಿಮ್ಮ ಪ್ರೋಗ್ರಾಂ ಅನ್ನು ಪ್ರಶ್ನೆಯನ್ನು ಕೇಳಿದ್ದೀರಿ, ಉತ್ತರವನ್ನು ನೆನಪಿಟ್ಟುಕೊಳ್ಳಲು ನಿಮಗೆ ಇದು ಬೇಕು! Scratch `answer`{:class="block3sensing"} ಎಂಬ ವಿಶೇಷ ವೇರಿಯೇಬಲ್ ಅನ್ನು ಹೊಂದಿದೆ,ಅಲ್ಲಿ ಅದು ಸ್ವೀಕರಿಸಿದ ಇತ್ತೀಚಿನ ಉತ್ತರವನ್ನು ಸಂಗ್ರಹಿಸುತ್ತದೆ. **Sensing** ಬ್ಲಾಕ್ಗಳ ನಡುವೆ ನೀವು ಈ ವೇರಿಯೇಬಲ್ ಅನ್ನು ಕಾಣಬಹುದು.

--- task ---

**Variables** ನಿಂದ `set to`{:class="block3variables"} ಬ್ಲಾಕ್ ಅನ್ನು ಉಪಯೋಗಿಸಿ,ಅದರಿಂದ `answer`{:class="block3sensing"} ಮೌಲ್ಯವನ್ನು ತೆಗೆದುಕೊಂಡು ಅದರನ್ನು `increase`{:class="block3variables"} ವೇರಿಯಬಲ್ ಅಲ್ಲಿ ಈತರ ಇರಿಸಿ:

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

--- /task ---

--- task ---

ಈಗ, `degrees`{:class="block3variables"} ಗಳೊಂದಿಗೆ ಅದೇ ಕೆಲಸವನ್ನು ಮಾಡಿ, `How many degrees should I turn?`{:class="block3sensing"} ಎಂದು ಕೇಳುತ್ತಾ ಮತ್ತು `answer`{:class="block3sensing"} ಮೌಲ್ಯವನ್ನು `degrees`{:class="block3variables"} ಗಳಲ್ಲಿ ಸಂಗ್ರಹಿಸುತ್ತದೆ:

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

--- /task ---

--- task ---

ನಿಮ್ಮ ಪ್ರೋಗ್ರಾಂ ಈಗ ಕೆಳಗಿನಂತೆ ತೋರುತ್ತಿದೆ ಎಂದು ಪರಿಶೀಲಿಸಿ, ಮತ್ತು ಅದನ್ನು ವಿಭಿನ್ನ ಸಂಖ್ಯೆಗಳೊಂದಿಗೆ ಕೆಲವು ಬಾರಿ ಚಲಾಯಿಸಿ. ಚೆನ್ನಾಗಿರುವ ಚಿತ್ರಗಳನ್ನು ಮಾಡುವ ಉತ್ತರಗಳನ್ನು ಬರೆಯಿರಿ. ನಂತರದ ಹಂತದಲ್ಲಿ ನಿಮಗೆ ಅವುಗಳು ಬೇಕಾಗುತ್ತವೆ!

```blocks3
    when green flag clicked
    set [steps v] to [0]
    ask [How many steps should I grow by?] and wait
    set [increase v] to (answer)
    ask [How many degrees should I turn?] and wait
    set [degrees v] to (answer)
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

--- /task ---