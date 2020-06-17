## 要求输入

好的，这已经很酷了，但是每次你想要绘制不同的图案时都必须编辑代码有点无聊。 让程序询问你要使用的值不是很好吗？ 你可以这样做：

\--- task \---

首先，前往**变量**部分，并创建 `degrees`{:class="block3variables"} 和 `increase`{:class="block3variables"} 的变量。

\--- /task \---

\--- task \---

现在将新的变量添加到你的代码中，例如：

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

现在，你需要询问这两个变量的值并存储它们。 你可以使用一个叫做 `询问并等待` {:class=“block3sensing”} 的 **侦测** 块，你可以在其中输入问题。

\--- task \---

拉取`询问并等待`{:class="block3sensing"} 块进入你的精灵图面板，然后将问题更改为`我应该采取多少步骤？`{:class="block3sensing"}

然后将其添加到你的程序，就在你设置`steps`{:class="block3variables"} 为`0`之后，像这样：

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

\--- /task \---

现在，你的程序能询问问题了，你还需要它记住问题的答案！ Scratch 有一个名为` 回答 ` {:class=“block3sensing”} 的特殊变量，它存储收到的最新答案。 您可以在**侦测**模块中找到此变量。

\--- task \---

使用 ** 变量** 中的 `将变量设为`{:class=“block3variables”} 块，并取值为 ` 回答 ` {:class=“block3sensing”} 并将其存储在变量 `increase` {:class=“block3variables”}中，如下所示：

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

\--- /task \---

\--- task \---

现在，对`degrees` {:class=“block3variables”}进行相同的操作，询问`我应该转动多少度？ ` {:class=“block3sensing”}并在`度` {:class=“block3variables”}：中存储` 回答` {:class=“block3sensing”}的值。

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

\--- /task \---

\--- task \---

现在检查你的程序，如下所示，并使用不同的输入数字运行几次。 写下答案来制作出最酷的图片。 你会在稍后的步骤中需要他们！

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