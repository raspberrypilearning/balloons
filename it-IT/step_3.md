## Palloncini imprevedibili

--- task ---

Con il codice che hai ora, il tuo palloncino inizierà sempre dallo stesso punto e farà sempre lo stesso percorso.

Fai clic più volte sulla bandiera per avviare il programma e vedrai che si comporta sempre allo stesso modo.

--- /task ---

--- task ---

Invece di usare tutte le volte le stesse coordinate x e y, puoi lasciare che Scratch scelga un `numero a caso` {: class = "blockoperators"}. Change your balloon's code, so that it looks like this:

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

If you click the green flag a few times, you should notice that your balloon starts in a different place each time.

--- /task ---

--- task ---

You could even use a random number to choose a random balloon colour each time:

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

