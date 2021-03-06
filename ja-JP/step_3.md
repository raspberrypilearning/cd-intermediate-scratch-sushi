## もようをかく

これで線を引くプログラムができましたが、1本の線しか引けません。 これではちょっとつまらないですね。 `ずっと`{:class="block3control"}ループを使えば何度もかきつづけることができますが、そのうちステージからはみ出してしまうでしょう。

そこで、`まで繰り返す`{:class="block3control"} (くりかえす) というべつのループを使う必要があります。これは **制御** (せいぎょ) セクションにあります。 このタイプのループは、 真／偽 (ぎ) の条件 (じょうけん) がみたされる**まで**、何度も繰り返し実行します。

--- task ---

`まで繰り返す`{:class="block3control"}ブロックを**制御**セクションから取り出し、`(10)歩動かす`{:class="block3motion"}ブロックと`(15)度回す`{:class="block3motion"}ブロックをその中に入れ、次のようにします。

```blocks3
+    repeat until <> 
        move (50) steps
        turn cw (15) degrees
    end
```

--- /task ---

--- task ---

緑の旗をクリックしてプログラムを数回実行し、何が起こるかを見ましょう。 2つのことに気づくと思います。ペンはいつもステージの中央に向かって線を引き始めること、そしてペンがステージの端 (はし) で止まらないことです。

--- /task ---

--- collapse ---
---
title: どうしてペンはこのような動きをするのですか？
---

ペンはいつも中央に向かってかき始めます。 なぜなら、`ペンを下ろす`{:class="block3extensions"}ブロックの後に最初 (さいしょ) に実行される **動き**ブロックは`x座標 (ざひょう) を0、 y座標を0にする`{:class="block3motion"}ブロックだからです。 したがって、ペンはステージの中央に移動しながら線を引くようになります。

`まで繰り返す`{:class="block3control"}ループがチェックする条件を指定していないため、ステージの端でペンが止まりません。 条件が決してみたされないので、ループが繰り返し実行されつづけるのです。 つまりこのままでは、ループは`ずっと`{:class="block3control"}ループのように動作します。

--- /collapse ---

--- task ---

`x座標を0、y座標を0にする`{:class="block3motion"}ブロックを`ペンを下ろす`{:class="block3extensions"}ブロックの前に移動し、 **ペン**セクションから、`ペンを上げる`{:class="block3extensions"}ブロックをコードの先頭に追加します。

--- /task ---

では、`まで繰り返す`{:class="block3control"}ループを直して、止めたいときに止まるようにしましょう。 （目に見えない）スプライトがステージの端に触れて (ふれて) いるかどうかを知りたいので、**調べる**ブロックの、この場合、`に触れた`{:class="block3sensing"}ブロックが必要です。

--- task ---

`に触れた`{:class="block3sensing"}ブロックを`まで繰り返す`{:class="block3control"}ループに追加し、`端`{:class="block3sensing"}をえらびます。 これで、(見えない) スプライトがステージの端に触れる**まで**ループが繰り返されます。

```blocks3
    pen down
+    repeat until <touching [edge v] ?> 
        move (50) steps
        turn cw (15) degrees
    end
```

--- /task ---

--- task ---

`(50)歩動かす`{:class="block3motion"}ブロックの数値 (すうち) を`5`にかえて、テストする前にプログラムが次のようになっていることをたしかめましょう。

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

--- /task ---

このコードを実行すると、ペンがかいた線がステージ上にとどまっていることがわかります。

それだけでなく、あなたのプログラムは円をかくプログラムになりました！ ここで何が起こっているかというと、15度ずつ回転していくと最終的に360度になるため、ペンは完全 (かんぜん) な円をかくようになっているのです。 動く方法を少しかえて、毎回少し長く動くようにします。そうすると、らせんじょうに広がっていきます。 これには**変数** (へんすう) が必要になります。

変数は基本的には、数値やその他の大切な情報 (じょうほう) をしまうための名前の付いた場所のことです。 **変数**ブロックセクションで作成 (さくせい) できます。

--- task ---

`ステップ数`{:class="block3variables"}という名前の変数を作り、`(ステップ数)を0にする`{:class="block3variables"}ブロックをプログラムの先頭に追加します。

```blocks3
    when green flag clicked
+   set [ステップ数 v] to [0]
    pen up
```

--- /task ---

--- task ---

次に、`(5)歩動かす`{:class="block3motion"}ブロックの`5`の代わりに`ステップ数`{:class="block3variables"}の値を使用し、ループの中に`ステップ数を1ずつ変える`{:class="block3variables"}ブロックを追加します。

```blocks3
    pen down
    repeat until <touching [edge v] ?> 
+       move (ステップ数) steps
        turn cw (76) degrees
+        change [ステップ数 v] by (1)
    end
```

--- /task ---

ループのどこに`ステップ数を1ずつ変える`{:class="block3variables"}ブロックを入れるかは重要だと思いますか？

--- collapse ---
---
title: 正しい順序 (じゅんじょ) でコードをならべる
---

ブロックをおく順番を決めるときは、それぞれのブロックが何をするか、コードに何をさせたいかを考えてみましょう。

このプロジェクトでは、ペンを動かしてから回転させるということを何度も繰り返します。 これを行うたびに、1ステップずつ長く移動させます。

そのため、`ステップ数を1ずつ変える`{:class="block3variables"}ブロックを` (ステップ数) 歩動かす`{:class="block3motion"}ブロックの**後**に置くのは理にかなっています。 ただし、移動した後で、ペンが最初に回転してからステップ数が変わるのか、またはステップ数が最初に変わってからペンが回転するのかはどちらでも問題ありません。

--- /collapse ---

--- task ---

ここでプログラムを実行し、回転角度を変えてみましょう (`76`度および`120`度をためしてみてください)！

--- /task ---