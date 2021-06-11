## Ballons aléatoires

--- task ---

Avec le code que tu as maintenant, ton ballon commencera toujours au même endroit et se déplacera dans la même direction.

Clique sur le drapeau plusieurs fois pour démarrer ton programme, et tu verras que c'est la même chose à chaque fois.

--- /task ---

--- task ---

Au lieu d'utiliser la même position x et y à chaque fois, tu peux laisser Scratch `choisir un nombre aléatoire`{:class="blockoperators"} à la place. Modifie le code de ton ballon pour qu'il ressemble à ceci :

![sprite ballon](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Si tu cliques plusieurs fois sur le drapeau vert, tu devrais remarquer que ton ballon démarre à un endroit différent à chaque fois.

--- /task ---

--- task ---

Tu peux même utiliser un nombre aléatoire pour choisir une couleur de ballon aléatoire à chaque fois :

![sprite ballon rouge](images/balloons-colour.png)

--- hints ---

--- hint ---

`Ajoute à l'effet couleur`{:class="block3looks"} un `nombre aléatoire`{:class="block3operators"} `quand le drapeau vert est cliqué`{:class="block3events"}.

--- /hint ---

--- hint ---

Tu devras ajouter ces blocs à ton code.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Your code should look like this:

![sprite ballon](images/balloon-sprite.png)

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

Que se passe-t-il si ce code est mis au début de ton programme ? Est-ce que quelque chose de différent se produit si tu mets ce code _à l'intérieur_ d'une boucle `répéter indéfiniment`{:class="block3control"} ? Lequel préfères-tu ?
