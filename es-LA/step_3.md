## Globos al azar

--- task ---

Con el código que tienes ahora, tu globo siempre comenzará en el mismo lugar y se moverá en el mismo camino.

Haz clic en la bandera varias veces para iniciar tu programa, y verás que siempre es igual.

--- /task ---

--- task ---

En lugar de usar la misma posición x e y cada vez, puedes dejar que Scratch `elija un número aleatorio`{:class="blockoperators"} en su lugar. Cambia el código de tu globo para que se vea así:

![objeto globo](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Si haces clic en la bandera verde varias veces, deberías notar que tu globo comienza en un lugar diferente cada vez.

--- /task ---

--- task ---

Incluso podrías usar un número aleatorio para elegir un color de globo aleatorio cada vez:

![objeto globo rojo](images/balloons-colour.png)

--- hints ---


--- hint ---

`Cambiar el efecto de color por`{:class="block3looks"} por un `número aleatorio`{:class="block3operators"} cuando `se hace clic en la bandera verde`{:class="block3events"}.

--- /hint ---

--- hint ---

Tendrás que añadir estos bloques a tu código.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Tu código debería verse así:

![objeto globo](images/balloon-sprite.png)

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

¿Qué pasa si este código se coloca al comienzo de tu programa? ¿Pasa algo diferente si colocas este código _dentro_ del loop `para siempre`{:class="block3control"}? ¿Cuál prefieres?

