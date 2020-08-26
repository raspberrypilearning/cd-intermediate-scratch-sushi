## Запит на введення даних

Гаразд, це виглядає досить круто, але трохи нудно редагувати код кожного разу, коли хочеться намалювати інший візерунок. Чи не було б краще, щоб програма запитувала в тебе, які значення використовувати? Ти можеш це зробити!

\--- task \---

Спочатку перейди у розділ **Змінні** та створи змінні з назвами `градуси`{:class="block3variables"} та `приріст`{:class="block3variables"}.

\--- /task \---

\--- task \---

Тепер додай нові змінні до свого коду наступним чином:

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

Тепер тобі потрібно запитати значення для цих двох змінних і зберегти їх. Це можна зробити використовуючи блок `запитати і чекати`{:class="block3sensing"} з розділу **Датчики**, куди можна ввести запитання.

\--- task \---

Перетягни блок `запити і чекати`{:class="block3sensing"} до панелі спрайтів та заміни запитання на `На скільки кроків збільшуватись?`{:class="block3sensing"}

Потім додай цей блок до програми, одразу після встановлення значення для змінної `кроки`{:class="block3variables"} до `0`, ось так:

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

\--- /task \---

Зараз у тебе є програма, яка задає питання, а тепер потрібно, щоб вона запам'ятала відповідь! Виявляється, що Скретч має спеціальну змінну під назвою `відповідь`{:class="block3sensing"}, де зберігається остання відповідь, яку отримала програма. Ти знайдеш цю змінну серед блоків розділу **Датчики**.

\--- task \---

Використовуючи блок `надати значення`{:class="block3variables"} з розділу **Змінні**, візьми значення `відповідь`{:class="block3sensing"} і збережи його у змінній `приріст`{:class="block3variables"} як тут:

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

\--- /task \---

\--- task \---

Тепер зроби те ж саме зі змінною `градуси`{:class="block3variables"}, запитуючи `На скільки градусів повертати?`{:class="block3sensing"} і зберігаючи значення `відповідь`{:class="block3sensing"} у змінній `градуси`{:class="block3variables"}:

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

\--- /task \---

\--- task \---

Перевір, чи виглядає твоя програма так, як наведено нижче, і запусти її кілька разів з різними числами. Запиши відповіді, які створюють найкрутіші малюнки. Вони знадобляться тобі на наступному кроці!

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