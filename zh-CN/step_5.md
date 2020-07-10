## 更酷的线条

是时候添加颜色了！ 现在，你的线是一种颜色，但是**画笔**中有积木可以改变它的颜色。 同时加上正确的**运算**块，你甚至可以随机更改颜色！

更改**画笔**颜色的方块是 通过`将笔的颜色设为`{:class="block3extensions"}：

```blocks3
    change pen color by (10)
```

--- task ---

抓住其中一个块并将其放入你的`重复执行直到`{:class="block3control"}循环，如下所示：

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (步骤) steps
        turn cw (度数 ::variables) degrees
        change [步骤 v] by (增加 ::variables)
    end
```

--- /task ---

虽然这很酷，但它是可预测的，没有太多变化。 如果在其中添加一个随机数，可以使其更有趣，颜色也会随机变化。

--- task ---

将随机数 **运算** 块放入 `将笔的颜色设为`{:class="block3extensions"} 块中，并选择一些值。 试着用`1`和`100`开始。

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (pick random (1) to (100))
        move (步骤) steps
        turn cw (度数 ::variables) degrees
        change [步骤 v] by (增加 ::variables)
    end
```

--- /task ---

--- task ---

尝试再次运行它，就能观看随机的彩虹！

--- /task ---