## 風船に動きをつける

--- task ---

新しいScratchプロジェクトを開きます。

**オンライン**：[新しいオンラインScratchプロジェクト](http://rpf.io/scratch-new){:target="_blank"}を開きます。

Scratchアカウントをお持ちの場合は**リミックス**をクリックしてコピーを作成できます。

**オフライン**：オフラインエディタで新しいプロジェクトを開きます。

[rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}からScratchオフラインエディタをダウンロードしてインストールできます。

--- /task ---

--- task ---

猫のスプライトを削除します。

--- /task ---

--- task ---

新しい風船のスプライトと、ふさわしいステージの背景（はいけい）を追加します。

![背景と風船のスプライト](images/balloons-balloon.png)

--- /task ---


--- task ---

このコードを風船に追加して、画面の端で跳ね返るようにします：

![風船のスプライト](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(0) y:(0)
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

--- /task ---

--- task ---

風船の動きを確認しましょう。 動きが遅すぎませんか？ もう少し速くするには、コードの数値を変更してください。

--- /task ---

--- task ---

画面の端で跳ね返るときに風船がひっくり返ることにも気づきましたか？

![逆さまの風船](images/balloons-flip.png)

風船はこのように動きません！ これを修正するには、風船のスプライトアイコンをクリックして、向きをクリックします。

「回転しない」アイコンをクリックして、風船がひっくり返らないようにします。

![回転方法の選択](images/balloons-lock-annotated.png)

--- /task ---

--- task ---

プログラムを再度テストして、問題が修正されたかどうかを確認します。

--- /task ---
