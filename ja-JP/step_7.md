## 風船をたくさんに

1つの風船を割るだけではゲームというほどではないので、もっとたくさんにしましょう！

風船をたくさんにする簡単な方法の1つは、風船のスプライトを右クリックして、**複製**をクリックすることです。 数個だけなら問題ありませんが、20個必要な場合はどうでしょうか？ 100個では？ そんなに何回も**複製**をクリックしますか？

風船をたくさんにするもっと良い方法は、風船のスプライトの_クローンを作る_ことです。

--- task ---

風船の`旗が押されたとき`{:class="block3events"}コードを新しい制御ブロック`クローンされたとき`{:class="block3control"}にドラッグします。

![風船のスプライト](images/balloon-sprite.png)

```blocks3
when flag clicked
set [スコア v] to [0]
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

`旗が押されたとき`{:class="block3events"}コードに風船のクローンを20個作成するコードを追加します。

![風船のスプライト](images/balloon-sprite.png)

```blocks3
when flag clicked
set [スコア v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

また、風船のスプライトが押されたときのスクリプトにある`隠す`{:class="block3looks"}ブロックを、 `このクローンを削除する`{:class="block3control"}ブロックに置き換える必要があります。

![風船のスプライト](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (割れた v)
start sound (pop v)
wait (0.3) seconds
change [スコア v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

プロジェクトをテストしましょう！ 旗が押されると、最初の風船のスプライトが消え、そのクローンが20個作成されます。 これらの20個のクローンがそれぞれ動き始めると、1個の時と同じように、それぞれが画面上でランダムに跳ね返ります。 20個の風船を割ることができるかを確認してください。

--- /task ---

