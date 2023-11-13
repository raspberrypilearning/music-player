## Stop and shuffle

Great job so far! You have chosen melodies to play and you have programmed the `A` and `B` buttons to skip through tracks. What happens if you want to stop the tunes from playing?

In this step, you will make use of the `on shake`{:class="microbitinput"} gesture to stop the tunes from playing.

### Shake to stop

--- task ---

From the `Input`{:class="microbitinput"} menu, drag an `on shake`{:class="microbitinput"} block and place it on the code editor panel.

```microbit
input.onGesture(Gesture.Shake, function () {
	
})
```

--- /task ---

--- task ---

From the `Logic`{:class="microbitlogic"} menu, drag an `if...else`{:class="microbitlogic"} block and place it inside the `on shake`{:class="microbitinput"} block.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (true) {
    	
    } else {
    	
    }
})
```

--- /task ---

--- task ---

Click on the `Logic`{:class="microbitlogic"} menu again and drag a comparison `0 = 0`{:class="microbitlogic"} block. 

Place it inside the `true`{:class="microbitlogic"} part of the `if...else`{:class="microbitlogic"} block.

--- /task ---

--- task ---

Click on the arrow next to the `=` on the comparison block. 

Choose the not equal to `≠` symbol.

```microbit
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {
    	
    } else {
    	
    }
})
```

--- /task ---

--- task ---

From the `Variables`{:class="microbitvariables"} menu, drag the `tune`{:class="microbitvariables"} variable block. 

Place it in the first `0` on the `0 ≠ 0`{:class="microbitlogic"} block.

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

From the `Music`{:class="microbitmusic"} block menu, drag a `stop all sounds`{:class="microbitmusic"} block. 

Place it inside the `if`{:class="microbitlogic"} part of the `if...else`{:class="microbitlogic"} block.

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

Click on the `Variables`{:class="microbitvariables"} menu and drag a `set [tune] to 0`{:class="microbitvariables"} block. 

Place it below the `stop all sounds`{:class="microbitmusic"} block. 

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

Now, when a melody is playing, you can shake the micro:bit and it will stop playing the melody.

### Shake again to shuffle

You will now add a condition so the micro:bit plays a random melody from your chosen melodies. This is similar to the shuffle function on a music player app.

--- task ---

Click on the `Variables`{:class="microbitvariables"} block menu and drag the `set [tune] to 0`{:class="microbitvariables"} block. 

Place it inside the `else`{:class="microbitlogic"} part of the `if...else`{:class="microbitlogic"} block.

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

From the `Math`{:class="microbitmath"} menu, drag a `pick random`{:class="microbitmath"} block.

Place it inside the `0` part of the `set tune`{:class="microbitvariables"} block. 

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

The range on the random block is currently set to `0 to 10`, however, our melodies are set from `1 to 4`. 

You will need to update this range to match.

--- task ---

Change the `0` part of the `pick random`{:class="microbitmath"} block to `1`.

Change the `10` part of the `pick random`{:class="microbitmath"} block to `4`.

--- /task ---

Your code should look like this:

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

When you make a change to a code block in the code editor panel, the simulator will restart.

**Test** 

When the program runs, you should now be able to stop and shuffle by shaking the micro:bit.

--- /task ---

--- task ---

Download your program onto your micro:bit!

--- /task ---

[[[download-to-microbit]]]

Well done! You now have a fully working music player!

Next, it is time to check what you have learnt!