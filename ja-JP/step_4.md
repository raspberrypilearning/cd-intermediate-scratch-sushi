## 入力をもとめる

さて、すでにかなりクールになっていますが、べつのもようをかきたい時に毎回コードを編集 (へんしゅう) する必要があるのは少しうんざりします。 プログラムが使用する値を聞いてくれるようになればいいのではないでしょうか？ こうすればできます。

\--- task \---

まず、**変数**セクションに移動します。そして`回転角度`{:class="block3variables"}および`ふやす量`{:class="block3variables"}という名前の変数を作成します。

\--- /task \---

\--- task \---

そして、次のように新しい変数をコードに追加します。

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

次に、これらの2つの変数の値をたずね、保存 (ほぞん) する必要があります。 `と聞いて待つ`{:class="block3sensing"}という**調べる**ブロックを使えばできます。このブロックは質問 (しつもん) を表示できます。

\--- task \---

`と聞いて待つ`{:class="block3sensing"}ブロックをスプライトパネルに引き出して、質問文を`何ステップずつふやしますか？`{:class="block3sensing"}に変えます。

そして、プログラムの`ステップ数`{:class="block3variables"}を`0`にした直後にこのブロックを追加します。次のようになります。

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    when green flag clicked
    set [steps v] to [0]
    ask [How many steps should I grow by?] and wait
    set [increase v] to (answer)
    ask [How many degrees should I turn?] and wait
    set [degrees v] to (answer)
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
```

\--- /task \---