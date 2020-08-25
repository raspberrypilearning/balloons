## Zufällige Luftballons

--- task ---

Mit dem Code, den du jetzt hast, startet dein Luftballon immer an derselben Stelle und bewegt sich auf demselben Weg.

Klicke einige Male auf die Fahne, um dein Programm zu starten und du wirst sehen, dass es jedes Mal das Gleiche ist.

--- /task ---

--- task ---

Anstatt jedes Mal dieselbe x- und y-Position zu verwenden, kannst du stattdessen Scratch eine `Zufallszahl von bis`{:class="blockoperators"} auswählen lassen. Ändere den Code deines Luftballons so, dass er folgendermaßen aussieht:

![Luftballon-Sprite](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Wenn du einige Male auf die grüne Fahne klickst, solltest du feststellen, dass dein Luftballon jedes Mal an einer anderen Stelle startet.

--- /task ---

--- task ---

Du kannst auch eine Zufallszahl verwenden, um jedes Mal eine zufällige Ballonfarbe auszuwählen:

![roter Luftballon-Sprite](images/balloons-colour.png)

--- hints ---


--- hint ---

Benutze im `ändere Effekt Farbe um`{:class="block3looks"} Block einen `Zufallszahl von bis`{:class="block3operators"} Block, um die Farbe im `wenn die Fahne angeklickt wird`{:class="block3events"} Skript anzupassen.

--- /hint ---

--- hint ---

Du musst diese Blöcke zu deinem Code hinzufügen.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Dein Code sollte so aussehen:

![Luftballon-Sprite](images/balloon-sprite.png)

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

Was passiert, wenn dieser Code am Anfang deines Programms steht? Passiert etwas anderes, wenn der Code _innerhalb_ der `Endlosschleife`{:class="block3control"} steht? Was bevorzugst du?

