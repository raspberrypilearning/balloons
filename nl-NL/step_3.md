## Willekeurige ballonnen

--- task ---

Met de code die je nu hebt, zal je ballon altijd op dezelfde plek starten en over hetzelfde pad bewegen.

Klik een paar keer op de vlag om je programma te starten en je zult zien dat het elke keer hetzelfde is.

--- /task ---

--- task ---

In plaats van elke keer dezelfde x- en y-positie te gebruiken, kun je Scratch `een willekeurig getal laten kiezen`{:class="blockoperators"} in plaats daarvan. Wijzig de code van je ballon, zodat deze er als volgt uitziet:

![ballon sprite](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Als je een paar keer op de groene vlag klikt, zou je moeten merken dat je ballon elke keer op een andere plaats begint.

--- /task ---

--- task ---

Je kunt zelfs een willekeurig getal gebruiken om elke keer een willekeurige ballonkleur te kiezen:

![rode ballonsprite](images/balloons-colour.png)

--- hints ---

--- hint ---

`Wijzig het kleureffect met`{:class="block3looks"} met een `willekeurig getal`{:class="block3operators"} wanneer op de `groene vlag wordt geklikt`{:class="block3events"}.

--- /hint ---

--- hint ---

Je moet deze blokken toevoegen aan je code.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Je code zou er als volgt uit moeten zien:

![ballon sprite](images/balloon-sprite.png)

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

Wat gebeurt er als deze code aan het begin van je programma wordt gezet? Gebeurt er iets anders als je deze code _binnen_ de `herhaal`{:class="block3control"} lus zet? Wat heb je liever?

