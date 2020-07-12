## ペンツールを使用する

これから作るプロジェクトは、 **ペン** ツールを使います。このツールは、スプライトの中心点が移動 (いどう) した跡 (あと) を線として表示 (ひょうじ) するものです。 このプロジェクトで、その使いかたをおぼえましょう！

\--- task \---

新しい Scratch ファイルを開き、ネコのスプライトをえらびます。 そして次の通りになるよう、ブロックメニューからスプライトパネルにブロックをドラッグします。

```blocks3
    緑色の旗が押されたとき
    x座標を (0) 、y座標を (0) にする
    (50) 歩動かす
    cw (15) 度回す
```

\--- /task \---

さあ、ペンをテストしてみましょう！

Scratch でペンブロックを使うには、 **ペン拡張機能** (かくちょうきのう) を追加 (ついか) する必要があります。

\--- task \---

左下すみにある[ **拡張機能を追加**] ボタンをクリックします。

![強調表示された「拡張機能を追加」ボタン](images/add-extension-annotated.png)

**ペン** 拡張機能をクリックして追加します。

![強調表示されたペン拡張機能](images/click-pen-annotated.png)

ペンセクションがブロックメニューの下の方に追加されます。

![ペン拡張機能ブロック](images/pen-extension-blocks.png)

**ペン**セクションから、`ペンを下ろす`{:class="block3extensions"}ブロックをえらび、次のようにプログラムの先頭に追加します。

```blocks3
    when green flag clicked
+    pen down
    go to x: (0) y: (0)
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
    when green flag clicked
+    hide
    pen down
```

\--- /task \---

Now, you can change the colour of the pen with another block from the **Pen** section, but the block is a little different to the others you’ve seen. It’s the `set pen color to`{:class="block3extensions"} block and looks like this:

```blocks3
    set pen color to [#4a6cd4]
```

\--- task \---

Drag a `set pen color to`{:class="block3extensions"} block into your sprite panel, and snap it in above the `pen down`{:class="block3extensions"} block.

```blocks3
    when green flag clicked
    hide
+    set pen color to [#4a6cd4]
    pen down
```

Now, click on the box of colour (in the code above it’s the blue one), and choose a colour.

\--- /task \---

If you’ve been clicking on the green flag to test your code, you’ll have noticed that the drawings the pen makes don’t go away.

\--- task \---

Add a `clear`{:class="block3extensions"} block from the **Pen** section to the start of your code to take care of that:

```blocks3
    when green flag clicked
+    clear
    hide
```

\--- /task \---