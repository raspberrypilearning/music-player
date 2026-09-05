
--- question ---

---
legend: Vraag 3 van 3
---

Hier is de code voor het programma voor de muziekspeler.

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

De variabele `deuntje` is momenteel ingesteld op `1`.

Welke melodie wordt afgespeeld als knop `B` wordt ingedrukt?


--- choices ---

- ( ) `wawawawaa`

  --- feedback ---

Niet helemaal. Knop B slaat de volgende track over en voegt een toe aan de variabele waarde, wat betekent dat `deuntje` wordt ingesteld op `2`, die wordt geassocieerd met de `clou` melodie.

  --- /feedback ---

- (x) `clou`

  --- feedback ---

Geweldig! Knop B voegt een toe aan de variabele waarde, wat betekent dat `deuntje` wordt ingesteld op `2`, die wordt geassocieerd met de `clou` melodie.

  --- /feedback ---

- ( ) `dadadum`

  --- feedback ---

Niet helemaal. De variabele waarde is `1` en knop B voegt `1` toe aan de variabele waarde, wat betekent dat de melodie die hoort bij waarde 1 (`dadadum`) niet langer zal spelen.

  --- /feedback ---

--- /choices ---

--- /question ---
