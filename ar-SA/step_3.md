## بالونات عشوائية

--- task ---

باستخدام الكود الذي لديك الآن، سيبدأ بالونك دائماً في نفس المكان ويتحرك في نفس المسار.

انقر فوق العلم عدة مرات لبدء برنامجك، وسترى أنه هو نفس البالون في كل مرة.

--- /task ---

--- task ---

بدلاً من استخدام نفس موضع س و ص في كل مرة، يمكنك السماح لـ Scratch `باختيار رقم عشوائي`{:class="blockoperators"} بدلاً من ذلك. قم بتغيير كود بالونك بحيث يبدو كالتالي:

![كائن بالون](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

إذا قمت بالنقر فوق العلم الأخضر عدة مرات، يجب أن تلاحظ أن بالونك يبدأ في مكان مختلف في كل مرة.

--- /task ---

--- task ---

يمكنك حتى استخدام رقم عشوائي لاختيار لون بالون عشوائي في كل مرة:

![كائن بالون احمر](images/balloons-colour.png)

--- hints ---

--- hint ---

` تغيير تأثير اللون `{:class="block3looks"} بـ `رقم عشوائي `{:class="block3operators"} عند `النقر على العلم الاخضر`{:class="block3events"}.

--- /hint ---

--- hint ---

ستحتاج إلى إضافة هذه الكتل للكود الخاصة بك.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

يجب أن تبدو التعليمات البرمجية خاصتك بالشكل التالي:

![كائن بالون](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    change [colour v] effect by (pick random (0) to (200))
    forever
        move (1) steps
        if on edge, bounce
    end
```

--- /hint ---


--- /hints ---

--- /task ---

ماذا يحدث إذا تم وضع هذا الكود في بداية برنامجك؟ هل يحدث أي شيء مختلف إذا قمت بوضع هذا الكود _ في داخل _ حلقة `كرر باستمرار `{:class="block3control"}؟ أى واحدة تفضل؟

