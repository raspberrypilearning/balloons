## Hinzufügen eines Timers

Du kannst das Spiel interessanter machen, indem du deinem Spieler nur 10 Sekunden Zeit gibst, um so viele Luftballons wie möglich platzen zu lassen.

--- task ---

Du kannst eine weitere Variable verwenden, um die verbleibende Zeit zu speichern. Klicke auf die Bühne und füge eine neue Variable `Zeit`{:class="block3variables"} hinzu.

--- /task ---

So sollte der Timer funktionieren:

+ Der Timer sollte bei 10 Sekunden starten;
+ Der Timer sollte jede Sekunde herunterzählen;
+ Das Spiel soll aufhören, wenn der Timer 0 erreicht.

--- task ---

Hier ist der Code, den du der _Bühne_ hinzufügen kannst:

![Luftballon-Sprite](images/stage-sprite.png)

```blocks3
when flag clicked
set [time v] to [10]
repeat until <(time) = [0]>
    wait (1) seconds
    change [time v] by (-1)
end
stop [all v]
```

--- /task ---

--- task ---

Zieh die Anzeige deiner Variablen „Zeit“ auf die rechte Seite der Bühne. Du kannst auch mit der rechten Maustaste auf die Variablenanzeige klicken und "Große Anzeige" auswählen, um die Anzeige der Uhrzeit zu ändern.

![Screenshot](images/balloons-readout.png)

--- /task ---

--- task ---

Teste dein Spiel. Wieviele Punkte schaffst du? Wenn dein Spiel zu einfach ist, kannst du:

+ Dem Spieler weniger Zeit geben;
+ Mehr Luftballons erzeugen;
+ Die Luftballons schneller bewegen;
+ Die Luftballons verkleinern.

Spiele dein Spiel ein paarmal, bis du mit dem Schwierigkeitsgrad zufrieden bist.

--- /task ---

