## Adding a score

Let's make things more interesting by keeping score.

--- task ---

To keep the player's score, you need a place to put it. Create a new `variable`{:class="blockdata"} called `score`{:class="blockdata"}.

[[[generic-scratch-add-variable]]]

--- /task ---

--- task ---

When a new game is started (by clicking the flag), you should set the player's score to 0. Add this code to the top of the balloon's `when flag clicked`{:class="blockevents"} code:

```blocks
when flag clicked
+ set [score v] to [0]
show
switch costume to [balloon1-a v]
```

--- /task ---

--- task ---

Whenever a balloon is popped, you need to add 1 to the score:

```blocks
when this sprite clicked
switch costume to [burst v]
play sound [pop v]
wait (0.3) secs
+change [score v] by (1)
hide
```

--- /task ---

--- task ---

Run your program again and click the balloon. Does your score change?

--- /task ---

