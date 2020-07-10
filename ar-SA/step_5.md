## اجمل خطوط

الوقت لإضافة الوان! إلى الآن ، الخط الخاص بك هو لون واحد ، ولكن **القلم** لديه كتل يمكن أن تغير لونه. ومع كتلة **المشغل** الصحيحة، يمكنك حتى تغيير اللون عشوائيا!

كتلة تغيير لون **القلم** هي `تغيير لون القلم بمقدار`{:class="block3extensions"}:

```blocks3
    change pen color by (10)
```

--- task ---

اسحب واحدة من تلك الكتل وضعها داخل الحلقة الخاصة بك`كرر حتى`{:class="block3control"}, مثل هذا:

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (10)
        move (خطوات) steps
        turn cw (درجات ::variables) degrees
        change [خطوات v] by (زيادة ::variables)
    end
```

--- /task ---

هذا رائع ، لكن قابل للتنبؤ قليلاً. يمكنك جعله أكثر متعة قليلاً إذا أضفت رقمًا عشوائيًا إليه، بهذا يتغير اللون بشكل عشوائي.

--- task ---

ضع كتلة العدد عشوائي **المشغل**في كتلة `غير القلم اللون بمقدار`{:class="block3extensions"} واختر بعض القيم لتكون بداخلها. أود ان أحاول `1` و `100` للبدأ.

```blocks3
    repeat until <touching [edge v] ?> 
+        change pen color by (pick random (1) to (100))
        move (خطوات) steps
        turn cw (درجات ::variables) degrees
        change [خطوات v] by (زيادة ::variables)
    end
```

--- /task ---

--- task ---

حاول تشغيله مرة أخرى ، وشاهد قوس قزح عشوائي!

--- /task ---