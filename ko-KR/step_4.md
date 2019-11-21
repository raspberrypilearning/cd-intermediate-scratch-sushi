## 입력 요청

지금 제작한 프로그램은 아주 멋지지만, 다른 패턴을 그리고 싶을 때마다 코드를 편집해야 하는 것은 매우 지루한 작업입니다. 프로그램을 실행할 때마다 사용할 값을 물어보게 하는 게 좋지 않을까요? 당신은 할 수 있습니다!

\--- task \--- 먼저, **변수** 카테고리로 이동하여 `degrees`{:class="block3variables"} 라는 이름을 가진 변수와 `increase`{:class="block3variables"} 라는 이름을 가진 변수를 생성하세요. \--- /task \---

\--- task \--- 다음과 같이 새로운 변수를 코드에 추가합니다:

```blocks3
    <touching [edge v] ?> 까지 반복하기
       (steps) 만큼 움직이기
       cw 방향으로 (degress ::variables) 도 회전하기
       [steps v] 를 (increase ::variables) 만큼 바꾸기
    끝
```

\--- /task \---

이제 이 두 변수의 값을 물어보고 저장해야합니다. **감지** 카테고리의 `묻고 기다리기`{:class="block3sensing"} 블록을 활용할 수 있습니다.

\--- task \--- `묻고 기다리기`{:class="block3sensing"} 블록을 기존 코드에 추가하고, 질문의 내용을 `얼마나 많은 단계를 거쳐야 하나요?`{:class="block3sensing"} 로 변경하세요.

묻고 기다리기 블록 이전에 `steps`{:class="block3variables"} 변수를 `0` 으로 초기화해 줘야 합니다. 다음과 같이 프로그램에 추가하세요:

```blocks3
    녹색 깃발이 클릭되었을 때
   [steps v] 을 [0] 로 정하기
+   [얼마나 많은 단계를 거쳐야 하나요?] 라고 묻고 기다리기
    펜 올리기
```

\--- /task \---

이제 질문을 묻는 프로그램이 생겼습니다. 질문에 대한 대답을 기억해야 합니다! 스크래치에는 `대답`{:class="block3sensing"}이라고 하는 특별한 변수가 있습니다. 이 변수는 묻고 기다리기 블록의 질문에 대한 답을 저장합니다. 이 변수는 **감지** 카테고리에서 찾을 수 있습니다.

\--- task \--- **변수** 카테고리에 있는 `로 정하기`{:class="block3variables"} 블록을 사용하여, `대답`{:class="block3sensing"} 변수안에 있는 값을 `increase`{:class="block3variables"} 변수에 저장하세요:

```blocks3
    [얼마나 많은 단계를 거쳐야 하나요?] 라고 묻고 기다리기
+    [increase v] 을 (answer) 로 정하기
```

\--- /task \---

\--- task \--- 이제 다음과 같은 질문에 대한 답을 받아서 `degrees`{:class="block3variables"} 변수에 저장해야 합니다. `몇 도 돌려야 할까요?`{:class="block3sensing"} 라고 질문한 뒤 `대답`{:class="block3sensing"} 변수에 있는 이 값을 `degrees`{:class="block3variables"}변수에 저장합니다:

```blocks3
    [increase v] 를 (answer) 로 정하기
+   [몇 도 돌려야 할까요?] 라고 묻고 기다리기
+    [degrees v] 를 (answer) 로 정하기
```

\--- /task \---

\--- task \--- 프로그램이 아래처럼 보이는지 확인하고 다른 값을 넣어 몇 번 실행하십시오. 가장 멋진 그림을 만들어주는 값을 기록해 두세요. 다음 단계에서 이러한 값들을 필요로 합니다!

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