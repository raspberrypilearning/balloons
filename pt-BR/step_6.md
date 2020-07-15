## Adicionando uma pontuação

Vamos tornar as coisas mais interessantes e manter uma pontuação.

--- task ---

Para manter a pontuação do jogador, você precisa de um local para guardá-la. Crie uma nova `variável`{:class="block3variables"} chamada `pontos`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Quando um novo jogo é iniciado (clicando na bandeira), você deve definir a pontuação do jogador como 0. Adicione este código à parte superior do código do balão `quando ⚑ for clicado`{:class="block3events"}:

![ator balão](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [pontos v] to [0]
show
switch costume to (balão1-a v)
```

--- /task ---

--- task ---

Sempre que um balão é estourado, você precisa adicionar 1 à pontuação:

![ator balão](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (estouro v)
start sound (pop v)
wait (0.3) seconds
+change [pontos v] by (1)
hide
```

--- /task ---

--- task ---

Execute seu programa novamente e clique no balão. Sua pontuação muda?

--- /task ---

