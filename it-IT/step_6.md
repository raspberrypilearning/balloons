## Aggiungere un punteggio

Rendiamo il gioco più interessante tenendo il punteggio.

--- task ---

Per mantenere il punteggio del giocatore, hai bisogno di un posto dove metterlo. Crea una nuova `variabile`{:class="block3variables"} chiamata `punti`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Quando viene avviato un nuovo gioco (facendo clic sulla bandiera), bisogna azzerare il punteggio del giocatore. Aggiungi questo codice in cima al blocco `quando si clicca su bandiera`{:class="block3events"} del palloncino:

![sprite palloncino](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

Quando si fa scoppiare un palloncino, bisogna aggiungere 1 al punteggio:

![sprite palloncino](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
+change [score v] by (1)
hide
```

--- /task ---

--- task ---

Rilancia il programma e fai clic sul palloncino. Il tuo punteggio cambia?

--- /task ---

