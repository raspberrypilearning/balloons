## Palloncini imprevedibili

--- task ---

Con il codice che hai ora, il tuo palloncino inizierà sempre dallo stesso punto e farà sempre lo stesso percorso.

Fai clic più volte sulla bandiera per avviare il programma e vedrai che si comporta sempre allo stesso modo.

--- /task ---

--- task ---

Invece di usare tutte le volte le stesse coordinate x e y, puoi lasciare che Scratch scelga un `numero a caso`{:class="blockoperators"}. Modifica il codice del tuo palloncino in modo che assomigli a questo:

![sprite palloncino](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Se fai clic sulla bandiera verde diverse volte, dovresti notare che il palloncino inizia ogni volta in un punto diverso.

--- /task ---

--- task ---

Puoi anche usare un numero casuale per scegliere ogni volta un colore a caso per il palloncino:

![sprite palloncino rosso](images/balloons-colour.png)

--- hints ---

--- hint ---

`cambia effetto colore di`{:class="block3looks"} con un `numero a caso`{:class="block3operators"} quando si fa clic sulla `bandiera verde`{:class="block3events"}.

--- /hint ---

--- hint ---

Dovrai aggiungere questi blocchi al tuo codice.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Il tuo codice dovrebbe assomigliare a questo:

![sprite palloncino](images/balloon-sprite.png)

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

Cosa succede se mettiamo questo codice all'inizio del programma? Succede qualcosa di diverso se lo inseriamo _dentro_ il ciclo `per sempre`{:class="block3control"}? Quale preferisci?

