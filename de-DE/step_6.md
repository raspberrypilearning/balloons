## Einen Punktestand hinzufügen

Lass uns die Dinge interessanter machen, indem wir Punkte zählen.

--- task ---

Um den Punktestand des Spielers zu verfolgen, benötigst du einen Platz, an dem du sie anzeigen lassen kannst. Erstelle eine neue `Variable`{:class="block3variables"} mit dem Namen `Punktestand`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Wenn ein neues Spiel gestartet wird (durch Klicken auf die grüne Fahne), solltest du den Punktestand des Spielers auf 0 setzen. Fügen diesen Code an den Anfang des `Wenn die Fahne angeklickt wird`{:class="block3events"} -Skripts des Luftballons hinzu:

![Luftballon-Sprite](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [Punktestand v] to [0]
show
switch costume to (Luftballon1-a v)
```

--- /task ---

--- task ---

Immer, wenn ein Ballon platzt, musst du den Punktestand um eins erhöhen:

![Luftballon-Sprite](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (Geplatzt v)
start sound (pop v)
wait (0.3) seconds
+change [Punktestand v] by (1)
hide
```

--- /task ---

--- task ---

Führe dein Programm noch einmal aus und klicke auf den Luftballon. Ändert sich dein Punktestand?

--- /task ---

