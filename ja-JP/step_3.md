## もようをかく

これで線を引くプログラムができましたが、1本の線しか引けません。 これではちょっとつまらないですね。 `ずっと`{:class="block3control"}ループを使えば何度もかきつづけることができますが、そのうちステージからはみ出してしまうでしょう。

そこで、`まで繰り返す`{:class="block3control"} (くりかえす) というべつのループを使う必要があります。これは **制御** (せいぎょ) セクションにあります。 このタイプのループは、 真／偽 (ぎ) の条件 (じょうけん) がみたされる**まで**、何度も繰り返し実行します。

\--- task \---

`まで繰り返す`{:class="block3control"}ブロックを**制御**セクションから取り出し、`(10)歩動かす`{:class="block3motion"}ブロックと`(15)度回す`{:class="block3motion"}ブロックをその中に入れ、次のようにします。

```blocks3
+ <> まで繰り返す
        (50) 歩動かす
        cw (15) 度回す
    end
```

\--- /task \---

\--- task \---

緑の旗をクリックしてプログラムを数回実行し、何が起こるかを見ましょう。 2つのことに気づくと思います。ペンはいつもステージの中央に向かって線を引き始めること、そしてペンがステージのはしで止まらないことです。

\--- /task \---

## \--- collapse \---

## title: どうしてペンはこのような動きをするのですか？

ペンはいつも中央に向かってかき始めます。 なぜなら、`ペンを下ろす`{:class="block3extensions"}ブロックの後に最初 (さいしょ) に実行される **動き**ブロックは`x座標 (ざひょう) を0、 y座標を0にする`{:class="block3motion"}ブロックだからです。 したがって、ペンはステージの中央に移動しながら線を引くようになります。

The pen doesn't stop at the edge of the Stage, because you haven’t yet told the `repeat until`{:class="block3control"} loop what condition it’s checking. This means the condition can never be met, so the loop will run on and on. This means that right now, the loop is working like a `forever`{:class="block3control"} loop.

\--- /collapse \---

\--- task \---

Move the `go to x: 0 y: 0`{:class="block3motion"} block to before the `pen down`{:class="block3extensions"} block and add, from the **Pen** section, a `pen up`{:class="block3extensions"} block right at the start of your code.

\--- /task \---

Time to fix your `repeat until`{:class="block3control"} loop so that it stops when you want it to. You’re looking to figure out if the (invisible) sprite is touching the edge of the Stage, so you need a **Sensing** block — in this case, the `touching ?`{:class="block3sensing"} block.

\--- task \---

Add a `touching ?`{:class="block3sensing"} block into your `repeat until`{:class="block3control"} loop, and select `edge`{:class="block3sensing"} . Then the loop with run **until** the (invisible) sprite touches the edge of the Stage.

```blocks3
    pen down
+    repeat until <touching [edge v] ?> 
        move (50) steps
        turn cw (15) degrees
    end
```

\--- /task \---

\--- task \---

Change the number of steps in the `move`{:class="block3motion"} block to `5`, and check that your program matches this one before you test it:

```blocks3
    when green flag clicked
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (5) steps
        turn cw (15) degrees
    end
```

\--- /task \---

If you run the code now, you’ll see that the drawing the pen makes stays on the Stage.

Not only that, but your program has turned into a circle-drawing program! What's happening here is that those 15-degree turns eventually add up to 360 degrees, and so your pen turns in a full circle. You're going to change the way it moves slightly to make it take slightly a longer step each time, so it spirals out. For this, you’re going to need a **variable**.

Variables are basically labeled places to store numbers or other information that you care about. You can create them in the **Variables** blocks section.

\--- task \---

Make a variable called `steps`{:class="block3variables"}, and then add a `set steps to 0`{:class="block3variables"} block at the start of your program.

```blocks3
    when green flag clicked
+   set [steps v] to [0]
    pen up
```

\--- /task \---

\--- task \---

Then use the value of `steps`{:class="block3variables"} instead of the `5` in the `move`{:class="block3motion"} block, and add `change steps by 1`{:class="block3variables"} as part of your loop:

```blocks3
    pen down
    repeat until <touching [edge v] ?> 
+       move (steps) steps
        turn cw (76) degrees
+        change [steps v] by (1)
    end
```

\--- /task \---

Do you think it matters where in the loop you put the `change steps by 1`{:class="block3variables"} block?

## \--- collapse \---

## title: Putting code in the right order

When you're deciding which order to put blocks in, think about what each block does and what you want your code to do.

In this case, you want the pen to move, then turn, over and over. Each time it does this, you want to move one extra step.

So it makes sense to put the `change steps by 1`{:class="block3variables"} block **after** the `move`{:class="block3motion"} block. However, after moving, it doesn't really matter if the pen turns first and then the number of steps changes, or if the number of steps changes first and then the pen turns instead.

\--- /collapse \---

\--- task \---

Now run the program, and also try changing the number of degrees around (try `76` and `120`)!

\--- /task \---