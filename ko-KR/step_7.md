## 많은 풍선들

1개의 풍선은 게임에서 충분하지 않습니다. 그러니 더 많이 추가해 봅시다!

많은 풍선들을 넣기 위한 한 가지 간단한 방법은, 풍선 스프라이트를 우클릭하여 **복사**를 클릭하는 것입니다. 이 방법은 몇 개만 원할 때는 괜찮습니다. 하지만 만약 20개가 필요하다면요? 또는 100개가 필요하면요? 정말 **복사**를 그렇게 많이 클릭할 것인가요?

많은 풍선을 얻기 위한 훨씬 더 나은 방법은 풍선 스프라이트를 _복제_하는 것입니다.

--- task ---

새로운 `복제되었을 때`{:class="block3control"} 컨트롤 블록에 풍선의 `깃발을 클릭했을 때`{:class="block3events"} 코드를 드래그하세요.

![풍선 스프라이트](images/balloon-sprite.png)

```blocks3
when flag clicked
set [점수 v] to [0]
-show
-switch costume to (풍선1-가 v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end

+when I start as a clone
show
switch costume to (풍선1-가 v)
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

20개의 풍선 복제본을 만들기 위해 `깃발을 클릭했을 때`{:class="block3events"} 코드에 아래의 코드를 추가하세요.

![풍선 스프라이트](images/balloon-sprite.png)

```blocks3
when flag clicked
set [점수 v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

당신은 또한 풍선 클릭 스크립트에서 `숨기기`{:class="block3looks"} 블럭을 `이 복제본 삭제하기`{:class="block3control"} 블럭으로 바꿔야 할 것입니다.

![풍선 스프라이트](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (터뜨림 v)
start sound (pop v)
wait (0.3) seconds
change [점수 v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

프로젝트를 테스트해 보세요! 이제 깃발을 클릭하면, 당신의 기존 풍선 스프라이트는 숨겨지고 그것이 스스로를 20번 복제할 것입니다. 20개의 복제본이 출발하면, 그것들은 각각 화면을 튕겨다닐 것입니다. 원래 그랬던 것처럼요. 당신이 20개의 풍선을 터뜨릴 수 있는지 확인해 보세요!

--- /task ---

