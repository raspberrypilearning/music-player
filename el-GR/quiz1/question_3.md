
--- question ---

---
legend: Ερώτηση 3 από 3
---

Εδώ είναι ο κώδικας για το πρόγραμμα αναπαραγωγής μουσικής.

```microbit
input.onButtonPressed(Button.A, function () {
    music.stopAllSounds()
    μελωδία += -1
    if (μελωδία < 1) {
        μελωδία = 4
    }
})
input.onButtonPressed(Button.B, function () {
    music.stopAllSounds()
    μελωδία += 1
    if (μελωδία > 4) {
        μελωδία = 1
    }
})
input.onGesture(Gesture.Shake, function () {
    if (μελωδία != 0) {
        music.stopAllSounds()
        μελωδία = 0
    } else {
        μελωδία = randint(1, 4)
    }
})
let μελωδία = 0
μελωδία = 1
basic.forever(function () {
    if (μελωδία == 1) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (μελωδία == 2) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Punchline), music.PlaybackMode.UntilDone)
    } else if (μελωδία == 3) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.JumpDown), music.PlaybackMode.UntilDone)
    } else if (μελωδία == 4) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Wawawawaa), music.PlaybackMode.UntilDone)
    }
    basic.pause(200)
})
```

Η μεταβλητή `μελωδία` έχει οριστεί αυτήν τη στιγμή σε `1`.

Ποια μελωδία θα παίξει όταν πατηθεί το κουμπί `B`;


--- choices ---

- ( ) `wawawawaa`

  --- feedback ---

Όχι ακριβώς. Με το κουμπί Β γίνεται μετάβαση στο επόμενο τραγούδι και θα προστεθεί ένα στην τιμή της μεταβλητής, που σημαίνει ότι η `μελωδία` θα οριστεί σε `2`, η οποία σχετίζεται με τη μελωδία `punchline`.

  --- /feedback ---

- (x) `punchline`

  --- feedback ---

Εξαιρετικά! Πατώντας το κουμπί Β θα προστεθεί ένα στην τιμή της μεταβλητής, που σημαίνει ότι η `μελωδία` θα οριστεί σε `2`, η οποία σχετίζεται με τη μελωδία `punchline`.

  --- /feedback ---

- ( ) `dadadum`

  --- feedback ---

Περίπου. Η τιμή της μεταβλητής είναι `1` και το κουμπί B προσθέτει `1` στην τιμή της μεταβλητής, που σημαίνει ότι η μελωδία που σχετίζεται με την τιμή 1 (`dadadum`) δεν θα παίζει πλέον.

  --- /feedback ---

--- /choices ---

--- /question ---
