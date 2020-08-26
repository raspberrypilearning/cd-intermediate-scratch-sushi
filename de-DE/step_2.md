## Das Stiftwerkzeug verwenden

Das Projekt, das Du erstellen wirst, basiert auf dem **Malstift**-Werkzeug, das eine Linie hinter der Mitte einer Figur zieht, während sie sich bewegt. Du wirst jetzt lernen, es zu benutzen!

\--- task \---

Open a new Scratch project.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** open a new project in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Select the Scratch Cat sprite, and drag in a few blocks you may have already seen, until it looks like this:

```blocks3
    Wenn die grüne Flagge angeklickt
gehe zu x: (0) y: (0)
gehe (50) er Schritt
drehe dich nach rechts um (15) Grad
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
    Wenn die grüne Flagge angeklickt
+ schalte Stift ein
gehe zu x: (0) y: (0)
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
    Wenn die grüne Flagge angeklickt
+ verstecke dich
schalte Stift ein
```

\--- /task \---

Now, you can change the colour of the pen with another block from the **Pen** section, but the block is a little different to the others you’ve seen. It’s the `set pen color to`{:class="block3extensions"} block and looks like this:

```blocks3
    setze Stiftfarbe auf [#4a6cd4]
```

\--- task \---

Drag a `set pen color to`{:class="block3extensions"} block into your sprite panel, and snap it in above the `pen down`{:class="block3extensions"} block.

```blocks3
    Wenn die grüne Flagge angeklickt
verstecke dich
+ setze Stiftfarbe auf [#4a6cd4]
schalte Stift ein
```

Now, click on the box of colour (in the code above it’s the blue one), and choose a colour.

\--- /task \---

If you’ve been clicking on the green flag to test your code, you’ll have noticed that the drawings the pen makes don’t go away.

\--- task \---

Add a `clear`{:class="block3extensions"} block from the **Pen** section to the start of your code to take care of that:

```blocks3
    Wenn die grüne Flagge angeklickt
+ lösche alles
verstecke dich
```

\--- /task \---