## Tanti palloncini

Far scoppiare un palloncino non è molto divertente, aggiungiamone molti altri!

Per avere facilmente molti palloncini puoi fare clic con il tasto destro del mouse sullo sprite palloncino e fare clic su **duplica**. Questo metodo è comodo se hai bisogno di pochi palloncini, ma se te ne servono 20? O 100? Vuoi davvero fare clic su **duplica** così tante volte?

Un modo migliore per avere molti palloncini è _clonare_ lo sprite palloncino.

--- task ---

Trascina il codice del palloncino che trovi sotto al blocco `quando si clicca su bandiera`{:class="block3events"} sotto un nuovo blocco di controllo `quando vengo clonato`{:class="block3control"}.

![sprite palloncino](images/balloon-sprite.png)

```blocks3
when flag clicked
set [puntaje v] to [0]
-show
-switch costume to (globo1-a v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end

+when I start as a clone
show
switch costume to (globo1-a v)
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

Aggiungi il codice per creare 20 cloni di palloncino sotto al blocco`quando si clicca su bandiera`{:class="block3events"}.

![sprite palloncino](images/balloon-sprite.png)

```blocks3
when flag clicked
set [puntaje v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

Dovresti anche sostituire il blocco `nascondi`{:class="block3looks"} nello script per gestire il clic sul palloncino con il blocco `elimina questo clone`{:class="block3control"}.

![sprite palloncino](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (scoppio v)
start sound (pop v)
wait (0.3) seconds
change [puntaje v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Prova il tuo progetto! Adesso, quando fai clic sulla bandiera, lo sprite del palloncino principale si nasconderà e si clonerà 20 volte. Appena creato, ognuno dei 20 cloni, rimbalza sullo schermo in modo casuale, proprio come prima. Prova a far scoppiare i 20 palloncini!

--- /task ---

