## छान ओळी

रंग भरण्याची वेळ आली! आत्ता, आपली ओळ एका रंगाची आहे, परंतु **Pen** विभागात असे ब्लॉक्स आहेत जे रंग बदलू शकतात. आणि बरोबर **Operator** ब्लॉक निवडून, आपण सहजगत्या रंग बदलू शकता!

**Pen** चा रंग बदलण्यासाठी `change pen color by`{:class="block3extensions"} ब्लॉकचा वापर करा:

```blocks3
    change pen color by (10)
```

\--- task \---

त्यापैकी एक ब्लॉक निवडा आणि तो आपल्या `repeat until`{:class="block3control"} लूप मध्ये ह्या प्रकारे जोडा:

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

ते छान दिसते, परंतु अंदाज लावता येईल असे आहे. आपण त्यात एखादी वेगळी (रँडम) संख्या जोडल्यास आपण त्यास थोडे अधिक मजेदार बनवू शकता, जेणेकरून रंग कधीही बदलू शकेल.

\--- task \---

हा रँडम संख्येचा **Operator** ब्लॉक `change pen color by`{:class="block3extensions"} मध्ये घाला आणि मूल्ये निवडा. मी `1` आणि `100` निवडून सुरुवात केली असती.

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

हे पुन्हा चालवण्याचा प्रयत्न करा आणि आगळे वेगळे इंद्रधनुष्य पहा!

\--- /task \---