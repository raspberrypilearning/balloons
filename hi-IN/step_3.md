## इधर-उधर गुब्बारे

--- task ---

अब आपके पास जो कोड है, आपका गुब्बारा हमेशा उसी स्थान पर शुरू होगा और उसी रस्ते में आगे बढ़ेगा।

अपना प्रोग्राम (program) शुरू करने के लिए हरे झंडे को कई बार क्लिक करें और आप देखेंगे कि यह हर बार एक ही तरीके का दिखता है।

--- /task ---

--- task ---

हर बार एक ही X और Y जगह का उपयोग करने के बजाय, आप Scratch `pick a random number`{:class="blockoperators"} करने दे सकते हैं | अपने गुब्बारे का कोड बदलें ताकि वह इस तरह दिखे:

![balloon sprite](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

यदि आप कुछ बार हरे झंडे पर क्लिक करते हैं तो आपको यह दिखना चाहिए कि आपका गुब्बारा हर बार अलग जगह पर शुरू होरहा है।

--- /task ---

--- task ---

आप हर बार एक यादृच्छिक (random) गुब्बारा रंग चुनने के लिए एक यादृच्छिक संख्या का उपयोग कर सकते हैं:

![red balloon sprite](images/balloons-colour.png)

--- hints ---

--- hint ---

`Change the color effect by`{:class="block3looks"} by a `random number`{:class="block3operators"} when the `green flag is clicked`{:class="block3events"}.

--- /hint ---

--- hint ---

You will need to add these blocks to your code.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

You code should look like this:

![balloon sprite](images/balloon-sprite.png)

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

What happens if this code is put at the start of your program? Does anything different happen if you put this code _inside_ the `forever`{:class="block3control"} loop? Which do you prefer?

