## Ajouter un score

Rendons les choses plus intéressantes en gardant le score.

--- task ---

Pour conserver le score du joueur, tu as besoin d'un endroit pour le mettre. Crée une nouvelle `variable`{:class="block3variables"} appelée `score`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Lorsqu'une nouvelle partie démarre (en cliquant sur le drapeau), tu dois définir le score du joueur sur 0. Ajoute ce code en haut du code du ballon `quand le drapeau est cliqué`{:class="block3events"} :

![sprite ballon](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

Chaque fois qu'un ballon est éclaté, tu dois ajouter 1 au score :

![sprite ballon](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (éclatement v)
start sound (pop v)
wait (0.3) seconds
+change [score v] by (1)
hide
```

--- /task ---

--- task ---

Exécute à nouveau ton programme et clique sur le ballon. Ton score change-t-il ?

--- /task ---

