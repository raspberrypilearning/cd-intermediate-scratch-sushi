## Rysowanie wzorów

Teraz masz program, który rysuje linię, ale tylko jedną linię. To trochę nudne! Możesz użyć pętli `zawsze`{:class="block3control"}, żeby rysować coś w kółko, ale wtedy otrzymasz rysunki, które wyjdą poza scenę!

Musisz więc użyć innego typu pętli o nazwie `powtarzaj aż`{:class="block3control"}, którą znajdziesz w sekcji **Kontrola**. Ten rodzaj pętli będzie robił coś w kółko, **aż** spełniony zostanie warunek Prawda/Fałsz.

\--- task \---

Take a `repeat until`{:class="block3control"} block from the **Control** section, and put the `move`{:class="block3motion"} and `turn`{:class="block3motion"} blocks inside it, like so:

```blocks3
+ powtarzaj aż <> 
        przesuń o (50) kroków
        obróć cw o (15) stopni
    koniec
```

\--- /task \---

\--- task \---

Now click the green flag to run the program a few times and see what happens. You’ll notice two things: the pen always starts by drawing a line towards the middle of the Stage, and it doesn’t stop at the edge.

\--- /task \---

## \--- collapse \---

## title: Dlaczego pióro tak się zachowuje?

The pen always starts drawing in the direction of the middle, because the first **Motion** block that runs after the `pen down`{:class="block3extensions"} block is `go to x: 0 y: 0`{:class="block3motion"}. So the pen will draw a line as it moves to the centre of the Stage.

The pen doesn't stop at the edge of the Stage, because you haven’t yet told the `repeat until`{:class="block3control"} loop what condition it’s checking. This means the condition can never be met, so the loop will run on and on. This means that right now, the loop is working like a `forever`{:class="block3control"} loop.

\--- /collapse \---

\--- task \---

Move the `go to x: 0 y: 0`{:class="block3motion"} block to before the `pen down`{:class="block3extensions"} block and add, from the **Pen** section, a `pen up`{:class="block3extensions"} block right at the start of your code.

\--- /task \---

Time to fix your `repeat until`{:class="block3control"} loop so that it stops when you want it to. You’re looking to figure out if the (invisible) sprite is touching the edge of the Stage, so you need a **Sensing** block — in this case, the `touching ?`{:class="block3sensing"} block.

\--- task \---

Add a `touching ?`{:class="block3sensing"} block into your `repeat until`{:class="block3control"} loop, and select `edge`{:class="block3sensing"} . Then the loop with run **until** the (invisible) sprite touches the edge of the Stage.

```blocks3
    przyłóż pisak
+ powtarzaj aż <touching [edge v] ?> 
        przesuń o (50) kroków
        obróć cw o (15) stopni
    koniec
```

\--- /task \---

\--- task \---

Change the number of steps in the `move`{:class="block3motion"} block to `5`, and check that your program matches this one before you test it:

```blocks3
    kiedy kliknięto zieloną flagę
    podnieś pisak
    ukryj
    wyczyść wszystko
    idź do x: (0) y: (0)
    ustaw kolor pisaka na [#4a6cd4]
    przyłóż pisak
    powtarzaj aż <touching [edge v] ?> 
        przesuń o (50) kroków
        obróć w prawo o (15) stopni
    koniec
```

\--- /task \---

If you run the code now, you’ll see that the drawing the pen makes stays on the Stage.

Not only that, but your program has turned into a circle-drawing program! What's happening here is that those 15-degree turns eventually add up to 360 degrees, and so your pen turns in a full circle. You're going to change the way it moves slightly to make it take slightly a longer step each time, so it spirals out. For this, you’re going to need a **variable**.

Variables are basically labeled places to store numbers or other information that you care about. You can create them in the **Variables** blocks section.

\--- task \---

Make a variable called `steps`{:class="block3variables"}, and then add a `set steps to 0`{:class="block3variables"} block at the start of your program.

```blocks3
    kiedy kliknięto zieloną flagę
+ ustaw [kroki v] na [0]
    podnieś pisak
```

\--- /task \---

\--- task \---

Then use the value of `steps`{:class="block3variables"} instead of the `5` in the `move`{:class="block3motion"} block, and add `change steps by 1`{:class="block3variables"} as part of your loop:

```blocks3
    przyłóż pisak
    powtarzaj aż <touching [edge v] ?> 
+ przesuń o (kroki) kroki
        obróć cw o (76) stopni
+ zmień [kroki v] o (1)
    koniec
```

\--- /task \---

Do you think it matters where in the loop you put the `change steps by 1`{:class="block3variables"} block?

## \--- collapse \---

## title: Ustawianie kodu we właściwej kolejności

When you're deciding which order to put blocks in, think about what each block does and what you want your code to do.

In this case, you want the pen to move, then turn, over and over. Each time it does this, you want to move one extra step.

So it makes sense to put the `change steps by 1`{:class="block3variables"} block **after** the `move`{:class="block3motion"} block. However, after moving, it doesn't really matter if the pen turns first and then the number of steps changes, or if the number of steps changes first and then the pen turns instead.

\--- /collapse \---

\--- task \---

Now run the program, and also try changing the number of degrees around (try `76` and `120`)!

\--- /task \---