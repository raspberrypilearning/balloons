## Añadir una puntuación

Vamos a hacer las cosas más interesantes añadiendo una puntuación.

--- task ---

Para mantener el puntaje del jugador, necesitas un lugar donde colocarlo. Crear una nueva `variable`{:class="block3variables"} llamada `puntaje`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Cuando se inicia un nuevo juego (haciendo clic en la bandera), debes establecer la puntuación del jugador en 0. Agrega este código a la parte superior del código del globo `cuando hagas clic en la bandera`{:class="block3events"}:

![objeto globo](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [puntaje v] to [0]
show
switch costume to (globo1-a v)
```

--- /task ---

--- task ---

Cada vez que explota un globo, debes agregar 1 a la puntuación:

![objeto globo](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (estallar v)
start sound (pop v)
wait (0.3) seconds
+change [puntaje v] by (1)
hide
```

--- /task ---

--- task ---

Ejecuta su programa nuevamente y haz clic en el globo. ¿Tu puntaje cambia?

--- /task ---

