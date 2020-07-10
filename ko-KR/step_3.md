## Drawing patterns

Now you’ve got a program that draws a line, but it only draws one line. That’s a bit dull! You could use `forever`{:class="block3control"} loop to draw something over and over again, but then you’ll get drawings that go off the Stage!

So you need use a different type of loop called `repeat until`{:class="block3control"}, which you’ll also find in the **Control** section. This type of loop will do something over and over again, **until** a True/False condition is met.

\--- task \---

`까지 반복하기`{:class="block3control"} 블록을 **제어** 카테고리에서 꺼내 추가합니다. 그리고 `만큼 움직이기`{:class="block3motion"} 블록과 `방향으로 회전하기`{:class="block3motion"} 블록을 아래와 같이 추가합니다:

```blocks3
+ < > 까지 반복하기
        (50) 만큼 움직이기
        cw 방향으로 (15) 도 회전하기
    끝
```

\--- /task \---

\--- task \---

Now click the green flag to run the program a few times and see what happens. You’ll notice two things: the pen always starts by drawing a line towards the middle of the Stage, and it doesn’t stop at the edge.

\--- /task \---

## \--- collapse \---

## title: Why does the pen do this?

펜은 항상 중앙에서 그리기를 시작하게 됩니다. 왜냐하면 첫 번째 **동작** 블록이 `펜 내리기`{:class="block3extensions"} 블록과 `x: 0 y: 0 으로 이동하기`{:class="block3motion"} 블록 이후에 실행됩니다. 따라서 펜은 스테이지의 가운데로 이동할 때 선을 그립니다.

펜은 스테이지의 가장자리에서 멈추지 않습니다. `까지 반복하기`{:class="block3control"} 블록의 조건이 아직 정해지지 않았기 때문입니다. 즉, 조건이 충족 될 수 없으므로 루프가 계속 실행됩니다. 이것은 지금, 루프가 `무한 반복`{:class="block3control"} 하고 있다는 것을 말합니다.

\--- /collapse \---

\--- task \---

`x: 0 y: 0 으로 이동하기`{:class="block3motion"} 블록을 `펜 내리기`{:class="block3extensions"} 블록 이전에 추가합니다. 그리고, **펜** 카테고리에서 `펜 올리기`{:class="block3extensions"} 블록을 코드 시작에 추가합니다.

\--- /task \---

이제 `까지 반복하기`{:class="block3control"} 반복문을 수정하여 원하는 때 멈출 수 있도록 해야 합니다. 당신은 (보이지 않는) 스프라이트가 스테이지의 가장자리에 닿아 있는지 알아내기 위해 **감지** 블록을 활용합니다. — 이 경우에는, `에 닿았는가?`{:class="block3sensing"} 블록을 사용합니다.

\--- task \---

`에 닿았는가?`{:class="block3sensing"} 블록을 `까지 반복하기`{:class="block3control"} 루프 안에 넣고, 옵션을 `벽`{:class="block3sensing"} 으로 선택합니다. 그런 다음에 반복문은 (보이지 않는) 스프라이트가 벽에 닿을 **때까지** 반복하게 됩니다.

```blocks3
    펜 내리기
+ <touching [edge v] ?> 까지 반복하기
        (50) 만큼 움직이기
        cw 방향으로 (15) 도 회전하기
    끝
```

\--- /task \---

\--- task \---

`만큼 움직이기`{: class = "block3motion"} 블록의 변수를 `5`로 변경하고 테스트하기 전에 프로그램이 아래 프로그램과 일치하는지 확인하십시오.

```blocks3
    녹색 깃발이 클릭되었을 때
    펜 올리기
    숨기기
    지우기
    x: (0) y: (0) 로 이동
    펜 색깔을 [#4a6cd4] 으로 정하기
    펜 내리기
    <touching [edge v] ?> 까지 반복하기 
        (5) 만큼 움직이기
        cw 방향으로 (15) 도 회전하기
    끝
```

\--- /task \---

코드를 지금 실행하면 펜이 그린 그림이 스테이지에 남아 있음을 알 수 있습니다.

그 뿐만 아니라 프로그램이 원 그리기 프로그램으로 바뀌었습니다! 여기서 일어난 일은 15도 회전이 360도까지 증가하여 합쳐 지므로 펜이 완전한 원형으로 변하는 것입니다. 매번 조금씩 움직이는 방식을 약간 바꿔서 나선형으로 바꿔 놓을 것입니다. 이를 위해서는 **변수**가 필요합니다.

변수는 기본적으로 숫자나 다른 정보를 저장하는 곳으로 라벨이 붙어 있습니다. 당신은 변수를 **변수** 카테고리에서 만들 수 있습니다.

\--- task \---

`단계`{: class = "block3variables"}이라는 변수를 만든 다음 프로그램 시작시 `단계 을 0 로 정하기`{:class="block3variables"} 블록을 프로그램 시작에 추가합니다.

```blocks3
    녹색 깃발이 클릭되었을 때
+ [step v]변수를 [0] 로 정하기
    펜 올리기
```

\--- /task \---

\--- task \---

그 다음, `만큼 움직이기`{:class="block3motion"} 블록의 `5` 대신 `단계`{:class="block3variables"} 블록을 사용하고, `단계 을 1만큼 바꾸기`{:class="block3variables"} 블록을 반복문에 추가합니다:

```blocks3
    펜 내리기
    <touching [edge v] ?> 까지 반복하기 
+ (단계) 만큼 이동하기
        cw 방향으로 (76) 도 회전하기
+ [단계 v] 을 (1) 만큼 바꾸기
    끝
```

\--- /task \---

루프에서 `단계 을 1만큼 바꾸기`{{class = "block3variables"} 블록을 어디에 넣는 것이 중요하다고 생각하나요?

## \--- collapse \---

## title: Putting code in the right order

블록을 넣을 순서를 결정할 때 각 블록이 하는 일과 코드에서 수행 할 작업을 생각합니다.

이 경우, 펜을 움직이게 한 다음, 반복적으로 돌려야 합니다. 이 작업을 수행 할 때마다 펜의 움직임이 한 단계 더 나아가고 싶다는 마음이 생길 것입니다.

따라서 `단계 을 1만큼 바꾸기`{: class = "block3variables"} 블록을 `만큼 움직이기`{: class = "block3motion"} 블록**이후**에을 지정하는 것이 좋습니다. 그러나 이동 후 펜이 먼저 회전하고 그 다음에 단계가 바뀌거나 또는 단계가 먼저 바뀌고 그 다음에 펜이 대신 회전해도 실제로는 상관없습니다.

\--- /collapse \---

\--- task \---

이제 프로그램을 실행하고 각도값을 변경해보십시오 (`76` 혹은 `120` 을 시도해보세요)!

\--- /task \---