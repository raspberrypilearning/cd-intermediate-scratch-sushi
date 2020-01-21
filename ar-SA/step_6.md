## جعل كل شيء عشوائي

يمكنك بالحقيقة استخدام أرقام عشوائية لجعل البرنامج بأكمله يعمل مرارًا وتكرارًا ، مع تغيير النمط في كل مرة! سيبدو قليلاً كما فعلت شاشات التوقف في التسعينيات... وهو أمر ربما لن تتذكره ، ولكن اسأل أحد والديك!

تحتاج إلى بعض التغييرات لجعل هذا يحدث. أول واحد هو أنك تحتاج إلى تعيين متغيرين `زيادة`{:class="block3variables"} و `درجات`{:class="block3variables"} عشوائيًا بدلاً من طلبها من المستخدم. لذلك تحتاج إلى تغيير بعض كتل التعليمات البرمجية الخاصة بك.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    عندما نقر  العلم الأخضر
    اجعل [خطوات v] مساوياً [0]
-    اسأل [كم عدد الخطوات التي يجب عليّ أن أنمو بها؟] وانتظر
+    اجعل [زيادة v] مساوياً (عدد عشوائي بين (1) و (10))
-    اسأل [كم درجة يجب أن استدر؟] وانتظر
+ اجعل [درجات v] إلى (عدد عشوائي بين (1) و (180))
    ارفع القلم
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    عند نقر العلم الاخضر
+    كرر باستمرار 
        اجعل [خطوات v] مساويا [0]
         اجعل [زيادة v] مساوياً (رقم عشوائي بين(1) و(10))
        اجعل [درجات v] مساوياً (رقم عشوائي بين(1) و(180))
        ارفع القلم
        اختف
        امسح الكل
        اذهب إلى الموضع x: (0) y: (0)
        اجعل لون القلم مساوياً [#4a6cd4]
        أنزل القلم
        كرر حتى <touching [edge v] ?> 
            تحرك (خطوات) خطوة
            استدر باتجاه عقارب الساعة (درجات) درجة
            غير [درجات v] بمقدار (زيادة)
        النهاية
    النهاية
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!