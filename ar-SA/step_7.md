## الكثير من البالونات

فرقعة بالون واحد ليست لعبة، لذا دعنا نضيف المزيد!

إحدى الطرق البسيطة للحصول على الكثير من البالونات هي النقر بزر الماوس الأيمن على كائن بالون والنقر فوق **مضاعفة**. هذا جيد إذا كنت تريد القليل فقط ، ولكن ماذا لو كنت بحاجة إلى 20؟ أو 100؟ هل ستقوم حقاً بالنقر فوق **مضاعفة** مرات عديدة؟

هناك طريقة أفضل للحصول على الكثير من البالونات وهي _ استنساخ _ كائن بالون.

--- task ---

اسحب الكتلة `عند نقر العلم `{:class="block3events"} إلى  كتلة تحكم جديدة `عندما أبدأ كنسخة`{:class="block3control"}.

![كائن بالون](images/balloon-sprite.png)

```blocks3
when flag clicked
set [النتيجة v] to [0]
-show
-switch costume to (بالون١-أ v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end

+when I start as a clone
show
switch costume to (بالون١-أ v)
point in direction (pick random (-90) to (180))
go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
change [color v] effect by (pick random (0) to (200))
forever
    move (1) steps
    if on edge, bounce
end
```

--- /task ---

--- task ---

أضف هذه التعليمة البرمجية لإنشاء ٢٠ نسخة من البالونات في نهاية كود `عند نقر العلم`{:class="block3events"}:.

![كائن بالون](images/balloon-sprite.png)

```blocks3
when flag clicked
set [النتيجة v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

يجب عليك أيضًا استبدال كتلة `إخفاء `{:class="block3looks"}  في البرنامج النصي للنقر عل البالون الى `حذف هذا النسخة `{:class="block3control"}.

![كائن بالون](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
change [النتيجة v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

قم بإختبار مشروعك! الآن عند النقر على العلم، سيتم إخفاء كائن بالون الرئيسي الخاص بك ومن ثم يستنسخ نفسه 20 مرة. عند بدء كل من هذه النسخ العشرين، سيرتد كل منها بشكل عشوائي حول الشاشة، تمامًا كما فعلوا من قبل. انظر ما إذا كان بإمكانك فرقعة 20 بالوناً!

--- /task ---

