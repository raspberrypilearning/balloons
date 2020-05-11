## स्कोर (score) जोड़ना

चलिए स्कोर जोड़ कर चीजों को और अधिक रोचक बनाएं!

--- task ---

खिलाड़ी के स्कोर (score) को बनाने के लिए आपको इसे लगाने के लिए जगह चाहिए। एक नया `variable`{:class="block3variables"} बनाइये जिसका नाम `score`{:class="block3variables"} होगा ।

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

जब एक नया गेम शुरू किया जाता है (हरे झंडे को क्लिक करके) तो आपको खिलाड़ी का स्कोर 0 पर सेट करना चाहिए। इस कोड को अपने गुब्बारों `when flag clicked`{:class="block3events"} कोड के ऊपर जोड़ें:

![balloon sprite](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

जब भी एक गुब्बारा फूटता है तो आपको स्कोर में 1 जोड़ने की आवश्यकता होगी:

![balloon sprite](images/balloon-sprite.png)

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

अपना प्रोग्राम फिर से चलाएं और गुब्बारे पर क्लिक करें। क्या आपका स्कोर बदलता है?

--- /task ---

