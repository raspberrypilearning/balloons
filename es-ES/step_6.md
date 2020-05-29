## Añadir una puntuación

Hagamos las cosas más interesantes manteniendo la puntuación.

--- task ---

Para mantener la puntuación del jugador, necesitas un lugar donde colocarlo. Crea una nueva `variable`{:class="block3variables"} llamada `puntos`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Cuando se inicia un nuevo juego (haciendo clic en la bandera), debe establecer la puntuación del jugador a 0. Agrega este código al principio de la secuencia de comandos `cuando haga clic en la bandera`{:class="blockevents"} de tu globo:

![objeto globo](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [puntos v] to [0]
show
switch costume to (globo1-a v)
```

--- /task ---

--- task ---

Cada vez que haces estallar un globo, se debe sumar 1 a la variable puntos:

![objeto globo](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (explotando v)
start sound (pop v)
wait (0.3) seconds
+change [puntos v] by (1)
hide
```

--- /task ---

--- task ---

Ejecuta tu programa nuevamente y haz clic en el globo. ¿Tus puntos cambian?

--- /task ---

