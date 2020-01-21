## 펜 도구 사용

여러분이 제작할 이 프로젝트는 **펜** 도구를 사용합니다. 이 도구는 스프라이트가 움직일 때 그 중심에 선을 그립니다. 당신은 지금 이 도구를 사용하는 법을 배울 것입니다!

\--- task \---

Open a new Scratch file, select the Scratch Cat sprite, and drag in a few blocks you may have already seen, until it looks like this:

```blocks3
    녹색 깃발이 클릭되었을 때
    x: (0) y: (0) 로 이동하기
    (50) 만큼 움직이기
    cw 방향으로 (15) 도 회전하기
```

\--- /task \---

Now, time to test out the pen!

To use the Pen blocks in Scratch, you need add the **Pen extension**.

\--- task \---

Click on the **Add extension** button in the bottom left-hand corner.

![add extension button highlighted](images/add-extension-annotated.png)

Click on the **Pen** extension to add it.

![pen extension highlighted](images/click-pen-annotated.png)

The Pen section then appears at the bottom of the blocks menu.

![pen extension blocks](images/pen-extension-blocks.png)

From the **Pen** section, select the `pen down`{:class="block3extensions"} block and add it to the start of your program, like this:

```blocks3
    녹색 깃발이 클릭되었을 때
+    펜 내리기
    x: (0) y: (0) 로 이동하기
```

\--- /task \---

\--- task \---

Now click the green flag a few times and watch what happens.

\--- /task \---

If you can see the lines behind the cat sprite, then the pen is working and you can start making it draw really cool patterns.

First, you should get rid of the sprite. It’s getting in the way of the drawing!

\--- task \---

Add a `hide`{:class="block3looks"} block from **Looks** to the start of the program and it’ll disappear.

```blocks3
    녹색 깃발이 클릭되었을 때
+ 숨기기
    펜 내리기
```

\--- /task \---

Now, you can change the colour of the pen with another block from the **Pen** section, but the block is a little different to the others you’ve seen. It’s the `set pen color to`{:class="block3extensions"} block and looks like this:

```blocks3
    펜 색깔을 [#4a6cd4] (으) 로 정하기
```

\--- task \---

Drag a `set pen color to`{:class="block3extensions"} block into your sprite panel, and snap it in above the `pen down`{:class="block3extensions"} block.

```blocks3
    녹색 깃발이 클릭되었을 때
    숨기기
+ 펜 색깔을 [# 4a6cd4] 으로 정하기
    펜 내리기
```

Now, click on the box of colour (in the code above it’s the blue one), and choose a colour.

\--- /task \---

If you’ve been clicking on the green flag to test your code, you’ll have noticed that the drawings the pen makes don’t go away.

\--- task \---

Add a `clear`{:class="block3extensions"} block from the **Pen** section to the start of your code to take care of that:

```blocks3
    녹색 깃발이 클릭되었을 때
+ 모두 지우기
    숨기기
```

\--- /task \---