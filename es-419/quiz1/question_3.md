
--- question ---

---
legend: Pregunta 3 de 3
---

Aquí está el código para el programa reproductor de música.

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

La variable de melodía `` está establecida actualmente en `1`.

¿Qué melodía se reproducirá cuando se presione el botón `B`?


--- choices ---

- ( ) `wawawawaa`

  --- feedback ---

No exactamente. El botón B salta la pista hacia adelante y añadirá uno al valor de la variable, lo que significa que `tunada` se establecerá en `2`, que está asociada con la melodía `de punzonado`.

  --- /feedback ---

- (x) `remate`

  --- feedback ---

¡Genial! Al presionar el botón B se agregará uno al valor de la variable, lo que significa que la melodía `` se establecerá en `2`, que está asociada con la melodía `punchline`.

  --- /feedback ---

- ( ) `dadadum`

  --- feedback ---

No exactamente. El valor de la variable es `1` y el botón B añade `1` al valor de la variable. significa que la melodia asociada con el valor 1 (`dadadum`) dejará de jugar.

  --- /feedback ---

--- /choices ---

--- /question ---
