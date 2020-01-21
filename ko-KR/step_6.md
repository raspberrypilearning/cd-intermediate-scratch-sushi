## 모든 것을 무작위로

실제로 임의의 숫자를 사용하여 매번 패턴을 변경하면서 전체 프로그램을 반복해서 실행할 수 있습니다! 그것은 1990년대 화면 보호기처럼 보일 것입니다. 아마도 기억하지 못할 것이지만, 부모 중 한 명에게 물어보십시오!

이 문제를 해결하려면 몇 가지 변경 사항이 필요합니다. 먼저, `increase`{:class="block3variables"} 와 `degrees`{:class="block3variables"} 변수를 사용자가 요청하지 않고 무작위로 선택하도록 해야 합니다. 아래와 같이 블록을 변경해야 합니다.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    녹색 깃발을 클릭했을 때
   [steps v] 을 [0] 로 정하기
-    [얼마나 많은 단계를 거쳐야 하나요?] 라고 묻고 기다리기
+   [increase v] 을 (pick random (1) to (10)) 로 정하기
-    [몇 도 돌려야 할까요?] 라고 묻고 기다리기
+   [degrees v] 을 (pick random (1) to (180)) 로 정하기
    펜 올리기
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    녹색 깃발이 클릭되었을 때
+ 무한 반복
        [steps v] 을 [0] 로 정하기
        [얼마나 많은 단계를 거쳐야 하나요?] 라고 묻고 기다리기
        [increase v] 을 (answer) 로 정하기
        [몇 도 돌려야 할까요?] 라고 묻고 기다리기
        [degrees v] 을 (answer) 로 정하기
        펜 올리기
        숨기기
        모두 지우기
        x: (0) y: (0) 로 이동하기
        펜 색깔을 [#4a6cd4] 로 정하기
        펜 내리기
        <touching [edge v] ?> 까지 반복하기 
            (steps) 만큼 움직이기
            cw 방향으로 (degrees) 도 회전하기
            [steps v] 을 (increase) 만큼 바꾸기
        끝
    끝
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!