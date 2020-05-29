## 很多氣球

射擊一個氣球並不是太有趣,所以讓我們增加更多內容吧!

一個簡單的方法來獲得許多的氣球是右鍵點擊氣球角色然後點擊**複製**。 如果你只想要幾個，這沒關係，但是如果需要20個呢？ 還是100？ 你是否真的要點擊**複製**那麼多次？

一個獲得許多氣球更好的方式是 _複製分身_ 氣球角色。

--- task ---

拖曳你的氣球`當旗子被點擊`{:class="block3events"} 程式碼到新的`當分身產身`{:class="block3control"}控制積木。

![氣球角色](images/balloon-sprite.png)

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

增加一個程式碼來創造20個氣球分身到`當綠旗被點擊`{:class="block3events"} 程式碼。

![氣球角色](images/balloon-sprite.png)

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

你應該在射擊氣球的程式碼中替換 `隱藏`{:class="block3looks"} 積木用`分身刪除`{:class="block3control"} 積木。

![氣球角色](images/balloon-sprite.png)

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

測試你的專案。 現在當旗子被點擊時,你的主要氣球角色會隱藏接著複製它的分身 20次。 當這20個分身被啟動時,他們各自會隨機的在螢幕彈跳,就像之前一樣 。 看看你是否可以射擊20個氣球!

--- /task ---

