## Stop the tune

Great job so far! You have chosen melodies to play and you have programmed the `A` and `B` buttons to skip through tracks. What happens if you want to stop the tunes from playing?

In this step, you will make use of the `on shake` gesture to stop the tunes from playing.

### Using gestures

--- task ---

From the Input block menu, drag out an `on shake` block and place it on the code editor panel.

<div style="position:relative;height:calc(300px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:75%;height:75%;" src="https://makecode.microbit.org/---codeembed#pub:_Wff4v7MYXLrR" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the Logic block menu, drag out an `if.. true.. then.. else` block and place it inside the `on shake` block.

<div style="position:relative;height:calc(300px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:75%;height:75%;" src="https://makecode.microbit.org/---codeembed#pub:_gJtA1VWgueHk" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

Click on the Logic block menu again and drag out a comparison `0=0` block. Place it inside the `true` part of the `if.. true.. then.. else` block.

--- /task ---

--- task ---

Click on the arrow next to the `=` on the comparison block. Choose the not equal to `≠` symbol.

--- /task ---

--- task ---

From the Variables block menu, drag out the `music` variable block and place it in the first `0` on the `0 ≠ 0` comparison block.

--- /task ---

--- task ---

Using the Music blocks menu, drag out a `stop melody all` block. Place it inside the `if.. then` part of the `if.. true.. then.. else` block.

--- /task ---

--- task ---

Click on the Variables block menu again and drag out a `set music to 0` block. Place it below the `stop melody all` block.

--- /task ---

Now, each time a melody is playing, once you shake the micro:bit it will stop playing the melody.

### Creating a shuffle function

You will now add a condition so the melody plays a random melody from your chosen melodies. This is similar to the shuffle function on a music player app.

--- task ---

Click on the Variables block menu and drag out the `set music to 0` block. 

Place it inside the `else` part of the `if.. true.. then.. else` block.


--- /task ---