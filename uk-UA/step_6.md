## Додавання рахунку

Давай зробимо гру цікавішою, додавши підрахунок очок.

--- task ---

Щоб зберігати рахунок гравця, тобі потрібне для цього якесь місце. Створи нову `змінну`{:class="block3variables"} з назвою `рахунок`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Коли гра розпочинається (при натисканні прапора), ти маєш обнулити рахунок гравця. Додай наступний код на початку скрипта для кульки під `коли зелений прапор натистнуто`{:class="block3events"}:

![спрайт кульки](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [рахунок v] to [0]
show
switch costume to (рахунок v)
```

--- /task ---

--- task ---

Кожного разу, коли кулька лопається, тобі треба збільшувати рахунок на 1:

![спрайт кульки](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (бабах v)
start sound (pop v)
wait (0.3) seconds
+change [рахунок v] by (1)
hide
```

--- /task ---

--- task ---

Запусти свою програму знову і клацни на кульку. Чи змінюється твій рахунок?

--- /task ---

