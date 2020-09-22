## इनपुट मागत आहे

ठीक आहे, हे सगळं उत्तम आहे, परंतु प्रत्येक वेळी जेव्हा आपल्याला वेगळा नमुना काढायचा असेल तेव्हा आपल्या कोडमध्ये बदल करणे थोडे कंटाळवाणे आहे. ह्या ऐवजी प्रोग्रॅमनेच आपल्याला व्हॅल्यूज मागितल्या तर किती बरे नाही का? तुम्ही ते करू शकता!

--- task ---

प्रथम, **Variables** विभागात जाऊन `degrees`{:class="block3variables"} आणि `increase`{:class="block3variables"} व्हेरिएबल्स तयार करा.

--- /task ---

--- task ---

आता आपल्या कोडमध्ये हे नवीन व्हेरिएबल्स असे जोडा:

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

--- /task ---

आता आपल्याला या दोन व्हेरिएबल्ससाठी मूल्ये विचारण्याची आणि ती साठवण्याची आवश्यकता आहे. आपण `Ask and wait`{:class="block3sensing"} नावाचा **Sensing** ब्लॉक वापरून हे करणार आहोत, ज्यामध्ये आपण प्रश्न टाइप करू शकतो.

--- task ---

`Ask and wait`{:class="block3sensing"} नावाचा ब्लॉक आपल्या स्प्राइट पॅनेलमध्ये खेचून प्रश्न बदलून `How many steps should I grow by?`{:class="block3sensing"} करा

जिथे `steps`{:class="block3variables"} `0` सेट केलेले आहेत, त्यानंतर आपल्या प्रोग्राममध्ये हे पुढील प्रमाणे जोडा:

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

--- /task ---

आता आपला प्रश्न विचारणारा प्रोग्राम तयार झाला आहे, पण ह्या प्रश्नांची उत्तरे देखील त्याने लक्षात ठेवण्याची आवश्यकता आहे! Scratch कडे `answer`{:class="block3sensing"} नावाचा विशेष व्हेरिएबल आहे, जिथे प्राप्त झालेली सर्वात नवीन उत्तरे संग्रहित होतात. हे व्हेरिएबल आपल्याला **Sensing** ब्लॉक्स मध्ये सापडेल.

--- task ---

**Variables** मधील `set to`{:class="block3variables"} ब्लॉक वापरुन, `answer`{:class="block3sensing"} मधील व्हॅल्यूए घ्या आणि ते `increase`{:class="block3variables"} व्हेरिएबल मध्ये पुढील प्रमाणे साठवून ठेवा:

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

--- /task ---

--- task ---

आता, हेच `degrees`{:class="block3variables"} सोबत करा, जेणे करून `How many degrees should I turn?`{:class="block3sensing"} ह्या प्रश्नाचे उत्तर `answer`{:class="block3sensing"} ह्या ठिकाणी `degrees`{:class="block3variables"} मध्ये जतन करावे:

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

--- /task ---

--- task ---

आपला प्रोग्राम आता खालील प्रमाणे दिसत आहे का हे तपासा आणि काही वेळा वेगवेगळ्या संख्येसह चालवून पहा. अशी उत्तरे लिहा जेणे करून छान चित्रे बनतील. नंतरच्या चरणात आपल्याला त्यांची आवश्यकता असेल!

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