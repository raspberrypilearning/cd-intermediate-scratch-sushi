## طلب مدخلات

حسنًا ، هذا أمر رائع ، لكن من الممل قليلاً أن تضطر إلى تعديل التعليمات البرمجية في كل مرة تريد فيها رسم نمط مختلف. ألن يكون من الجيد جعل البرنامج يطلب منك ادخال القيم ليستخدمها؟ يمكنك فعل هذا!

\--- task \---

First, go to the **Variables** section and create variables called `degrees`{:class="block3variables"} and `increase`{:class="block3variables"}.

\--- /task \---

\--- task \---

Now add the new variables to your code like this:

```blocks3
    كرر حتى <touching [edge v] ?> 
        تحرك (خطوات) خطوة
        استدر باتجاه عقارب الساعة (درجات ::متغير) درجات
        غير [steps v] بمقدار (زيادة:: متغير)
    النهاية
```

\--- /task \---

Now you need to ask for values for these two variables and store them. You do this using a **Sensing** block called `Ask and wait`{:class="block3sensing"}, which you can type a question into.

\--- task \---

Pull the `Ask and wait`{:class="block3sensing"} block into your sprite panel and change the question to `How many steps should I grow by?`{:class="block3sensing"}

Then add it to your program, just after you set `steps`{:class="block3variables"} to `0`, like this:

```blocks3
    عند نقر العلم الاخضر
    اجعل [steps v] مساوياً [0]
+    اسأل [كم عدد الخطوات التي يجب أن أنمو بها؟] وانتظر
    ارفع القلم
```

\--- /task \---

Now you’ve got your program asking a question, you need it to remember the answer! It turns out that Scratch has a special variable called `answer`{:class="block3sensing"}, where it stores the most recent answer it has received. You can find this variable among the **Sensing** blocks.

\--- task \---

Using a `set to`{:class="block3variables"} block from **Variables**, take the value of `answer`{:class="block3sensing"} and store it in the `increase`{:class="block3variables"} variable like so:

```blocks3
    اسأل [كم عدد الخطوات التي يجب عليَّ ان انمو بها؟] وانتظر
+    اجعل [زيادة] مساوياً (الإجابة)
```

\--- /task \---

\--- task \---

Now, do the same thing with `degrees`{:class="block3variables"}, asking `How many degrees should I turn?`{:class="block3sensing"} and storing the value of `answer`{:class="block3sensing"} in `degrees`{:class="block3variables"}:

```blocks3
    اجعل [زيادة] مساوياً (الإجابة)
+    اسال [كم درجة يجب علي ان استدير؟] وانتظر
+    اجعل [درجات] مساوياً (الإجابة)
```

\--- /task \---

\--- task \---

Check your program now looks like the one below, and run it a few times with different numbers. Write down the answers that make the coolest pictures. You’ll need them in a later step!

```blocks3
    عند نقر العلم الاخضر
    اجعل [خطوات] مساويا [0]
    اسال [كم عدد الخطوات التي يجب علي أن أنمو بها؟] وانتظر
    اجعل [زيادة v] مساوياً (الإجابة)
    اسال [كم درجة يجب ان استدير؟] وانتظر
    اجعل [درجات] مساوياً (الإجابة)
    ارفع القلم
    اختف
    امسح الكل
    اذهب إلى الموضع x: (0) y: (0)
    اجعل لون القلم مساوياً [#4a6cd4]
    أنزل القلم
    كرر حتى <touching [edge v] ?> 
        تحرك (خطوات) خطوة
        استدر باتجاه عقارب الساعة (درجات) درجة
        غير [درجات] بمقدار (زيادة)
    النهاية
```

\--- /task \---