## Διακοπή και ανακάτεμα

Φοβερή δουλειά μέχρι στιγμής! Έχεις επιλέξει μελωδίες για να ακούσεις και έχεις προγραμματίσει τα κουμπιά `A` και `B` ώστε να επιλέγεις τραγούδια. Τι θα συμβεί αν θέλεις να σταματήσεις την αναπαραγωγή των τραγουδιών;

Σε αυτό το βήμα, θα χρησιμοποιήσετε την κίνηση `στο κούνημα`{:class="microbitinput"} για να σταματήσεις την αναπαραγωγή των τραγουδιών.

### Ανακίνηση για να σταματήσει

--- task ---

Από το μενού `Είσοδος`{:class="microbitinput"}, σύρε το μπλοκ `στο κούνημα`{:class="microbitinput"} στον πίνακα επεξεργασίας κώδικα.

```microbit
input.onGesture(Gesture.Shake, function () {

})
```

--- /task ---

--- task ---

Από το μενού `Λογική`{:class="microbitlogic"}, σύρε ένα μπλοκ `εάν...αλλιώς`{:class="microbitlogic"} και τοποθέτησέ το μέσα στο μπλοκ `στο κούνημα`{:class="microbitinput"}.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (true) {

    } else {

    }
})
```

--- /task ---

--- task ---

Κάνε κλικ στο μενού `Λογική`{:class="microbitlogic"} ξανά και σύρε ένα μπλοκ σύγκρισης `0 = 0`{:class="microbitlogic"}.

Τοποθέτησε το στην περιοχή `αληθές`{:class="microbitlogic"} του μπλοκ `εάν...αλλιώς`{:class="microbitlogic"}.

--- /task ---

--- task ---

Κάνε κλικ στο βέλος δίπλα στο `=` στο μπλοκ σύγκρισης.

Επίλεξε το σύμβολο όχι ίσο με `≠`.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

Από το μενού `Μεταβλητές`{:class="microbitvariables"}, σύρε το μπλοκ μεταβλητής `μελωδία`{:class="microbitvariables"}.

Τοποθέτησέ το μέσα στο πρώτο `0` στο μπλοκ `0 ≠ 0`{:class="microbitlogic"}.

```microbit
input.onGesture(Gesture.Shake, function () {
    let μελωδία = 0
    if (μελωδία != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

Από το μενού μπλοκ `Μουσική`{:class="microbitmusic"}, σύρε ένα μπλοκ `stop all sounds`{:class="microbitmusic"}.

Τοποθέτησε το στην περιοχή `έαν`{:class="microbitlogic"} του μπλοκ `εάν...αλλιώς`{:class="microbitlogic"}.

```microbit
input.onGesture(Gesture.Shake, function () {
    let μελωδία = 0
    if (μελωδία != 0) {
        music.stopAllSounds()
    } else {

    }
})
```

--- /task ---

--- task ---

Κάνε κλικ στο μενού `Μεταβλητές`{:class="microbitvariables"} και σύρε ένα μπλοκ `ορισμός μελωδία`{:class="microbitvariables"}.

Τοποθέτησέ το κάτω από το μπλοκ `stop all sounds`{:class="microbitmusic"}.

```microbit
let μελωδία = 0
input.onGesture(Gesture.Shake, function () {
    if (μελωδία != 0) {
        music.stopAllSounds()
        μελωδία = 0
    } else {

    }
})
```

--- /task ---

Τώρα, όταν παίζει μια μελωδία, μπορείς να ανακινήσεις το micro:bit και θα σταματήσει να παίζει τη μελωδία.

### Ανακίνηση ξανά για να ανακατευτούν τα τραγούδια

Τώρα θα προσθέσεις μια συνθήκη ώστε το micro:bit να παίζει μια τυχαία μελωδία από τις επιλεγμένες μελωδίες σου. Αυτή είναι παρόμοια με τη λειτουργία τυχαίας αναπαραγωγής σε μια εφαρμογή αναπαραγωγής μουσικής.

--- task ---

Κάνε κλικ στο μενού μπλοκ `Μεταβλητές`{:class="microbitvariables"} και σύρε το μπλοκ `ορισμός μελωδία`{:class="microbitvariables"}.

Τοποθέτησε το στην περιοχή `αλλιώς`{:class="microbitlogic"} του μπλοκ `εάν...αλλιώς`{:class="microbitlogic"}.

```microbit
let μελωδία = 0
input.onGesture(Gesture.Shake, function () {
    if (μελωδία != 0) {
        music.stopAllSounds()
        μελωδία = 0
    } else {
        μελωδία = 0
    }
})
```

--- /task ---

--- task ---

Από το μενού `Μαθηματικά`{:class="microbitmath"}, σύρε ένα μπλοκ `τυχαία επιλογή`{:class="microbitmath"}.

Τοποθέτησέ το μέσα στο τμήμα `0` του μπλοκ `ορισμός μελωδία`{:class="microbitvariables"}.

```microbit
let μελωδία = 0
input.onGesture(Gesture.Shake, function () {
    if (μελωδία != 0) {
        music.stopAllSounds()
        μελωδία = 0
    } else {
        μελωδία = randint(0, 10)
    }
})
```

--- /task ---

Το εύρος στο μπλοκ για την τυχαιότητα έχει οριστεί αυτή τη στιγμή από `0 έως 10`, όμως, οι μελωδίες μας έχουν οριστεί από `1 έως 4`.

Θα χρειαστεί να ενημερώσεις αυτό το εύρος ώστε να ταιριάζει με τις επιλογές μας.

--- task ---

Άλλαξε το τμήμα `0` του μπλοκ `τυχαία επιλογή`{:class="microbitmath"} σε `1`.

Άλλαξε το τμήμα `10` του μπλοκ `τυχαία επιλογή`{:class="microbitmath"} σε `4`.

--- /task ---

Ο κώδικας θα πρέπει να μοιάζει κάπως έτσι:

```microbit
let μελωδία = 0
input.onGesture(Gesture.Shake, function () {
    if (μελωδία != 0) {
        music.stopAllSounds()
        μελωδία = 0
    } else {
        μελωδία = randint(1, 4)
    }
})
```

--- task ---

Όταν κάνεις μια αλλαγή σε ένα μπλοκ στο πρόγραμμα επεξεργασίας κώδικα, ο προσομοιωτής θα επανεκκινήσει.

**Δοκιμή**

Όταν εκτελείται το πρόγραμμα, θα πρέπει τώρα να μπορείς να σταματήσεις και να κάνεις τυχαία αναπαραγωγή ανακινώντας το micro:bit.

--- /task ---

--- task ---

Κατέβασε το πρόγραμμά σου στο micro:bit!

--- /task ---

[[[download-to-microbit]]]

Συγχαρητήρια! Τώρα έχεις ένα πλήρως λειτουργικό πρόγραμμα αναπαραγωγής μουσικής!

Στη συνέχεια, ήρθε η ώρα να ελέγξεις τι έχεις μάθει!