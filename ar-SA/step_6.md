## إضافة النتيجة

لنجعل اللعبة أكثر تشويقاً بتسجيل النقاط.

--- task ---

للحفاظ على نتيجة اللاعب، تحتاج إلى مكان لوضعه فيه. `اصنع متغير جديد`{:class="block3variables"} يسمى `النتيجة`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

عند بدء لعبة جديدة (بالضغط على العلم)، يجب عليك ضبط نتيجة اللاعب الى 0. أضف هذه التعليمة البرمجية في نهاية مقطع`عند نقر العلم`{:class="block3events"}:

![كائن بالون](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

كلما يفرقع بالون، تحتاج إلى إضافة 1 إلى النتيجة:

![كائن بالون](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
+change [score v] by (1)
hide
```

--- /task ---

--- task ---

قم بتشغيل البرنامج مرة أخرى وانقر فوق البالون. هل تتغير درجاتك؟

--- /task ---

