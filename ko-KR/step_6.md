## 점수 추가하기

점수를 기록해서 좀 더 재밌게 만들어 봅시다.

--- task ---

점수를 기록하기 위해, 이를 적을 공간이 필요합니다. 새로운 `변수`{:class="block3variables"}를 생성하고, `점수`{:class="block3variables"}라는 이름을 붙이세요.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

(깃발을 클릭하여) 새로 게임이 시작됐을 때, 플레이어의 점수를 0으로 맞춰야 합니다. 이 코드를 풍선의 `깃발을 클릭했을 때`{:class="block3events"} 코드 가장 위쪽에 추가하세요:

![풍선 스프라이트](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

풍선이 터뜨려질 때마다, 점수에 1씩 추가해야 합니다:

![풍선 스프라이트](images/balloon-sprite.png)

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

프로그램을 다시 실행시킨 뒤 풍선을 클릭해 보세요. 점수가 바뀌나요?

--- /task ---

