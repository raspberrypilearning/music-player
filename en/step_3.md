## Allowing Choices

### Create a variable

Throughout the creation process for your music player, you will need to use variables. 

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
What is a <span style="color: #0faeb0">variable?</span>

A variable is a way to label and store data in your programs. Your program can use and change the data stored in a variable when it runs.

Data stored in a variable might be a number like `10` or a word like `dinosaur`.

</p>

--- task ---

Open the `Variables`{:class="microbitvariables"} menu, and click **Make a Variable**.

![The Variables menu with the 'Make a Variable' button highlighted.](images/variable-menu.png)

--- /task ---

--- task ---

Name the new variable `tune`, then click the **OK** button.

<img src="images/variable-tune.png" alt="The 'New variable name' window, with the name 'tune' written in the box." width="450"/>

--- /task ---

There will now be new blocks available that you can use to set, change, or use the value stored in the `tune`{:class="microbitvariables"} variable. 

<img src="images/variableblocks-tune.png" alt="The Variables menu with new blocks to set, change, and use the value of the tune variable." width="350"/>

--- task ---

Drag the `set`{:class="microbitvariables"} block and place it inside the `on start`{:class="microbitbasic"} block.

Change the `0` to `1`.

```microbit
let tune = 1
```

--- /task ---

### Use of if...then

For your music player to play different melody choices, you will need to make use of a logic block for each melody.

--- task ---

From the `Logic`{:class="microbitlogic"} menu, choose the `if`{:class="microbitlogic"} block.

<img src="images/if-block-location.png" alt="The Logic menu with the `if` block highlighted." width="350"/>

--- /task ---

--- task ---

Place the `if`{:class="microbitlogic"} block above the `play melody dadadum`{:class="microbitmusic"} block.
 
Click on the `Logic`{:class="microbitlogic"} menu and drag a comparison `0 = 0`{:class="microbitlogic"} block. 

Place this in the `true`{:class="microbitlogic"} area of the `if`{:class="microbitlogic"} block.

```microbit
basic.forever(function () {
    if (0 == 0) {
    	
    }
    basic.showIcon(IconNames.Duck)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
})
```

--- /task ---

--- task ---

From the `Variables`{:class="microbitvariables"}</code> menu, drag a `tune`{:class="microbitvariables"} block. 

Place it into the first `0` in the `0 = 0`{:class="microbitlogic"} block.

Change the second `0` to `1`.

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
    	
    }
    basic.showIcon(IconNames.Duck)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
})
```

--- /task ---

--- task ---

Move the `show icon`{:class="microbitbasic"} and `show melody`{:class="microbitmusic"} blocks inside the `if`{:class="microbitlogic"} block.

**Tip:** Whenever you grab a block, all the blocks beneath it will move as well, so just drag the `show icon`{:class="microbitbasic"} block and the others will follow.

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Duck)
    }
})
```

--- /task ---

To add more melody choices, you need to create more conditions in the `if`{:class="microbitlogic"} 
block.

--- task ---

Click on the `+` symbol on the bottom left of the `if`{:class="microbitlogic"} block. This will create an `else`{:class="microbitlogic"} section. 

--- /task ---

--- task ---

Click on the `+` symbol below the `else`{:class="microbitlogic"} section. 

This will create an <code style="background-color: #00A4A6">else if</code> section. 

Repeat this twice, so you have three `else if`{:class="microbitlogic"} sections and an `else`{:class="microbitlogic"} section.

--- /task ---

--- task ---

Click on the `-` symbol next to the `else`{:class="microbitlogic"} section to remove the `else`{:class="microbitlogic"} section.

<img src="images/elseif-blocks.gif" alt="An animation showing the + symbol being used to add three 'else if' sections. Finally, the 'else' is removed from the end by clicking the '-' symbol next to it." width="350"/>

--- /task ---

--- task ---

Right-click on the `tune`{:class="microbitvariables"} `=`{:class="microbitlogic"} `1` block and duplicate it.

<img src="images/duplicate-comparison.png" alt="The '=' comparison block highlighted, with the right click menu expanded showing options including 'Duplicate'." width="350"/>

--- /task ---

--- task ---

Place the duplicated `tune`{:class="microbitvariables"} `=`{:class="microbitlogic"} `1` block between the first `else if`{:class="microbitlogic"} and `then`{:class="microbitlogic"}. 

Duplicate two more comparison blocks and place them between the other <code style="background-color: #00A4A6">else if</code> and <code style="background-color: #00A4A6">then</code> parts.

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        basic.showIcon(IconNames.Duck)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (tune == 1) {
    	
    } else if (tune == 1) {
    	
    } else if (tune == 1) {
    	
    }
})
```

--- /task ---

--- task ---


basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        basic.showIcon(IconNames.Duck)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (tune == 1) {
    	
    } else if (tune == 1) {
    	
    } else if (tune == 1) {
    	
    }
})
Inside the first `else if`{:class="microbitlogic"} section, change the `1` to `2`.

For the second `else if`{:class="microbitlogic"} section, change the `1` to `3`. 

For the third `else if`{:class="microbitlogic"} section, change the `1` to `4`.

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        basic.showIcon(IconNames.Duck)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (tune == 2) {
    	
    } else if (tune == 3) {
    	
    } else if (tune == 4) {
    	
    }
})
```

--- /task ---

You now need to select a different melody for each `else if`{:class="microbitlogic"} section. 

Each time the variable value is changed, a different melody will play.

--- task ---

Duplicate the `play melody dadadum`{:class="microbitmusic"} block. 

Place the duplicated block inside the first `else if`{:class="microbitlogic"} section. 

Click on the arrow next to `melody dadadum`{:class="microbitmusic"}</code> to see more melody options. 

Scroll to view all the melodies and choose one. 

Repeat these steps for the second and third `else if`{:class="microbitlogic"} sections. 

You should now have four melodies, one for each of the four conditions.

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Duck)
    } else if (tune == 2) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Punchline), music.PlaybackMode.UntilDone)
    } else if (tune == 3) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Birthday), music.PlaybackMode.UntilDone)
    } else if (tune == 4) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Baddy), music.PlaybackMode.UntilDone)
    }
})
```

--- /task ---

You also need to select some **icons** for each of your new songs. 

You can duplicate the `show icon`{:class="microbitbasic"} block.

You can also use the `show leds`{:class="microbitbasic"} block to draw your own!

--- collapse ---

---
title: The show leds block
---

Inside the `Basic`{:class="microbitbasic"} menu, find the `show leds`{:class="microbitbasic"} block and drag it inside an `else if`{:class="microbitlogic"} to use it.

<img src="images/show-leds.png" alt="The Basic menu with the 'show leds' block highlighted." width="350"/>

You can click on each of the squares to draw your picture. White squares will be lit on the micro:bit.

We drew a **birthday cake** for the `birthday` melody.

<img src="images/draw-icon.png" alt="The 'show leds' block with a birthday cake with two candles created in white squares." width="350"/>

--- /collapse ---

--- task ---

Add icons for each of your songs using either the `show icon`{:class="microbitbasic"} or `show leds`{:class="microbitbasic"} block. 

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        basic.showIcon(IconNames.Duck)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
    } else if (tune == 2) {
        basic.showIcon(IconNames.Silly)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Punchline), music.PlaybackMode.UntilDone)
    } else if (tune == 3) {
        basic.showLeds(`
            . # . # .
            . # . # .
            # # # # #
            # # # # #
            # # # # #
            `)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Birthday), music.PlaybackMode.UntilDone)
    } else if (tune == 4) {
        basic.showIcon(IconNames.Skull)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Baddy), music.PlaybackMode.UntilDone)
    }
})
```

--- /task ---

--- task ---

**Debug:** Ensure you have changed all the numbers in the comparisons after duplicating them. 

You should have `1` in the `if`{:class="microbitlogic"} section and then `2, 3, 4` in the `else if`{:class="microbitlogic"} sections.

--- /task ---

--- task ---

When you make a change to a code block in the code editor panel, the simulator will restart.

**Test your program**

+ Change the `set tune`{:class="microbitvariables"} from `1` to `2` on the `on start`{:class="microbitbasic"} block. 
The simulator will restart and play the melody for 2, and show that icon.

+ Repeat the same steps for melodies 3 and 4.

+ Ensure you change the `set tune`{:class="microbitvariables"} back to `1` at the end of your tests.

Well done, you have chosen different melodies for your music player!

--- /task ---
