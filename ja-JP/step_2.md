## ペンツールを使用する

これから作るプロジェクトは、 **ペン** ツールを使います。このツールは、スプライトの中心点が移動 (いどう) した跡 (あと) を線として表示 (ひょうじ) するものです。 このプロジェクトで、その使いかたをおぼえましょう！

--- task ---

新しい Scratch ファイルを開き、ネコのスプライトをえらびます。 そして次の通りになるよう、ブロックメニューからスプライトパネルにブロックをドラッグします。

```blocks3
    when green flag clicked
    go to x: (0) y: (0)
    move (50) steps
    turn cw (15) degrees
```

--- /task ---

さあ、ペンをテストしてみましょう！

Scratch でペンブロックを使うには、 **ペン拡張機能** (かくちょうきのう) を追加 (ついか) する必要があります。

--- task ---

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

--- /task ---

--- task ---

緑の旗 (はた) を数回クリックして、何が起きるかを見てみましょう。

--- /task ---

ネコのスプライトの後ろに線が出ていたら、ペンがちゃんと動いています。そしてペンを使ってとてもカッコいいもようをかくことができます。

まず、スプライトをけしましょう。 ペンでかくのにジャマだからです。

--- task ---

**見た目**セクションの`隠す`{:class="block3looks"} (かくす) ブロックをプログラムの最初 (さいしょ) に追加するとスプライトがきえます。

```blocks3
    when green flag clicked
+    hide
    pen down
```

--- /task ---

さて、**ペン**セクションのべつのブロックでペンの色をかえることができます。 でも、そのブロックは他の見たことのあるブロックとは少しちがいます。 それは`ペンの色を(色)にする`{:class="block3extensions"}ブロックで、次のようなブロックです。

```blocks3
    set pen color to [#4a6cd4]
```

--- task ---

`ペンの色を(色)にする`{:class="block3extensions"}ブロックをスプライトパネルにドラッグし、`ペンを下ろす`{:class="block3extensions"}ブロックの上に入れます。

```blocks3
    when green flag clicked
    hide
+    set pen color to [#4a6cd4]
    pen down
```

次に、色のついたボックス (上のコードの青い部分) をクリックして、色をえらびます。

--- /task ---

緑の旗をクリックしてコードをテストしていると、ペンでかいた絵がきえないことに気付いたと思います。

--- task ---

**ペン**セクションから`全部消す`{:class="block3extensions"} (けす) ブロックをコードの始めに追加して、かいた線がきえるようにします。

```blocks3
    when green flag clicked
+    clear
    hide
```

--- /task ---