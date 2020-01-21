## 입력 요청

지금 제작한 프로그램은 아주 멋지지만, 다른 패턴을 그리고 싶을 때마다 코드를 편집해야 하는 것은 매우 지루한 작업입니다. 프로그램을 실행할 때마다 사용할 값을 물어보게 하는 게 좋지 않을까요? 당신은 할 수 있습니다!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    <touching [edge v] ?> 까지 반복하기
       (steps) 만큼 움직이기
       cw 방향으로 (degress ::variables) 도 회전하기
       [steps v] 를 (increase ::variables) 만큼 바꾸기
    끝
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    녹색 깃발이 클릭되었을 때
   [steps v] 을 [0] 로 정하기
+   [얼마나 많은 단계를 거쳐야 하나요?] 라고 묻고 기다리기
    펜 올리기
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    [얼마나 많은 단계를 거쳐야 하나요?] 라고 묻고 기다리기
+    [increase v] 을 (answer) 로 정하기
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    [increase v] 를 (answer) 로 정하기
+   [몇 도 돌려야 할까요?] 라고 묻고 기다리기
+    [degrees v] 를 (answer) 로 정하기
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    녹색 깃발이 클릭되었을 때
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
```

\--- /task \---