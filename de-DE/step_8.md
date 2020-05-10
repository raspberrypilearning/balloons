## Hinzufügen eines Timers

Du kannst das Spiel interessanter machen, indem du deinem Spieler nur 10 Sekunden Zeit gibst, um so viele Luftballons wie möglich platzen zu lassen.

--- task ---

Du kannst eine weitere Variable verwenden, um die verbleibende Zeit zu speichern. Klicke auf die Bühne und füge eine neue Variable `Zeit`{:class="block3variables"} hinzu.

--- /task ---

So sollte der Timer funktionieren:

+ Der Timer sollte bei 10 Sekunden starten;
+ The timer should count down every second;
+ The game should stop when the timer gets to 0.

--- task ---

Here's the code to do this, which you can add to your _stage_:

![balloon sprite](images/stage-sprite.png)

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

Drag your 'time' variable display to the right side of the stage. You can also right-click on the variable display and choose 'large readout' to change how the time is displayed.

![screenshot](images/balloons-readout.png)

--- /task ---

--- task ---

Test your game. How many points can you score? If your game is too easy, you can:

+ Give the player less time;
+ Have more balloons;
+ Make the balloons move faster;
+ Make the balloons smaller.

Play your game a few times until you're happy that it's the right level of difficulty.

--- /task ---

