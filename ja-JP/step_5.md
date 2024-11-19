## 停止してシャッフル

これまでのところ素晴らしい仕事です! 再生するメロディーを選択し、 `A` と `B` ボタンでトラックをスキップするようにプログラムしました。 曲の再生を停止したい場合はどうなりますか?

このステップでは、`ゆさぶられたとき`{:class="microbitinput"} ジェスチャで を使用して、曲の再生を停止します。

### 振って止める

--- task ---

`入力`{:class="microbitinput"} メニューから、 `ゆさぶられたとき`{:class="microbitinput"} ブロックをドラッグし、コード エディター パネルに配置します。

```microbit
input.onGesture(Gesture.Shake, function () {

})
```

--- /task ---

--- task ---

`論理`{:class="microbitlogic"} メニューから、 `もし...でなけらば`{:class="microbitlogic"} ブロックをドラッグし、 `ゆさぶられたとき`{:class="microbitinput"} ブロック内に配置します。

```microbit
input.onGesture(Gesture.Shake, function () {
    if (true) {

    } else {

    }
})
```

--- /task ---

--- task ---

`論理`{:class="microbitlogic"} メニューをもう一度クリックし、くらべる `0 = 0`{:class="microbitlogic"} ブロックをドラッグします。

それを `もし...でなければ`{:class="microbitlogic"} ブロックの `真` 部分内に配置します。

--- /task ---

--- task ---

くらべるブロックの `=` の横にある矢印をクリックします。

等しくないを意味する`≠` 記号を選択します。

```microbit
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

`変数`{:class="microbitvariables"} メニューから、 `tune`{:class="microbitvariables"} 変数ブロックをドラッグします。

それを `0 ≠ 0`{:class="microbitlogic"} ブロックの最初の `0` に配置します。

```microbit
input.onGesture(Gesture.Shake, function () {
    let tune = 0
    if (tune != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

`音楽`{:class="microbitmusic"} ブロックメニューから、 `すべての音を停止する`{:class="microbitmusic"} ブロックをドラッグします。

それを `もし...でなければ`{:class="microbitlogic"} ブロックの `もし` 部分内に配置します。

```microbit
input.onGesture(Gesture.Shake, function () {
    let tune = 0
    if (tune != 0) {
        music.stopAllSounds()
    } else {

    }
})
```

--- /task ---

--- task ---

`変数`{:class="microbitvariables"} メニューをクリックし、 `変数[tune] を 0 にする`{:class="microbitvariables"} ブロックをドラッグします。

`すべての音を停止する`{:class="microbitmusic"} ブロックの下に配置します。

```microbit
let tune = 0
input.onGesture(Gesture.Shake, function () {
    if (tune != 0) {
        music.stopAllSounds()
        tune = 0
    } else {

    }
})
```

--- /task ---

これで、メロディーの再生中に micro:bit を振るとメロディーの再生が停止します。

### もう一度振ってシャッフル

ここで、micro:bit が選択したメロディーからランダムにメロディーを再生するように条件を追加します。 これは音楽プレーヤーアプリのシャッフル機能に似ています。

--- task ---

`変数`{:class="microbitvariables"} ブロックメニューをクリックし、 `変数[tune] を 0 にする`{:class="microbitvariables"} ブロックをドラッグします。

それを `もし...でなければ`{:class="microbitlogic"} ブロックの `でなければ` 部分内に配置します。

```microbit
let tune = 0
input.onGesture(Gesture.Shake, function () {
    if (tune != 0) {
        music.stopAllSounds()
        tune = 0
    } else {
        tune = 0
    }
})
```

--- /task ---

--- task ---

`計算`{:class="microbitmath"} メニューから、 `...から...までの乱数`{:class="microbitmath"} ブロックをドラッグします。

それを `変数[tune]を0にする`{:class="microbitvariables"} ブロックの `0` の部分内に配置します。

```microbit
let tune = 0
input.onGesture(Gesture.Shake, function () {
    if (tune != 0) {
        music.stopAllSounds()
        tune = 0
    } else {
        tune = randint(0, 10)
    }
})
```

--- /task ---

ランダム ブロックの範囲は現在 `0 から 10`に設定されていますが、メロディーは `1 から 4`に設定されています。

この範囲を一致させるには更新する必要があります。

--- task ---

`...から...までの乱数`{:class="microbitmath"} ブロックの `0` の部分を `1`に変更します。

`...から...までの乱数`{:class="microbitmath"} ブロックの `10` の部分を `4`に変更します。

--- /task ---

コードは以下のようになります：

```microbit
let tune = 0
input.onGesture(Gesture.Shake, function () {
    if (tune != 0) {
        music.stopAllSounds()
        tune = 0
    } else {
        tune = randint(1, 4)
    }
})
```

--- task ---

コード エディター パネルでコード ブロックを変更すると、シミュレーターが再起動します。

**テスト**

プログラムを実行すると、micro:bit を振ることで停止したりシャッフルしたりできるようになります。

--- /task ---

--- task ---

プログラムをmicro:bitにダウンロードしましょう！

--- /task ---

[[[download-to-microbit]]]

よくできました！ これで完全に機能する音楽プレーヤーが完成しました。

次に、学んだ内容を確認します。