## Viele Luftballons

Einen Luftballon platzen zu lassen ist kein tolles Spiel, also lasst uns noch viele mehr hinzufügen!

Eine einfache Möglichkeit, viele Luftballons zu erhalten, ist, mit der rechten Maustaste auf das Luftballon-Sprite zu klicken und auf **Duplizieren** zu klicken. Dies ist in Ordnung, wenn du nur wenige möchtest, aber was ist, wenn du 20 benötigst? oder 100? Möchtest du wirklich so oft auf **Duplizieren** klicken?

Eine viel bessere Möglichkeit, viele Ballons zu erhalten, ist das _Klonen_ des Luftballon-Sprite.

--- task ---

Zieh deinen Luftballon `Wenn die Fahne angeklickt wird` {: class = "block3events"} Code in einen neuen `Wenn ich als Klon enstehe` {: class = "block3control"} Steuerblock.

![Luftballon-Sprite](images/balloon-sprite.png)

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

Füge dem `Wenn die Fahne angeklickt wird` {: class = "block3events"} Block Code hinzu um 20 Luftballon-Klone zu erstellen.

![Luftballon-Sprite](images/balloon-sprite.png)

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

Du solltest auch den `verstecke dich`{: class = "block3looks"} Block im Luftballon-Klick-Skript mit einem `lösche diesen Klon`{: class = "block3control"} Block ersetzen.

![Luftballon-Sprite](images/balloon-sprite.png)

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

Teste dein Projekt! Wenn du jetzt auf die Fahne klickst, wird dein Haupt-Luftballon-Sprite ausgeblendet und es klont sich anschließend 20 Mal. Wenn jeder dieser 20 Klone gestartet wird, springt er wie zufällig über den Bildschirm, so wie er es vorher auch getan hat. Schau, ob du die 20 Luftballons platzen lassen kannst!

--- /task ---

