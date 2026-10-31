## Arrêter et lecture aléatoire

Bravo ! Tu as choisi des mélodies à jouer et tu as programmé les boutons `A` et `B` pour passer les pistes. Que se passe-t-il si tu veux arrêter la lecture des musiques ?

Dans cette étape, tu utiliseras le geste `lorsque secouer`{:class="microbitinput"} pour arrêter la lecture des musiques.

### Secouer pour arrêter

--- task ---

Dans le menu `Entrée`{:class="microbitinput"}, fais glisser un bloc `lorsque secouer`{:class="microbitinput"} et place-le sur le panneau de l'éditeur de code.

```microbit
input.onGesture(Gesture.Shake, function () {

})
```

--- /task ---

--- task ---

Dans le menu `Logique`{:class="microbitlogic"}, fais glisser un bloc `si...sinon`{:class="microbitlogic"} et place-le à l'intérieur du bloc `lorsque secouer`{:class="microbitinput"}.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (true) {

    } else {

    }
})
```

--- /task ---

--- task ---

Clique sur le menu `Logique`{:class="microbitlogic"} et fais glisser un bloc de comparaison `0 = 0`{:class="microbitlogic"}.

Place-le à l'intérieur du bloc `vrai`{:class="microbitlogic"} de la partie du bloc `si...sinon`{:class="microbitlogic"}.

--- /task ---

--- task ---

Clique sur la flèche à côté de la `=` sur le bloc de comparaison.

Choisis le symbole `≠` .

```microbit
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

Dans le menu `Variables`{:class="microbitvariables"}, fais glisser le bloc variable `musique`{:class="microbitvariables"}.

Place-le dans le premier bloc `0` sur le bloc `0 ≠ 0`{:class="microbitlogic"}.

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

Dans le menu bloc `Musique`{:class="microbitmusic"}, fais glisser un bloc `arrêter tous les sons`{:class="microbitmusic"}.

Place-le à l'intérieur du bloc `si`{:class="microbitlogic"} de la partie du bloc `si...sinon`{:class="microbitlogic"}.

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

Clique sur le menu `Variables`{:class="microbitvariables"} et fais glisser un bloc `définir [musique] à 0`{:class="microbitvariables"}.

Place-le sous le bloc `arrêter tous les sons`{:class="microbitmusic"}.

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

Maintenant, lorsqu'une mélodie est jouée, tu peux secouer le micro:bit et il arrêtera de jouer la mélodie.

### Secouer à nouveau pour une lecture aléatoire

Tu vas maintenant ajouter une condition pour que le micro:bit joue une mélodie aléatoire à partir des mélodies que tu as choisies. Ceci est similaire à la fonction de lecture aléatoire sur une application de lecteur de musique.

--- task ---

Clique sur le menu bloc `Variables`{:class="microbitvariables"} et fais glisser le bloc `définir [musique] à 0`{:class="microbitvariables"}.

Place-le à l'intérieur du bloc `sinon`{:class="microbitlogic"} de la partie du bloc `si...sinon`{:class="microbitlogic"}.

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

Dans le menu `Maths`{:class="microbitmath"}, fais glisser un bloc `choisir au hasard`{:class="microbitmath"}.

Place-le à l'intérieur de la partie `0` du bloc `définir musique`{:class="microbitvariables"}.

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

La portée du bloc choisir au hasard est actuellement définie de `0 à 10`, cependant, nos mélodies sont définies de `1 à 4`.

Tu devras mettre à jour cette plage pour qu'elle corresponde.

--- task ---

Modifie la partie `0` du bloc `choisir au hasard`{:class="microbitmath"} par `1`.

Modifie la partie `10` du bloc `choisir au hasard`{:class="microbitmath"} par `4`.

--- /task ---

Ton code devrait ressembler à ceci :

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

Lorsque tu modifies un bloc de code dans le panneau de l'éditeur de code, le simulateur redémarrera.

**Test**

Lorsque le programme s'exécute, tu devrais maintenant être en mesure d'arrêter et de faire une lecture aléatoire en secouant le micro:bit.

--- /task ---

--- task ---

Télécharge ton programme sur ton micro:bit !

--- /task ---

[[[download-to-microbit]]]

Bien joué ! Tu as maintenant un lecteur de musique entièrement fonctionnel !

Ensuite, il est temps de vérifier ce que tu as appris !