
--- question ---

---
legend: Question 3 sur 3
---

Voici le code du programme du lecteur de musique.

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

La variable `musique` est actuellement définie sur `1`.

Quelle mélodie sera jouée lorsque le bouton `B` est pressé ?


--- choices ---

- ( ) `wawawawaa`

  --- feedback ---

Pas tout à fait. Le bouton B permet d'avancer d'une piste et d'ajouter un à la valeur de la variable, ce qui signifie que `musique` sera défini sur `2`, qui est associé à la mélodie `punchline`.

  --- /feedback ---

- (x) `punchline`

  --- feedback ---

Super ! Appuyer sur le bouton B ajoutera un à la valeur de la variable, ce qui signifie que `musique` sera défini sur `2`, qui est associé à la mélodie `punchline` .

  --- /feedback ---

- ( ) `dadadum`

  --- feedback ---

Pas tout à fait. La valeur de la variable est `1` et le bouton B ajoute `1` à la valeur de la variable, ce qui signifie que la mélodie associée à la valeur 1 (`dadadum`) ne sera plus jouée.

  --- /feedback ---

--- /choices ---

--- /question ---
