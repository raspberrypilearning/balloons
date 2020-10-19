## Losowe balony

--- task ---

Dzięki kodowi, który masz teraz, twój balon zawsze zacznie w tym samym miejscu i będzie poruszać się tą samą ścieżką.

Kliknij flagę kilka razy, aby uruchomić program, a zobaczysz, że za każdym razem jest taki sam.

--- /task ---

--- task ---

Zamiast używać tej samej pozycji x i y za każdym razem, możesz pozwolić Scratch użyć bloku `losuj liczbę`{:class="blockoperators"}. Zmień kod balonu, aby wyglądał następująco:

![duszek balonu](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Jeśli klikniesz zieloną flagę kilka razy, zauważysz, że twój balon za każdym razem zaczyna w innym miejscu.

--- /task ---

--- task ---

Możesz nawet użyć losowej liczby, aby wybrać losowy kolor balonu za każdym razem:

![czerwony duszek balonu](images/balloons-colour.png)

--- hints ---


--- hint ---

`Zmień efekt kolor o`{:class="block3looks"} `losuj liczbę`{:class="block3operators"} `kiedy kliknięto zieloną flagę`{:class="block3events"}.

--- /hint ---

--- hint ---

Musisz dodać te bloki do swojego kodu.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Twój kod powinien wyglądać tak:

![duszek balonu](images/balloon-sprite.png)

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

Co się stanie, jeśli ten kod zostanie umieszczony na początku programu? Czy coś innego się wydarzy, jeśli umieścisz ten kod _w środku_ pętli `zawsze`{:class="block3control"}? Który wolisz?

