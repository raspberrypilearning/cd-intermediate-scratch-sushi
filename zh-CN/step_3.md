## 绘制图案

现在，你有一个可以画一条线的程序，但它也只能画一条线。 这样有点呆板！ 你可以使用 `重复执行`{:class="block3control"} 循环来一遍又一遍地绘制一些东西，但是你的画很快会超出舞台边界。

所以你需要用到一个不同类型的循环，叫做`重复执行直到`{:class="block3control"}，你可以从**控制**部分找到它。 这种类型的循环会反复执行某些操作，**直到**满足对/错条件。

--- task ---

从**控制**中拖一个`重复执行直到`{:class="block3control"}块出来 ，然后放置`移动`{:class="block3motion"} 和 `左转`{:class="block3motion"} 块，就像这样：

```blocks3
+    repeat until <> 
        move (50) steps
        turn cw (15) degrees
    end
```

--- /task ---

--- task ---

现在，单击绿色旗子几次来运行该程序，然后看看会发生什么。 你会注意到两件事：笔总是从在舞台中间画一条线开始，而它并没有在边缘处停止。

--- /task ---

--- collapse ---

## 标题：为什么笔会这样做？

笔总是从中间的方向开始绘制，因为在 `落笔`{:class="block3extensions"}后第一个运行的**运动**是`移到 x：0 y：0`{:class="block3motion"}。 因此，笔在移到舞台中央的过程中会画一条线。

笔不会停在舞台的边缘，因为你还没有告诉`重复执行直到`{:class="block3control"}循环检查的条件。 这意味着永远无法满足循环停止的条件，因此它将不断运行。 这意味着，这个循环就像`重复执行`{:class="block3control"}循环一样工作。

--- /collapse ---

--- task ---

把`移到 x: 0 y`{:class="block3motion"} 块挪到 `画笔`{:class="block3extensions"} 块之前，并从**画笔**部分拿一个`抬笔`{:class="block3extensions"} 块到右端代码的开头。

--- /task ---

是时候修复你的`重复执行直到`{:class="block3control"}循环了，以使其在你需要时停止。 你得知道（隐藏起来的）精灵是否接触到了舞台边缘，为此你需要**侦测** 工具中的 `碰到?`{:class="block3sensing"}块。

--- task ---

添加`碰到?`{:class="block3sensing"}块到你的`重复执行直到`{:class="block3control"}循环，然后选择`舞台边缘`{:class="block3sensing"}。 然后循环运行**重复执行直到** （隐藏起来的）精灵触及舞台的边缘。

```blocks3
    pen down
+    repeat until <touching [edge v] ?> 
        move (50) steps
        turn cw (15) degrees
    end
```

--- /task ---

--- task ---

更改`移动`{class="block3motion"}块中的步骤数为`5` ，并在测试之前检查程序是否与此程序匹配：

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

如果现在运行代码，你将看到钢笔绘制的图形停留在舞台上。

不仅如此，你的程序还变成了画圆的程序！ 此处发生的情况是，这些15度的转弯最终加起来为360度，因此你的笔旋转了一个完整的圆圈。 你将稍微更改它的移动的方式，使它每次都稍微多走一步，这样它就会螺旋式向外移动。 为此，你将需要一个**变量** 。

变量基本上就是一种带有标签的位置，在位置中存储数字或其它你关心的信息。 你可以在 **变量** 部分中创建它们。

--- task ---

创建一个名为 `步骤`{:class="block3variables"}的变量，然后添加一个 `将 步骤 设为 0`{:class="block3variables"} 块到程序的开头。

```blocks3
    when green flag clicked
+   set [步骤 v] to [0]
    pen up
```

--- /task ---

--- task ---

然后用`步骤`{:class="block3variables"}块替换`移动`{:class="block3motion"}块中的`5`，之后加入`将 步骤 增加 1`{:class="block3variables"}块作为循环的一部分：

```blocks3
    pen down
    repeat until <touching [edge v] ?> 
+       move (步骤) steps
        turn cw (76) degrees
+        change [步骤 v] by (1)
    end
```

--- /task ---

你觉得在循环中的不同位置放置`将 步骤 增加 1`{:class="block3variables"} 块会不一样吗？

--- collapse ---
---
title: 以正确的顺序放置代码
---

当你决定哪个命令放置方块时，想想每个方块做什么以及你想要你的代码做什么。

在这种情况下，你想要笔移动，然后一遍又一遍地转动。 每次执行此操作时，你都希望再移动一个额外的步骤。

因此，将`将 步骤 增加`{:class="block3variables"} 块放置在 `移动`{:class="block3motion"}块 **之后** 是有意义的。 然而在移动后，笔先转动再改变步骤数， 还是先改变步骤数再转笔都不重要。

--- /collapse ---

--- task ---

现在运行程序，并尝试更改周围的度数（尝试`76`和`120` ）！

--- /task ---