## Stop en shuffle

Goed gedaan! Je hebt de melodietjes gekozen om af te spelen en je hebt de `A` en `B` knoppen geprogrammeerd om nummers over te kunnen slaan. Wat gebeurt er als je het afspelen van de muziek wil stoppen?

In deze stap maak je gebruik van de `bij schudden`{:class="microbitinput"} mogelijkheid van je micro:bit om te voorkomen dat de melodieën spelen.

### Schud om te stoppen

--- task ---

Vanuit het `Invoer`{:class="microbitinput"} menu, sleep je het `bij schudden`{:class="microbitinput"} blok naar het bewerkingspaneel.

```microbit
input.onGesture(Gesture.Shake, function () {

})
```

--- /task ---

--- task ---

Vanuit het `Logisch`{:class="microbitlogic"} menu, sleep je een `als...anders`{:class="microbitlogic"} blok en plaats het in het `bij schudden`{:class="microbitinput"} blok.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (true) {

    } else {

    }
})
```

--- /task ---

--- task ---

Klik dan opnieuw op het `Logisch`{:class="microbitlogic"} menu en sleep een vergelijking `0 = 0`{:class="microbitlogic"} blok.

Plaats dit in het `waar`{:class="microbitlogic"} gebied van het `als....anders`{:class="microbitlogic"} blok.

--- /task ---

--- task ---

Klik op de pijl naast de `=` in het vergelijkingsblok.

Kies het symbool niet gelijk aan `≠`.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

Sleep vanuit het menu `Variabelen`{:class="microbitvariables"} een blok `deuntje`{:class="microbitvariables"}.

Plaats het in de eerste `0` in het `0 ≠ 0`{:class="microbitlogic"} blok.

```microbit
input.onGesture(Gesture.Shake, function () {
    let deuntje = 0
    if (deuntje != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

Sleep vanuit het menu `Muziek`{:class="microbitmusic"} het blok `stop alle geluiden`{:class="microbitmusic"}.

Plaats dit in het `als`{:class="microbitlogic"} gebied van het `als....anders`{:class="microbitlogic"} blok.

```microbit
input.onGesture(Gesture.Shake, function () {
    let deuntje = 0
    if (deuntje != 0) {
        music.stopAllSounds()
    } else {

    }
})
```

--- /task ---

--- task ---

Sleep vanuit het menu `Variabelen`{:class="microbitvariables"} een blok `stel [deuntje] in op 0`{:class="microbitvariables"}.

Plaats het onder het blok `stop alle geluiden`{:class="microbitmusic"}.

```microbit
let deuntje = 0
input.onGesture(Gesture.Shake, function () {
    if (deuntje != 0) {
        music.stopAllSounds()
        deuntje = 0
    } else {

    }
})
```

--- /task ---

Als er nu een melodie speelt, kun je de micro:bit schudden en stopt hij met het spelen van de melodie.

### Opnieuw schudden om te shuffelen

Je voegt nu een voorwaarde toe zodat de micro:bit een willekeurige melodie speelt uit de door jou gekozen melodieën. Dit is vergelijkbaar met de shuffle-functie op een muziekspeler-app.

--- task ---

Klik op het blokmenu `Variabelen`{:class="microbitvariables"} en sleep het `stel [deuntje] in op`{:class="microbitvariables"} blok.

Plaats dit in het `anders`{:class="microbitlogic"} gebied van het `als....anders`{:class="microbitlogic"} blok.

```microbit
let deuntje = 0
input.onGesture(Gesture.Shake, function () {
    if (deuntje != 0) {
        music.stopAllSounds()
        deuntje = 0
    } else {
        deuntje = 0
    }
})
```

--- /task ---

--- task ---

Sleep vanuit het menu `Rekenen`{:class="microbitmath"} een blok `kies willekeurig 0 tot 10`{:class="microbitmath"}.

Plaats dit in het `0`{:class="microbitlogic"} deel van het `stel deuntje in op`{:class="microbitlogic"} blok.

```microbit
let deuntje = 0
input.onGesture(Gesture.Shake, function () {
    if (deuntje != 0) {
        music.stopAllSounds()
        deuntje = 0
    } else {
        deuntje = randint(0, 10)
    }
})
```

--- /task ---

Het bereik op het willekeurige blok is momenteel ingesteld op `0 tot 10`, maar onze melodieën zijn ingesteld van `1 tot 4`.

Je moet dit bereik bijwerken zodat het overeenkomt met het aantal melodieën dat je hebt gekozen.

--- task ---

Verander de `0` van het blok `kies willekeurig`{:class="microbitmath"} naar `1`.

Verander de `10` van het blok `kies willekeurig`{:class="microbitmath"} naar `4`.

--- /task ---

Je code zou er als volgt uit moeten zien:

```microbit
let deuntje = 0
input.onGesture(Gesture.Shake, function () {
    if (deuntje != 0) {
        music.stopAllSounds()
        deuntje = 0
    } else {
        deuntje = randint(1, 4)
    }
})
```

--- task ---

Als je een wijziging aanbrengt in een codeblok in het bewerkingspaneel zal de simulator opnieuw starten.

**Test**

Wanneer het programma wordt uitgevoerd, moet je nu kunnen stoppen en shuffelen door de micro:bit te schudden.

--- /task ---

--- task ---

Download je programma naar de micro:bit!

--- /task ---

[[[download-to-microbit]]]

Goed gedaan! Je hebt nu een volledig werkende muziekspeler!

Nu is het tijd om te kijken wat je hebt geleerd!
