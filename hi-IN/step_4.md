## इनपुट के लिए पूछ रहा है

ठीक है, यह बहुत अच्छा हो रहा है, लेकिन हर बार जब आप एक अलग पैटर्न बनाना चाहते हैं तो अपने कोड को संपादित करना थोड़ा उबाऊ है। मूल्यों का उपयोग करने के लिए आपसे पूछना कार्यक्रम प्राप्त करना अच्छा नहीं होगा? तुम यह कर सकते हो!

\--- task \---

सबसे पहले, ** चर पर जाएं ** अनुभाग और वैरिएबल बनाएं ` डिग्री ` {:class="block3variables"} और ` वृद्धि ` {:class= "block3variables"}।

\--- /task \---

\--- task \---

अब इस तरह अपने कोड में नए चर जोड़ें:

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

अब आपको इन दो चर के लिए मान पूछने और उन्हें संग्रहीत करने की आवश्यकता है। आप इसे ** सेंसिंग का उपयोग करके करते हैं ** ब्लॉक ` पूछें और प्रतीक्षा करें ` {":class="block3sensing"}, जिसे आप एक प्रश्न टाइप कर सकते हैं।

\--- task \---

` पूछें और प्रतीक्षा करें ` {:class= "block3sensing"} अपने स्प्राइट पैनल में ब्लॉक करें और इस प्रश्न को बदलें ` मुझे कितने चरणों में बढ़ना चाहिए? ` {:class="block3sensing"}

इसके बाद इसे अपने प्रोग्राम में जोड़ें, बस ` चरण सेट करने के बाद ` {:class = "block3variables"} से ` 0 तक `, इस तरह:

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

\--- /task \---

अब आपको अपना कार्यक्रम एक प्रश्न पूछ रहा है, आपको इसका उत्तर याद रखने की आवश्यकता है! यह पता चला है कि स्क्रैच का एक विशेष चर है जिसे ` उत्तर कहा जाता है ` {:class="block3sensing"}, जहां इसे प्राप्त हुए सबसे हालिया उत्तर को संग्रहीत करता है। आप इस वैरिएबल को ** सेंसिंग के बीच पा सकते हैं ** ब्लॉक।

\--- task \---

` सेट का उपयोग करना ` {:class="block3variables"} ब्लॉक से ** चर **, ` उत्तर का मान लें ` {:class="block3sensing"} और इसे ` वृद्धि में संग्रहीत करें ` {:class="block3variables"} चर जैसा:

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

\--- /task \---

\--- task \---

अब, ` डिग्री के साथ एक ही काम करें ` {:class="block3variables"}, पूछते हुए ` मुझे कितने डिग्री मुड़ना चाहिए? ` {:class="block3sensing"} और ` उत्तर का मान संग्रहीत करना ` {:class="block3sensing"} `डिग्री में ` {:class= "block3variables"}:

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

\--- /task \---

\--- task \---

अपने प्रोग्राम को अब नीचे दिए गए अक्षर की तरह देखें, और इसे अलग-अलग संख्याओं के साथ कुछ बार चलाएं। सबसे अच्छे चित्र बनाने वाले उत्तरों को लिखिए। आपको बाद के चरण में उनकी आवश्यकता होगी!

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

\--- /task \---