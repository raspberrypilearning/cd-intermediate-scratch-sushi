## すべてをランダムにする

じっさいに乱数を使って、プログラム全体を何度も実行し、そのたびにもようを変えることができます。 1990年代のスクリーンセーバーのようになりますが・・・おぼえていないかもしれませんね。お父さんかお母さんに聞いてみてください。

そうするには、いくつか変える必要があります。 まず最初に、ユーザーにたずねるのではなく、`ふやす量`{:class="block3variables"}と`回転角度`{:class="block3variables"}変数をランダムに設定 (せってい) する必要があります。 したがって、コードブロックの一部を変える必要があります。

\--- task \---

コードから質問ブロックを削除 (さくじょ) し、代わりに乱数を使いましょう。

```blocks3
    緑色の旗が押されたとき
    [ステップ数 v] を [0] にする
- [何ステップずつふやしますか？] と聞いて待つ
+ [ふやす量 v] を ((1) から (10) までの乱数) にする
- [何度回転しますか？] と聞いて待つ
+ [回転角度 v] を ((1) から (180) までの乱数) にする
    ペンを上げる
```

\--- /task \---

今プログラムを実行すると、ランダムなもようがえがかれますが、1回だけで終わってしまいます。 なぜだと思いますか？

これは、ループがステージの端に到達 (とうたつ) するまでしか実行されないためです。

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    when green flag clicked
+    forever 
        set [steps v] to [0]
        set [increase v] to (pick random (1) to (10))
        set [degrees v] to (pick random (1) to (180))
        pen up
        hide
        clear
        go to x: (0) y: (0)
        set pen color to [#4a6cd4]
        pen down
        repeat until <touching [edge v] ?> 
            move (steps) steps
            turn cw (degrees) degrees
            change [steps v] by (increase)
        end
    end
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!