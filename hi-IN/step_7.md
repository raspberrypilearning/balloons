## बहुत सारे गुब्बारे

1 गुब्बारा फोड़ना कोई खेल नहीं है तो चलिए और भी बहुत कुछ जोड़ते हैं!

बहुत सारे गुब्बारों को लाने के एक बहुत आसान तरीका है कि आप गुब्बारे के स्प्राइट पर राइट क्लिक (right-click) करके **duplicate** दबा सकते हैं | यह ठीक है यदि आप केवल कुछ गुब्बारे चाहते, लेकिन क्या होगा यदि आपको 20 की आवश्यकता है? या 100? क्या आप सचमुच **duplicate** उतनी बार दबाएंगे?

बहुत सारे गुब्बारे पाने का एक बेहतर तरीका है, गुब्बारा स्प्राइट का _clone_ बनाना।

--- task ---

अपने गुब्बारे के `when flag clicked`{:class="block3events"} कोड को खींचकर इस नए `when I start as a clone`{:class="block3control"} कंट्रोल (control) ब्लॉक में जोड़ें |

![balloon sprite](images/balloon-sprite.png)

```blocks3
when flag clicked
set [score v] to [0]
-show
-switch costume to (balloon1-a v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end

+when I start as a clone
show
switch costume to (balloon1-a v)
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

अपने `when flag clicked`{:class="block3events"} कोड में यह और कोड जोड़ें ताकि आपके गुब्बारों के 20 क्लोन्स (clones) बन जाएं |

![balloon sprite](images/balloon-sprite.png)

```blocks3
when flag clicked
set [score v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

आपको `hide`{:class="block3looks"} ब्लॉक को बदलना पड़ेगा, गुब्बारा क्लिक करने वाली स्क्रिप्ट (script) में `delete this clone`{:class="block3control"} ब्लॉक से |

![balloon sprite](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
change [score v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

अपने प्रोजेक्ट का परीक्षण करें। अब जब हरे झंडे पर क्लिक किया जाएगा, तो आपका मुख्य गुब्बारा स्प्राइट छिप जाएगा और फिर 20 बार क्लोन (clone) बनाएगा। जब यह प्रत्येक 20 क्लोन (clone) बनना शुरू होते है, तो वे स्क्रीन के चारों ओर अनियमित ढंग से उछलेगा जैसा कि पहले किया था। देखें कि क्या आप 20 गुब्बारे को फोड़ सकते हैं!

--- /task ---

