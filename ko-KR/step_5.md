## 멋진 라인

이제 색상을 추가해 볼 시간입니다! 지금은 선이 하나의 색이지만 ** 펜 ** 색상을 변경할 수있는 블록이 있습니다. 그리고 ** 연산자 ** 블록을 사용하면 색상을 임의로 변경할 수도 있습니다.

**펜** 색상을 변경하기 위한 블록은 `펜 색상을 만큼 바꾸기`{:class="block3extensions"} 블록입니다:

```blocks3
    펜 색깔을 (10) 만큼 바꾸기
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    <touching [edge v] ?> 까지 반복하기
+        펜 색깔을 (10) 만큼 바꾸기
       (steps) 만큼 움직이기
       cw 방향으로 (degress ::variables) 도 회전하기
       [steps v] 를 (increase ::variables) 만큼 바꾸기
    끝
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    <touching [edge v] ?> 까지 반복하기
+        펜 색깔을 ((1) 부터 (100) 사이의 난수) 만큼 바꾸기
       (steps) 만큼 움직이기
       cw 방향으로 (degress ::variables) 도 회전하기
       [steps v] 를 (increase ::variables) 만큼 바꾸기
    끝
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---