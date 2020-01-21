## استخدام أداة القلم

يعتمد المشروع الذي ستقوم بصنعه على أداة **Pen** التي ترسم خطًا خلف مركز العفريت أثناء تحركها. سوف تتعلم كيفية استخدامها الآن!

\--- task \---

Open a new Scratch file, select the Scratch Cat sprite, and drag in a few blocks you may have already seen, until it looks like this:

```blocks3
    عندما ينقر العلم الأخضر
    الذهاب إلى x: (0) y: (0)
    تحرك (50) خطوة
    استدر باتجاه عقارب الساعة (15) درجة
```

\--- /task \---

Now, time to test out the pen!

To use the Pen blocks in Scratch, you need add the **Pen extension**.

\--- task \---

Click on the **Add extension** button in the bottom left-hand corner.

![add extension button highlighted](images/add-extension-annotated.png)

Click on the **Pen** extension to add it.

![pen extension highlighted](images/click-pen-annotated.png)

The Pen section then appears at the bottom of the blocks menu.

![pen extension blocks](images/pen-extension-blocks.png)

From the **Pen** section, select the `pen down`{:class="block3extensions"} block and add it to the start of your program, like this:

```blocks3
    عند نقر العلم الأخضر
+ أنزل القلم
    اذهب إلى إلى س: (0) ص: (0)
```

\--- /task \---

\--- task \---

Now click the green flag a few times and watch what happens.

\--- /task \---

If you can see the lines behind the cat sprite, then the pen is working and you can start making it draw really cool patterns.

First, you should get rid of the sprite. It’s getting in the way of the drawing!

\--- task \---

Add a `hide`{:class="block3looks"} block from **Looks** to the start of the program and it’ll disappear.

```blocks3
    عند نقر العلم الأخضر
+ إخف
    انزل القلم
```

\--- /task \---

Now, you can change the colour of the pen with another block from the **Pen** section, but the block is a little different to the others you’ve seen. It’s the `set pen color to`{:class="block3extensions"} block and looks like this:

```blocks3
    اجعل لون القلم مساويا [#4a6cd4]
```

\--- task \---

Drag a `set pen color to`{:class="block3extensions"} block into your sprite panel, and snap it in above the `pen down`{:class="block3extensions"} block.

```blocks3
    عندما ينقر العلم الأخضر
    اخفاء
+ تحديد لون القلم إلى [# 4a6cd4]
    القلم إلى أسفل
```

Now, click on the box of colour (in the code above it’s the blue one), and choose a colour.

\--- /task \---

If you’ve been clicking on the green flag to test your code, you’ll have noticed that the drawings the pen makes don’t go away.

\--- task \---

Add a `clear`{:class="block3extensions"} block from the **Pen** section to the start of your code to take care of that:

```blocks3
    عند نقر العلم الأخضر
+ امسح الكل
    إخف
```

\--- /task \---