## Use the buttons to skip tunes

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Instead of changing the melody by changing the `tune` variable value in the `on start` block, you can use buttons to change the value (and, therefore, the melody). 

In this step, you will create code to skip tracks using the micro:bit's event handlers.

</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
What is an <span style="color: #0faeb0">event handler</span>?

An event handler is code that will run when a particular event happens, such as “button A pressed”.

</p>

### Add button controls

The micro:bit has a Button `A` and a Button `B`.

You can use an event to control what happens when a button is pressed.

### Skip to the next track

Button B is on the right of the micro:bit, so use this button to skip to the next track.

To do this, you need to change the value of the <code style="background-color: #DC143C">tune</code> variable by `1`.

--- task ---

From the <code style="background-color: #D400D4">Input</code> menu, drag the <code style="background-color: #D400D4">on button</code> block to the code editor panel.

![The Input block menu with the 'on button A pressed' block highlighted.](images/input-on-ButtonA.png)

--- /task ---

--- task ---

Click on the arrow next to `A` on the <code style="background-color: #D400D4">on button</code> block. 

Change the `A` to `B`.

![The down arrow menu on the 'on button A pressed' block with B highlighted.](images/buttonA-arrow.png)

--- /task ---

#### Stop all sounds!

Now, you need to stop the current tune. 

--- task ---

From the <code style="background-color: #E63022">Music</code> menu, drag the <code style="background-color: #E63022">stop all sounds</code> block.

Place it in the <code style="background-color: #D400D4">on button [B]</code> block in the code editor panel.

![The Music block menu with the 'stop all sounds' block highlighted.](images/stop-all-sounds.png)

<div style="position:relative;height:calc(120px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_MLDi2adDz8u7" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #DC143C">Variables</code> menu, drag the <code style="background-color: #DC143C">change</code> block.

Place it below the <code style="background-color: #E63022">stop all sounds</code> block.

![The Variables block menu with the 'change tune by 1' block highlighted.](images/change-tune-by-1.png)

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_7oT6My8u3869" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

#### Dealing with 'out of range'

If the value of the variable is `4`, then changing it by `1` will make the value `5`.

🚨 But there is no melody associated with the value `5`! 🚨

Because you only have four melodies, if the variable changes to 5, you need to go back to the first melody.

<div style="position:relative;height:calc(400px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_0yCP24EifRFs" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- task ---

From the <code style="background-color: #00A4A6">Logic</code> menu, drag the <code style="background-color: #00A4A6">if</code> block.

Place it below the <code style="background-color: #DC143C">change tune</code> block in your code.

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_0PcDtthUHHMv" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

Also from the <code style="background-color: #00A4A6">Logic</code> menu, drag a <code style="background-color: #00A4A6">0 < 0</code> block.

Place it inside the `true` part of the <code style="background-color: #00A4A6">if</code> block.

Change the `<` (less than) to `>` (greater than) by clicking on the arrow next to the `<` symbol.

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_D4ACRhEUP3ae" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #DC143C">Variables</code> menu, drag the <code style="background-color: #DC143C">tune</code> variable  block.

Place it on the first `0` in the <code style="background-color: #00A4A6">0 > 0</code> block.

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_6u0MChMKJUTi" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

Change the second `0` to `4`.

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_UfKAa33KUUYx" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #DC143C">Variables</code> menu, drag the <code style="background-color: #DC143C">set</code> block.

Place it inside the <code style="background-color: #00A4A6">if</code> block in your code. 

Change the `0` to `1`.

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_PrxidP2WEb33" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---


#### Skip to the previous track

Button A is on the left of the micro:bit, so use this button to skip to the previous track.

To do this, you need to change the value of the `tune` variable by `-1`.

You can re-use the code you created to control what happens when Button B is pressed.

--- task ---

**Right-click** on the top part of the <code style="background-color: #D400D4">on button B pressed</code> block that you now have in the code editor panel. 

Click **Duplicate** to make a copy of the whole block. 

You should now have a second <code style="background-color: #D400D4">on button</code> block that will be 'greyed out'.

Change the button from `B` to `A`. This will stop the block from being greyed out.

<div style="position:relative;height:calc(175px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_PUj7f7TvzY1A" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---
Make these changes to the <code style="background-color: #D400D4">on button A pressed</code> block:

Change the `1` to `-1` in the <code style="background-color: #DC143C">change</code> block.

In the comparison block:

+ Change the `<` to `>` 

+ Change the `1` to `4`

Change the `1` to `4` in the <code style="background-color: #DC143C">set</code> block.

--- /task ---


You should now have an <code style="background-color: #D400D4">on button A pressed</code> block of code and an <code style="background-color: #D400D4">on button B pressed</code> block of code:

<div style="position:relative;height:calc(200px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_CbfbVkYrt0iW" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- task ---

**Debug:** Make sure you have changed the correct values in the blocks used to change the value of the variables.

For example: `Button A` should change the variable by `-1` and Button B should change the variable value by `1`.

--- /task ---

--- task ---

When you make a change to a code block in the code editor panel, the simulator will restart.

**Test your program** 

+ Press Button A to skip to the previous track

+ Press Button B to skip to the next track

--- /task ---


Well done, you can now skip your tracks back and forth!
