## मजे की लाइनें

रंग जोड़ने का समय! अभी, आपकी लाइन एक रंग है, लेकिन ** पेन ** ऐसे ब्लॉक हैं जो अपना रंग बदल सकते हैं। और दाईं ओर ** ऑपरेटर के साथ ** ब्लॉक, आप भी रंग अनियमित रूप से बदल सकते हैं!

** पेन बदलने के लिए ब्लॉक ** रंग ` द्वारा पेन रंग बदलें ` {:class= "block3extensions"}:

```blocks3
    change pen color by (10)
```

\--- task \---

उन ब्लॉकों में से एक को पकड़ो और इसे अपने ` में डालें जब तक दोहराएं ` {:class="block3control"} लूप, इस तरह:

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

यह अच्छा है, लेकिन थोड़ा सा पूर्वानुमान है। यदि आप इसमें एक यादृच्छिक संख्या जोड़ते हैं, तो आप इसे थोड़ा और मज़ेदार बना सकते हैं, इसलिए रंग अनियमित रूप से बदलता है।

\--- task \---

यादृच्छिक संख्या डालें ** ऑपरेटर ** ` द्वारा पेन कलर बदलें ` {:class ="block3extensions"} इसमें जाने के लिए कुछ मानों को ब्लॉक करें और चुनें। मैं कोशिश करूँगा ` 1 ` और ` 100 ` शुरू करना।

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

इसे फिर से चलाने की कोशिश करें, और यादृच्छिक इंद्रधनुष देखें!

\--- /task \---