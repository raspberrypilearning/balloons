## Een score toevoegen

Laten we het interessanter maken door de score bij te houden.

--- task ---

Om de score van de speler bij te houden, heb je een plek nodig om deze te plaatsen. Maak een nieuwe `variabele`{:class="block3variables"} genaamd `score`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Wanneer een nieuw spel wordt gestart (door op de vlag te klikken), moet je de score van de speler op 0 zetten. Voeg deze code toe aan de bovenkant van de `wanneer er op de groene vlag wordt geklikt`{:class="block3events"}-code van de ballon:

![ballon sprite](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

Telkens wanneer een ballon ploft, moet je 1 toevoegen aan de score:

![ballon sprite](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (uitbarsting v)
start sound (pop v)
wait (0.3) seconds
+change [score v] by (1)
hide
```

--- /task ---

--- task ---

Voer je programma opnieuw uit en klik op de ballon. Verandert je score?

--- /task ---

