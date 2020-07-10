## طلب مدخلات

حسنًا ، هذا أمر رائع ، لكن من الممل قليلاً أن تضطر إلى تعديل التعليمات البرمجية في كل مرة تريد فيها رسم نمط مختلف. ألن يكون من الجيد جعل البرنامج يطلب منك ادخال القيم ليستخدمها؟ يمكنك فعل هذا!

--- task ---

أولاً, انتقل إلى قسم **المتغيرات** وانشئ متغيرات جديدة سمها `درجات`{:class="block3variables"} و `زيادة`{:class="block3variables"}.

--- /task ---

--- task ---

الان اضف المتغيرات الجديدة لتعليماتك البرمجية مثل هذا:

```blocks3
    repeat until <touching [edge v] ?> 
        move (خطوات) steps
        turn cw (درجات ::variables) degrees
        change [خطوات v] by (زيادة ::variables)
    end
```

--- /task ---

أنت الآن بحاجة إلى طلب قيم لهذين المتغيرين وتخزينهم. يمكنك القيام بذلك باستخدام كتلة **تحسس** تسمى `اسأل وانتظر`{:class="block3sensing"}, و التي يمكنك كتابة سؤال فيها.

--- task ---

اسحب كتلة `اسأل وانتظر`{:class="block3sensing"} إلى لوحة العفريت وقم بتغيير السؤال إلى `كم عدد الخطوات التي يجب أن أتقدم بها؟ `{:class="block3sensing"}

ثم قم بإضافته إلى البرنامج ، مباشرة بعد جعل `خطوات`{:class="block3variables"} مساوياً لـ `0` ، مثل:

```blocks3
    when green flag clicked
    set [خطوات v] to [0]
+    ask [كم عدد الخطوات التي يجب أن أتقدم بها؟] and wait
    pen up
```

--- /task ---

الآن لديك برنامج يطرح سؤالاً ، فأنت تريده ان يتذكر الإجابة! اتضح أن سكراتش له متغير خاص يسمى `الإجابة`{:class="block3sensing"}، حيث يخزن آخر إجابة تلقاها. يمكنك العثور على هذا المتغير بين كتل **التحسس**.

--- task ---

باستخدام كتل `اجعل مساوياً`{:class="block3variables"} من قسم **المتغيرات**, خذ قيمة `الاجابة`{:class="block3sensing"} وخزنها في متغير `زيادة`{:class="block3variables"} مثل هذا:

```blocks3
    ask [كم عدد الخطوات التي يجب أن أتقدم بها؟] and wait
+    set [زيادة v] to (answer)
```

--- /task ---

--- task ---

الان, افعل نفس الشيئ مع `درجات`{:class="block3variables"}, اسال `كم درجة يجب ان تكون الاستدارة الخاصة بي؟`{:class="block3sensing"} وخزن قيمة `الإجابة`{:class="block3sensing"} في متغير `درجات`{:class="block3variables"}:

```blocks3
    set [زيادة v] to (answer)
+    ask [كم درجة يجب ان تكون الاستدارة الخاصة بي؟] and wait
+    set [درجات v] to (answer)
```

--- /task ---

--- task ---

تحقق من أن برنامجك يشبه الآن البرنامج أدناه ، وقم بتشغيله عدة مرات بأرقام مختلفة. اكتب الإجابات التي تصنع أروع الصور. ستحتاج إليهم في خطوة لاحقة!

```blocks3
    when green flag clicked
    set [خطوات v] to [0]
    ask [كم عدد الخطوات التي يجب أن أتقدم بها؟] and wait
    set [زيادة v] to (answer)
    ask [كم درجة يجب ان تكون الاستدارة الخاصة بي؟] and wait
    set [درجات v] to (answer)
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (خطوات) steps
        turn cw (درجات) degrees
        change [خطوات v] by (زيادة)
    end
```

--- /task ---