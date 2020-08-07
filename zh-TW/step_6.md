## 增加一個得分

讓我們透過紀錄得分讓遊戲變得更有趣。

--- task ---

你需要放置得分來紀錄玩家的分數。 建立一個新`變數`{:class="block3variables"} 稱為 `得分`{:class="block3variables"}。

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

當開始新遊戲時 (通過點擊旗子)，你應該將玩家的得分設置為0。 把這程式碼增加到氣球程式碼的頂端 `當綠旗被點擊`{:class="block3events"}:

![氣球角色](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [得分 v] to [0]
show
switch costume to (氣球1-a v)
```

--- /task ---

--- task ---

每次氣球被射擊時,你需要在得分中加1:

![氣球角色](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (爆炸 v)
start sound (pop v)
wait (0.3) seconds
+change [得分 v] by (1)
hide
```

--- /task ---

--- task ---

再次執行你的程式然後點擊氣球。 你的分數有改變嗎？

--- /task ---

