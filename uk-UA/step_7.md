## Тьма кульок

Лопання 1 кульки — не дуже цікава гра, тому давай додамо їх набагато більше!

Один зі простих способів отримати велику кількість кульок — просто клікати правою кнопкою мишки на спрайт кульки і вибирати **дублювати**. Це підходить, якщо треба створити лише декілька кульок, але що коли тобі треба 20? Або 100? Чи справді ти хочеш клікати **дублювати** таку велику кількість разів?

Набагато кращий спосіб отримання великої кількості кульок — _клонувати_ спрайт кульки.

--- task ---

Перетягни код кульки із `коли зелений прапор натиснуто`{:class="block3events"} до нового блоку керування `коли я починаю як клон`{:class="block3control"}.

![спрайт кульки](images/balloon-sprite.png)

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

Додай код для створення 20 клонів кульки під `коли зелений прапор натиснуто`{:class="block3events"}.

![спрайт кульки](images/balloon-sprite.png)

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

Також ти маєш замінити блок `сховати`{:class="block3looks"} в скрипті, що обробляє клацання по кульці, на блок `видалити цей клон`{:class="block3control"}.

![спрайт кульки](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
change [score v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Перевір свій проєкт! Тепер, коли прапор натиснуто, твій головний спрайт кульки ховається і клонує себе 20 разів. Коли кожен із цих 20 клонів стартує, він рухається випадковим чином по екрану, як це робила єдина кулька раніше. Побачимо, чи зможеш ти лопнути всі 20 кульок!

--- /task ---

