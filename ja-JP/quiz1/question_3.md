
--- question ---

---
legend: 質問3/3
---

以下は音楽プレーヤー プログラムのコードです。

```microbit
input.onButtonPressed(Button.A, function () {
    music.stopAllSounds()
    tune += -1
    if (tune < 1) {
        tune = 4
    }
})
input.onButtonPressed(Button.B, function () {
    music.stopAllSounds()
    tune += 1
    if (tune > 4) {
        tune = 1
    }
})
input.onGesture(Gesture.Shake, function () {
    if (tune != 0) {
        music.stopAllSounds()
        tune = 0
    } else {
        tune = randint(1, 4)
    }
})
let tune = 0
tune = 1
basic.forever(function () {
    if (tune == 1) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (tune == 2) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Punchline), music.PlaybackMode.UntilDone)
    } else if (tune == 3) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.JumpDown), music.PlaybackMode.UntilDone)
    } else if (tune == 4) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Wawawawaa), music.PlaybackMode.UntilDone)
    }
    basic.pause(200)
})
```

変数`tune` は現在 `1`に設定されています。

ボタン `B` を押すとどのメロディーが再生されますか?


--- choices ---

- ( ) `wawawawaa`

  --- feedback ---

不正解です。 ボタン B はトラックを先にスキップし、変数値に 1 を追加します。つまり、 `tune` は `2`に設定され、これは `ちゃんちゃん♩` のメロディーに関連付けられます。

  --- /feedback ---

- (x) `ちゃんちゃん♩`

  --- feedback ---

素晴らしい！ ボタン B を押すと変数値に 1 を追加します。つまり、 `tune` は `2`に設定され、これは `ちゃんちゃん♩` のメロディーに関連付けられます。

  --- /feedback ---

- ( ) `ダダダム`

  --- feedback ---

不正解です。 変数値は `1` であり、ボタン B は変数値に `1` を追加します。つまり、値 1 (`ダダダム`) に関連付けられたメロディーは再生されなくなります。

  --- /feedback ---

--- /choices ---

--- /question ---
