## جعل كل شيء عشوائي

يمكنك بالحقيقة استخدام أرقام عشوائية لجعل البرنامج بأكمله يعمل مرارًا وتكرارًا ، مع تغيير النمط في كل مرة! سيبدو قليلاً كما فعلت شاشات التوقف في التسعينيات... وهو أمر ربما لن تتذكره ، ولكن اسأل أحد والديك!

تحتاج إلى بعض التغييرات لجعل هذا يحدث. أول واحد هو أنك تحتاج إلى تعيين متغيرين `زيادة`{:class="block3variables"} و `درجات`{:class="block3variables"} عشوائيًا بدلاً من طلبها من المستخدم. لذلك تحتاج إلى تغيير بعض كتل التعليمات البرمجية الخاصة بك.

--- task ---

قم بإزالة الأسئلة من الكود الخاص بك، وقم بتحديثه لاستخدام أرقام عشوائية بدلاً من ذلك.

```blocks3
    when green flag clicked
    set [خطوات v] to [0]
-    ask [كم عدد الخطوات التي يجب أن أتقدم بها؟] and wait
+    set [زيادة v] to (pick random (1) to (10))
-    ask [كم درجة يجب ان تكون الاستدارة الخاصة بي؟] and wait
+    set [درجات v] to (pick random (1) to (180))
    pen up
```

--- /task ---

إذا قمت بتشغيل البرنامج الآن ، فستجد أنه يرسم نمطًا عشوائيًا ، ولكن مرة واحدة فقط. لماذا تعتقد ذلك؟

ذلك لأن الحلقة تعمل فقط حتى تصل إلى حافة المنصة.

--- task ---

تحتاج إلى حلقة أخرى تعمل إلى الأبد (لذلك كتلة `كرر باستمرار`{:class="block3control"}!) خارج الحالية لابقائها تعمل مراراً وتكراراً. فقط اسحب واحدة من قسم **التحكم**، وإضاف جميع التعليمات البرمجية الأخرى فيها.

```blocks3
    when green flag clicked
+    forever 
        set [خطوات v] to [0]
        set [زيادة v] to (pick random (1) to (10))
        set [درجات v] to (pick random (1) to (180))
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
    end
```

--- /task ---

الآن لديك حقا شيء رائع للنظر اليه!

ومع ذلك ، قد تلاحظ أنه ،بين الحين والآخر ، يرسم الكمبيوتر شيئًا يبدو سيئًا. هذا لأن بعض الأرقام لبعض هذه المتغيرات هي مجرد خيارات سيئة ، وبعض **مجموعات من تلك الأرقام** هي أيضا خيارات سيئة.

في البطاقة التالية، سوف تساعد الكمبيوتر على اختيار مجموعات جيدة فقط!