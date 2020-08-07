## Muchos globos

Hacer estallar 1 globo no es un gran juego, ¡así que agreguemos mucho más!

Una forma sencilla de obtener muchos globos es simplemente hacer clic derecho en el objeto globo y hacer clic en ** duplicar **. Esto está bien si solo quieres unos pocos, pero ¿qué pasa si necesitas 20? o 100? ¿Realmente vas a hacer clic en ** duplicar ** tantas veces?

Una forma mucho mejor de conseguir muchos globos _es clonar_ el objeto globo.

--- task ---

Arrastra el código de tu globo `cuando hagas clic en la bandera`{:class="block3events"} a un nuevo bloque de control `cuando empiezo como clon`{:class="block3control"}.

![objeto globo](images/balloon-sprite.png)

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

Agrega este código al código del globo `cuando hagas clic en la bandera`{:class="block3events"} para crear 20 globos iguales.

![objeto globo](images/balloon-sprite.png)

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

También debes reemplazar el bloque `ocultar`{:class="block3looks"} en la secuencia de comandos de hacer clic al globo con un bloque `eliminar este clon`{:class="block3control"}.

![objeto globo](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (estallar v)
start sound (pop v)
wait (0.3) seconds
change [puntaje v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Prueba tu proyecto! Ahora, cuando se hace clic en la bandera, tu objeto globo principal se ocultará y luego se clonará 20 veces. Cuando se inicia cada uno de estos 20 clones, cada uno de ellos rebota alrededor de la pantalla al azar, tal como lo hicieron antes. ¡Ve si puedes reventar los 20 globos!

--- /task ---

