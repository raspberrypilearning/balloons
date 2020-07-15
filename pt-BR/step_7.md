## Muitos balões

Estourar 1 balão não é muito um jogo, então vamos adicionar muito mais!

Uma maneira simples de obter muitos balões é apenas clicar com o botão direito do mouse no ator balão e clicar em **duplicar**. Isso funciona se você quiser apenas alguns, mas e se precisar de 20? ou 100? Você realmente vai querer clicar em **duplicar** tantas vezes assim?

Uma maneira muito melhor de obter muitos balões é _clonar_ o ator balão.

--- task ---

Arraste o código do seu balão `quando ⚑ for clicado`{:class="block3events"} para um novo bloco de controle `quando eu começar como um clone`{:class="block3control"}.

![ator balão](images/balloon-sprite.png)

```blocks3
when flag clicked
set [pontos v] to [0]
-show
-switch costume to (balão1-a v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end
+when I start as a clone
show
switch costume to (balão1-a v)
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

Adicione código para criar 20 clones de balão no código `quando ⚑ for clicado`{:class="block3events"}.

![ator balão](images/balloon-sprite.png)

```blocks3
when flag clicked
set [pontos v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

Você também deve substituir o bloco `esconda`{:class="block3looks"} no script 'quando este ator for clicado' pelo bloco `apague este clone`{:class="block3control"}.

![ator balão](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (estouro v)
start sound (pop v)
wait (0.3) seconds
change [pontos v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Teste seu projeto! Agora, quando a bandeira é clicada, seu ator balão principal se esconderá e se clonara 20 vezes. Quando cada um desses 20 clones é iniciado, eles saltam aleatoriamente pela tela, exatamente como antes. Veja se você pode estourar os 20 balões!

--- /task ---

