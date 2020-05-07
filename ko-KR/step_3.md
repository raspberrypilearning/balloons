## 무작위의 풍선들

--- task ---

지금 가진 코드로는, 당신의 풍선은 항상 같은 자리에서 출발하여 같은 경로를 돌아다닐 것입니다.

프로그램을 실행시키기 위해 깃발을 몇 번 클릭해보세요. 그럼 매번 똑같다는 것을 발견할 것입니다.

--- /task ---

--- task ---

같은 x좌표와 y좌표를 매번 사용하는 대신, 스크래치가 `무작위 위치(으)로 이동하기`{:class="blockoperators"}하도록 할 수 있습니다. 풍선의 코드를 변경하세요. 즉, 이런식으로요:

![풍선 스프라이트](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

초록색 깃발을 몇 번 눌러본다면, 당신은 풍선이 매번 다른 위치에서 출발한다는 것을 알아차릴 수 있습니다.

--- /task ---

--- task ---

당신은 또한 난수를 사용하여 풍선의 색깔을 매번 무작위로 지정할 수 있습니다:

![빨간 풍선 스프라이트](images/balloons-colour.png)

--- hints ---


--- hint ---

`초록색  깃발을 클릭했을 때`{:class="block3events"} `난수`{:class="block3operators"}만큼  `색깔 효과를 바꾸기`{:class="block3looks"}.

--- /hint ---

--- hint ---

당신은 이 블록들을 코드에 추가해야할 것입니다.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

다음과 같은 코드가 될 것입니다:

![풍선 스프라이트](images/balloon-sprite.png)

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

만약 이 코드가 프로그램의 시작점에 놓인다면 어떻게 될까요? `무한 반복하기`{:class="block3control"} 루프 _안에_ 코드를 넣는 것과 다른 것이 있을까요? 무엇을 선호하나요?

