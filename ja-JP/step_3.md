## 風船をランダムに

--- task ---

今のコードでは、風船はいつも同じ場所から始まり、同じ道のりで動きます。

旗を何回かクリックしてプログラムを動かすと、毎回同じであることがわかります。

--- /task ---

--- task ---

毎回同じxとyの位置を使う代わりに、Scratchに`乱数`{:class="blockoperators"}を選ばせることができます。 風船のコードを変更して、次のようにします：

![風船のスプライト](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

緑の旗を何回かクリックすると、風船が毎回別の場所から動き始めることがわかります。

--- /task ---

--- task ---

乱数を使って、毎回風船の色をランダムに選ぶこともできます。

![赤い風船のスプライト](images/balloons-colour.png)

--- hints ---

--- hint ---

`緑の旗が押された`{:class="block3events"}とき、`乱数`{:class="block3operators"}で`色の効果を変える`{:class="block3looks"}ようにします。

--- /hint ---

--- hint ---

これらのブロックをコードに追加する必要があります：

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Your code should look like this:

![風船のスプライト](images/balloon-sprite.png)

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

このコードがプログラムの最初に置かれた場合はどうなりますか？ このコードを_ずっと_{:class="block3control"}ループの`内側に`置くと、何か違うことが起こりますか？ どちらがいいですか？
