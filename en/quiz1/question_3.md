
--- question ---

---
legend: Question 3 of 3
---

Here is the code for the music player program.

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

The `tune` variable is currently set to `1`.

Which melody will play when Button `B` is pressed?


--- choices ---

- ( ) `wawawawaa`
  
  --- feedback ---
  
Not quite. Button B skips the track forward and will add one to the variable value, meaning `tune` will be set to `2`, which is associated with the `punchline` melody.

  --- /feedback ---

- (x) `punchline`

  --- feedback ---

Great! Pressing Button B will add one to the variable value, meaning `tune` will be set to `2`, which is associated with the `punchline` melody.

  --- /feedback ---

- ( ) `dadadum`

  --- feedback ---

Not quite. The variable value is `1` and Button B adds `1` to the variable value, meaning the melody associated with value 1 (`dadadum`) will no longer play.

  --- /feedback ---

--- /choices ---

--- /question ---
