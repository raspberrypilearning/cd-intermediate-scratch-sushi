## اجمل خطوط

الوقت لإضافة الوان! إلى الآن ، الخط الخاص بك هو لون واحد ، ولكن **القلم** لديه كتل يمكن أن تغير لونه. ومع كتلة **المشغل** الصحيحة، يمكنك حتى تغيير اللون عشوائيا!

كتلة تغيير لون **القلم** هي `تغيير لون القلم بمقدار`{:class="block3extensions"}:

```blocks3
    تغيير لون القلم بمقدار (10)
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    كرر حتى<touching [edge v] ?> 
+        تغيير القلم اللون بمقدار (10)
        تحرك (خطوات) خطوة
        استدر باتجاه عقارب الساعة (درجات ::متغير) درجات
        غير [خطوات v] بمقدار (زيادة:: متغير)
    النهاية
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    كرر حتى<touching [edge v] ?> 
+        تغيير القلم اللون بمقدار (عدد عشوائي بين(1) و (100))
        تحرك (خطوات) خطوة
        استدر باتجاه عقارب الساعة (درجات ::متغير) درجات
        غير [خطوات] بمقدار (زيادة:: متغير)
    النهاية
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---