## Beaucoup de ballons

Faire éclater 1 ballon n'est pas vraiment un jeu, alors ajoutons en beaucoup plus !

Une façon simple d'obtenir beaucoup de ballons consiste simplement à cliquer avec le bouton droit sur le sprite de ballon et à cliquer sur **dupliquer**. Ce n'est pas grave si tu n'en veux que quelques-uns, mais qu'en est-il si tu en as besoin de 20 ? ou 100 ? Vas-tu vraiment cliquer sur **dupliquer** autant de fois ?

Une bien meilleure façon d'obtenir beaucoup de ballons est de _cloner_ le sprite de ballon.

--- task ---

Fais glisser le code de ton ballon `quand le drapeau est cliqué`{:class="block3events"} vers un nouveau bloc de contrôle `quand je commence comme un clone`{:class="block3control"}.

![sprite ballon](images/balloon-sprite.png)

```blocks3
when flag clicked
set [score v] to [0]
-show
-switch costume to (balloon1-a v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end

+when I start as a clone
show
switch costume to (balloon1-a v)
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

Ajoute du code pour créer 20 clones de ballons dans le code `quand le drapeau est cliqué`{:class="block3events"}.

![sprite ballon](images/balloon-sprite.png)

```blocks3
when flag clicked
set [score v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

Tu dois également remplacer le bloc `cacher`{:class="block3looks"} dans le script en cliquant sur le ballon avec un bloc `supprimer ce clone`{:class="block3control"}.

![sprite ballon](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (éclatement v)
start sound (pop v)
wait (0.3) seconds
change [score v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Teste ton projet ! Maintenant, quand le drapeau est cliqué, ton sprite de ballon principal se cache et se clone ensuite 20 fois. Lorsque chacun de ces 20 clones est démarré, ils rebondissent chacun au hasard sur l'écran, comme ils le faisaient auparavant. Vois si tu peux faire éclater les 20 ballons !

--- /task ---

