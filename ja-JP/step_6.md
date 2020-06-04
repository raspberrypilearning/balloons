## スコアを追加する

スコアをつけてもっと面白くしましょう！

--- task ---

プレーヤーのスコアを保持するには、それを置く場所が必要です。 `スコア`{:class="block3variables"}という新しい`変数`{:class="block3variables"}を作成します。

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

（旗を押して）新しいゲームが始まるときに、プレーヤーのスコアを0に設定しなければなりません。 Add this code to the top of the balloon's `when flag clicked`{:class="block3events"} code:

![balloon sprite](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

Whenever a balloon is popped, you need to add 1 to the score:

![balloon sprite](images/balloon-sprite.png)

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

Run your program again and click the balloon. Does your score change?

--- /task ---

