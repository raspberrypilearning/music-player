
--- question ---

---
legend: Question 3 sur 3
---

Voici le code du programme du lecteur de musique.

```microbit
input.onButtonPressed(Button.A, function () {
    music.stopAllSounds()
    musique += -1
    if (musique < 1) {
        musique = 4
    }
})
input.onButtonPressed(Button.B, function () {
    music.stopAllSounds()
    musique += 1
    if (musique > 4) {
        musique = 1
    }
})
input.onGesture(Gesture.Shake, function () {
    if (musique != 0) {
        music.stopAllSounds()
        musique = 0
    } else {
        musique = randint(1, 4)
    }
})
let musique = 0
musique = 1
basic.forever(function () {
    if (musique == 1) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (musique == 2) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Punchline), music.PlaybackMode.UntilDone)
    } else if (musique == 3) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.JumpDown), music.PlaybackMode.UntilDone)
    } else if (musique == 4) {
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
