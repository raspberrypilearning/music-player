## Detener y mezclar

¡Buen trabajo hasta ahora! Has elegido melodías para reproducir y has programado los botones `A` y `B` para saltar entre pistas. ¿Qué pasa si quieres detener la reproducción de las melodías?

En este paso, utilizarás el gesto `al agitar`{:class="microbitinput"} para detener la reproducción de las melodías.

### Agitar para detener

--- task ---

Desde el menú `Entrada`{:class="microbitinput"}, arrastre un bloque `al agitar`{:class="microbitinput"} y colóquelo en el panel del editor de código.

```microbit
input.onGesture(Gesture.Shake, function () {

})
```

--- /task ---

--- task ---

Desde el menú `lógica`{:class="microbitlógica"}, arrastra un bloque `si...else`{:class="microbitlógica"} y colócalo dentro del bloque `al agitar`{:class="microbitinput"}.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (true) {

    } else {

    }
})
```

--- /task ---

--- task ---

Haga clic en el menú `Lógica`{:class="microbitlogic"} nuevamente y arrastre un bloque de comparación `0 = 0`{:class="microbitlogic"}.

Colóquelo dentro de la parte `true`{:class="microbitlogic"} del bloque `if...else`{:class="microbitlogic"}.

--- /task ---

--- task ---

Haga clic en la flecha junto a `=` en el bloque de comparación.

Elija el símbolo no igual `=`.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {

    } else {

    }
})
```

--- /task ---

--- task ---

Desde el menu `Variables`{:class='microbitvariables'}, obten el bloque `fijar a`{:class='microbitvariables'}.

Colóquelo en el primer `0` del bloque `0 = 0`{:class="microbitlogic"}.

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

Desde el menú del bloque `Música`{:class="microbitmusic"}, arrastre un bloque `detener todos los sonidos`{:class="microbitmusic"}.

Colóquelo dentro de la parte `if`{:class="microbitlogic"} del bloque `if...else`{:class="microbitlogic"}.

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

Haz clic en el menú `Variables`{:class="microbitvariables"} y arrastra un bloque `fijar [tune] a 0`{:class="microbitvariables"}.

Colocalo debajo del bloque `mostrar icono`{:class='microbitbasic'}.

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

Ahora, cuando se reproduce una melodía, puedes agitar el micro:bit y dejará de reproducir la melodía.

### Agitar de nuevo para mezclar

Ahora añadirás una condición para que el micro:bit reproduzca una melodia aleatoria de las melodias elegidas. Esto es similar a la función aleatoria en una aplicación de reproductor de música.

--- task ---

Haz clic en el menú `Variables`{:class="microbitvariables"} y arrastra un bloque `fijar [tune] a 0`{:class="microbitvariables"}.

Colóquelo dentro de la parte `true`{:class="microbitlogic"} del bloque `if...else`{:class="microbitlogic"}.

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

Desde el menú `Matemáticas`{:class="microbitmath"}, arrastre un bloque `de selección aleatoria`{:class="microbitmath"}.

Colóquelo dentro de la parte `0` del bloque `set tune`{:class="microbitvariables"}.

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

El rango en el bloque aleatorio actualmente está establecido en `0 a 10`, sin embargo, nuestras melodías están establecidas en `1 a 4`.

Necesitará actualizar este rango para que coincida.

--- task ---

Cambia la parte `0` del bloque `de selección aleatoria`{:class="microbitmath"} a `1`.

Cambia el bloque `10` parte de la ` seleccion aleatoria`{:class="microbitmath"} a `4`.

--- /task ---

Tu codigo deberia de verse asi:

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

Cuando haces un cambio a un bloque de codigo en el panel del editor de codigo, el simulador se reiniciara.

**Prueba**

Cuando el programa se ejecute, ahora deberías poder detenerlo y reproducirlo agitando el micro:bit.

--- /task ---

--- task ---

¡Descarga tu programa en tu micro:bit!

--- /task ---

[[[download-to-microbit]]]

¡Bien hecho! ¡Ahora tienes un reproductor de música totalmente funcional!

Ahora, ¡es tiempo de revisar lo que has aprendido!