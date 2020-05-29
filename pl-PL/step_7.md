## Dużo balonów

Przebicie 1 balona nie jest dobrą zabawą, więc dodajmy wiele więcej!

Jednym prostym sposobem na uzyskanie wielu balonów jest kliknięcie duszka balonu prawym przyciskiem myszy i kliknięcie **duplikuj**. To jest wystarczające jeżeli chcesz mieć tylko kilka, ale co jeśli chcesz mieć 20? albo 100? Czy naprawdę zamierzasz klikać **duplikuj** tyle razy?

O wiele lepszym sposobem na uzyskanie wielu balonów jest _klonowanie_ duszka balonu.

--- task ---

Przeciągnij kod balonu `kiedy kliknięto flagę`{:class="block3events"} do nowego bloku kontroli `kiedy zaczynam jako klon`{:class="block3control"}.

![duszek balonu](images/balloon-sprite.png)

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

Dodaj ten kod do kodu `kiedy kliknięto zieloną flagę`{:class=„block3events”} aby utworzyć 20 klonów balonu.

![duszek balonu](images/balloon-sprite.png)

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

Powinieneś także zastąpić blok `ukryj`{:class="block3looks"} w skrypcie klikania balonu blokiem `usuń tego klona`{:class="block3control"}.

![duszek balonu](images/balloon-sprite.png)

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

Przetestuj swój projekt! Teraz, gdy flaga zostanie kliknięta, twój główny duszek ukryje się, a następnie sklonuje się 20 razy. Kiedy każdy z tych 20 klonów zostanie uruchomiony, każdy z nich odbije się losowo wokół ekranu, tak jak wcześniej. Sprawdź, czy dasz radę przebić 20 balonów!

--- /task ---

