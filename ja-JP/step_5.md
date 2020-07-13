## もっとカッコいい線

色を追加しましょう！ 今のところ、線は1色ですが、**ペン**には色を変えることができるブロックがあります。 そして、**演算** (えんざん) ブロックを使えば、ランダムに色を変えることもできます！

**ペン**の色を変えるブロックは、`ペンの色を(10)ずつ変える`{:class="block3extensions"}ブロックです。

```blocks3
    change pen color by (10)
```

--- task ---

このブロックを`まで繰り返す`{:class="block3control"}ループに入れます。このようになります。

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (ステップ数) steps
        turn cw (回転角度 ::variables) degrees
        change [ステップ数 v] by (ふやす量 ::variables)
    end
```

--- /task ---

カッコいいですが、ちょっと予想がつきますね。 ランダムな数字を使うと色がランダムに変化するので、もっと楽しくすることができます。

--- task ---

乱数 (らんすう) の**演算**ブロックを`ペンの色を(10)ずつ変える`{:class="block3extensions"}ブロックに入れて、乱数の範囲 (はんい) を指定します。 ここでは`1`と`100`を入れてみます。

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (pick random (1) to (100))
        move (ステップ数) steps
        turn cw (回転角度 ::variables) degrees
        change [ステップ数 v] by (ふやす量 ::variables)
    end
```

--- /task ---

--- task ---

もう一度実行してみて、ランダムな色のにじを見ましょう！

--- /task ---