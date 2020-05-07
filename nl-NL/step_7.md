## Veel ballonnen

1 ballon laten knallen is niet echt een spel, dus laten we er nog veel meer aan toevoegen!

Een eenvoudige manier om veel ballonnen te krijgen, is door met de rechtermuisknop op de ballonsprite te klikken en op **dupliceren** te klikken. Dit is oké als je er maar een paar wilt, maar wat als je er 20 nodig hebt? of 100? Ga je echt zo vaak op **dupliceren** klikken?

Een veel betere manier om veel ballonnen te krijgen, is door de ballonsprite _te klonen_.

--- task ---

Sleep je ballon `wanneer er op de groene vlag wordt geklikt`{:class="block3events"} code naar een nieuwe `wanneer ik als kloon start`{:class="block3control"} besturenblok.

![ballon sprite](images/balloon-sprite.png)

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

Voeg code toe om 20 ballonklonen te maken aan de `wanneer op de groene vlag wordt geklikt`{:class="block3events"} code.

![ballon sprite](images/balloon-sprite.png)

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

Je moet ook het `verdwijn`{:class="block3looks"} blok in het ballon-klikkende script vervangen door een `verwijder deze kloon`{:class="block3control"} blok.

![ballon sprite](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (uitbarsting v)
start sound (pop v)
wait (0.3) seconds
change [score v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Test je project! Wanneer je nu op de vlag klikt, verbergt je hoofdballon-sprite zich en kloont zichzelf vervolgens 20 keer. Wanneer elk van deze 20 klonen wordt gestart, stuiteren ze elk willekeurig rond over het scherm, net als voorheen. Kijk of je de 20 ballonnen kunt laten knallen!

--- /task ---

