## 随机呈现整个内容

你实际上可以使用随机数来使整个程序反复运行，每次都更改模式！ 它会看起来有点像1990年代的屏幕保护程序……你可能不会记得，但请问你的父母！

你需要进行一些更改才能实现此目的。 首先你需要随机设置 `increase`{:class="block3variables"} 和 `degrees`{:class="block3variables"} 变量，而不是向用户询问。 所以你需要更改你的一些代码块。

\--- task \---

从你的代码中删除询问逻辑并使用随机的数字块替代它。

```blocks3
    when green flag clicked
    set [steps v] to [0]
-    ask [How many steps should I grow by?] and wait
+    set [increase v] to (pick random (1) to (10))
-    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (pick random (1) to (180))
    pen up
```

\--- /task \---

如果现在运行程序，你会发现它确实绘制了一个随机模式，但是只有一次。 你认为为什么会这样?

这是因为循环会在运行到到达舞台边缘时停止。

\--- task \---

你需要在当前代码块之外再添加一个循环（`重复执行` {:class=“block3control”}）块，以使其不断重复。 只需从**控制**部分拖动一个，然后将其他所有的代码都添加进去。

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

现在，您真的有一些很棒的东西可以看！

但是，您可能会注意到，计算机会时不时地绘制出一些看起来很糟糕的东西。 这是因为其中一些变量的某些数字只是不好的选择，其中某些**数字组合**也是不好的选择。

在下一张卡片上，您会帮助计算机只挑选好的组合！