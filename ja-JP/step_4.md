## 入力をもとめる

さて、すでにかなりクールになっていますが、べつのもようをかきたい時に毎回コードを編集 (へんしゅう) する必要があるのは少しめんどうです。 プログラムが使用する値を聞いてくれるようになればいいのではないでしょうか？ こうすればできます。

--- task ---

まず、**変数**セクションに移動します。そして`回転角度`{:class="block3variables"}および`ふやす量`{:class="block3variables"}という名前の変数を作成します。

--- /task ---

--- task ---

そして、次のように新しい変数をコードに追加します。

```blocks3
    repeat until <touching [edge v] ?> 
        move (ステップ数) steps
        turn cw (回転角度 ::variables) degrees
        change [ステップ数 v] by (ふやす量 ::variables)
    end
```

--- /task ---

次に、これらの2つの変数の値をたずね、保存 (ほぞん) する必要があります。 `と聞いて待つ`{:class="block3sensing"}という**調べる**ブロックを使えばできます。このブロックは質問 (しつもん) を表示できます。

--- task ---

`と聞いて待つ`{:class="block3sensing"}ブロックをスプライトパネルに引き出して、質問文を`何ステップずつふやしますか？`{:class="block3sensing"}に変えます。

そして、プログラムの`ステップ数`{:class="block3variables"}を`0`にした直後にこのブロックを追加します。次のようになります。

```blocks3
    when green flag clicked
    set [ステップ数 v] to [0]
+    ask [何ステップずつふやしますか？] and wait
    pen up
```

--- /task ---

プログラムがたずねるようになったので、入力する答えをおぼえさせる必要があります。 Scratch には`答え`{:class="block3sensing"}というとくべつな変数があり、そこには受け取った一番新しい答えがしまわれています。 この変数は、**調べる**ブロックにあります。

--- task ---

**変数**セクションの`(変数)を(0)にする`{:class="block3variables"}ブロックを使って、`答え`{:class="block3sensing"}の値を、`ふやす量`{:class="block3variables"}変数に保存します。

```blocks3
    ask [何ステップずつふやしますか？] and wait
+    set [ふやす量 v] to (answer)
```

--- /task ---

--- task ---

次に、`回転角度`{:class="block3variables"}で同じことをします。`何度回転しますか？`{:class="block3sensing"}とたずね、`答え`{:class="block3sensing"}の値を`回転角度`{:class="block3variables"}に保存します。

```blocks3
    set [ふやす量 v] to (answer)
+    ask [何度回転しますか？] and wait
+    set [回転角度 v] to (answer)
```

--- /task ---

--- task ---

プログラムが次のようになっていることをたしかめてから、ちがう数値で数回実行します。 一番カッコいいもようになる答えを書いておきましょう。 後のステップでその数値が必要になります！

```blocks3
    when green flag clicked
    set [ステップ数 v] to [0]
    ask [何ステップずつふやしますか？] and wait
    set [ふやす量 v] to (answer)
    ask [何度回転しますか？] and wait
    set [回転角度 v] to (answer)
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (ステップ数) steps
        turn cw (回転角度) degrees
        change [ステップ数 v] by (ふやす量)
    end
```

--- /task ---