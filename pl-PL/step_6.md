## Dodawanie wyniku

Uczyńmy rzeczy bardziej interesującymi, śledząc wynik.

--- task ---

Aby śledzić wynik gracza, potrzebujesz miejsca na jego umieszczenie. Utwórz nową `zmienną`{:class="block3variables"} nazwaną `wynik`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Gdy rozpoczyna się nowa gra (klikając flagę), powinieneś ustawić wynik gracza na 0. Dodaj ten kod na górze kodu balonu, `kiedy kliknięto zieloną flagę`{:class="block3events"}:

![duszek balonu](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [wynik v] to [0]
show
switch costume to (balon v)
```

--- /task ---

--- task ---

Ilekroć balon pęknie, musisz dodać 1 do wyniku:

![duszek balonu](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (przebity v)
start sound (pop v)
wait (0.3) seconds
+change [wynik v] by (1)
hide
```

--- /task ---

--- task ---

Uruchom ponownie swój program i kliknij balon. Czy twój wynik się zmienia?

--- /task ---

