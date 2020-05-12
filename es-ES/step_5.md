## Reventando los globos

¡Permitamos que el jugador haga estallar los globos!

--- task ---

Haz clic el objeto globo, y luego haz clic en la pestaña **Disfraces**. Puedes eliminar todos los otros disfraces, dejando solo 1 disfraz de globo. Agrega un traje nuevo haciendo clic en **Pinta** y crea un nuevo disfraz llamado `explotando`.

![disfraz de globo llamado explotando](images/balloons-costume.png)

--- /task ---

--- task ---

Asegúrate de que tu globo cambie al disfraz correcto cuando comience el juego. Tu código debe parecerse a esto:

![objeto globo](images/balloon-sprite.png)

```blocks3
when flag clicked
+switch costume to (balloon1-a v)
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

Para permitir que el jugador explote un globo, agrega este código:

![objeto globo](images/balloon-sprite.png)

```blocks3
    when this sprite clicked
    switch costume to (burst v)
    start sound (pop v)
```

--- /task ---

--- task ---

Prueba tu proyecto. ¿Puedes reventar el globo? ¿Funciona como esperabas?

Deberás mejorar este código, de modo que cuando se haga clic en el globo, muestre el disfraz `explotando` por un corto periodo de tiempo, y luego se oculte.

Puedes hacer que todo esto suceda cambiando el código `cuando se hace clic en el sprite`{:class="block3events"} de tu globo por esto:

![objeto globo](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
+ wait (0.3) seconds
+ hide
```

--- /task ---

--- task ---

Ahora que estás eliminando el globo cuando se hace clic en él, también deberás agregar un bloque `mostrar`{:class="block3looks"} al comienzo del código `cuando se hace clic en la bandera`{:class="block3events"}.

![objeto globo](images/balloon-sprite.png)

```blocks3
when flag clicked
+ show
switch costume to (balloon1-a v)
point in direction (pick random (-90) to (180))
```

--- /task ---

--- task ---

Intenta hacer estallar un globo nuevamente para verificar que funcione correctamente.

--- /task ---
