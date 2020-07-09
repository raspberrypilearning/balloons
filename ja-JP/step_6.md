## スコアを追加する

スコアをつけてもっと面白くしましょう！

--- task ---

プレーヤーのスコアをつけるには、それを置く場所が必要です。 `スコア`{:class="block3variables"}という新しい`変数`{:class="block3variables"}を作成します。

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

（旗を押して）新しいゲームを始めるときに、プレーヤーのスコアを0に設定しなければなりません。 風船の`旗が押されたとき`{:class="block3events"}コードの最初の部分にこのコードを追加します：

![風船のスプライト](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [スコア v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

風船が割れるたびに、スコアに1を加える必要があります。

![風船のスプライト](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (割れた v)
start sound (pop v)
wait (0.3) seconds
+change [スコア v] by (1)
hide
```

--- /task ---

--- task ---

プログラムを再度実行し、風船をクリックします。 スコアは変わりましたか？

--- /task ---

