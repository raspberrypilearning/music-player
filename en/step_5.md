## Stop and shuffle

Great job so far! You have chosen melodies to play and you have programmed the `A` and `B` buttons to skip through tracks. What happens if you want to stop the tunes from playing?

In this step, you will make use of the `on shake` gesture to stop the tunes from playing.

### Shake to stop

--- task ---

From the <code style="background-color: #D400D4">Input</code> menu, drag out an <code style="background-color: #D400D4">on shake</code> block and place it on the code editor panel.

<div style="position:relative;height:calc(100px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_Wff4v7MYXLrR" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #00A4A6">Logic</code> menu, drag out an <code style="background-color: #00A4A6">if else</code> block and place it inside the <code style="background-color: #D400D4">on shake</code> block.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_gJtA1VWgueHk" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

Click on the <code style="background-color: #00A4A6">Logic</code> menu again and drag a comparison <code style="background-color: #00A4A6">0 = 0</code> block. 

Place it inside the `<true>` part of the `<code style="background-color: #00A4A6">if else</code> block.

--- /task ---

--- task ---

Click on the arrow next to the `=` on the comparison block. 

Choose the not equal to `≠` symbol.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_AA9huPHi1YsX" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #DC143C">Variables</code> menu, drag out the <code style="background-color: #DC143C">tune</code> variable block. 

Place it in the first `0` on the <code style="background-color: #00A4A6">0 ≠ 0 </code> block.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_LA4CUmC8HgcM" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #E63022">Music</code> block menu, drag out a <code style="background-color: #E63022">stop all sounds</code> block. 

Place it inside the <code style="background-color: #00A4A6">if</code> part of the <code style="background-color: #00A4A6">if..else</code> block.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_Pt5h7M8UzMTJ" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

Click on the <code style="background-color: #DC143C">Variables</code> menu and drag out a <code style="background-color: #DC143C">set [tune] to 0</code> block. 

Place it below the <code style="background-color: #E63022">stop all sounds</code> block. 

<div style="position:relative;height:calc(150px + 5em);width:80%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_UT3Hzm0Wy69u" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

Now, each time a melody is playing, once you shake the micro:bit it will stop playing the melody.

### Shake again to shuffle

You will now add a condition so the micro:bit plays a random melody from your chosen melodies. This is similar to the shuffle function on a music player app.

--- task ---

Click on the <code style="background-color: #DC143C">Variables</code> block menu and drag out the <code style="background-color: #DC143C">set [tune] to 0</code> block. 

Place it inside the <code style="background-color: #00A4A6">else</code> part of the <code style="background-color: #00A4A6">if..else</code> block.

<div style="position:relative;height:calc(150px + 5em);width:80%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_djJ03JPU4X2u" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #9400D3">Math</code> menu drag out a <code style="background-color: #9400D3">pick random</code> block.

Place it inside the `20` part of the <code style="background-color: #DC143C">set tune</code> block. 

<div style="position:relative;height:calc(150px + 5em);width:80%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_01fgmFYmVfaC" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>


--- /task ---

The range on the random block is currently set to `0 to 10`, however, our melodies are set from `1 to 4`. 

You will need to update this range to match.

--- task ---

Change the `0` part of the <code style="background-color: #9400D3">pick random</code> block to `1`.

Change the `10` part of the <code style="background-color: #9400D3">pick random</code> block to `4`.

--- /task ---

Your code should look like this:

<div style="position:relative;height:calc(200px + 5em);width:80%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_fcaL4MJspL52" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- task ---

When you make a change to a code block in the code editor panel, the simulator will restart.

**Test** 

When the program runs, you should now be able to stop and shuffle by shaking the micro:bit.

--- /task ---

--- task ---

### Downloading your program to the micro:bit

To run your program on your physical micro:bit, you will need to download your program file to it.

Click on the `Download` button below the micro:bit simulator. 

![the MakeCode editor showing the highlighted Download button](images/download-button.png)

You will be asked to plug in your micro:bit. Do that now, then click **Continue**. 

Click **Pair** and select your device from the list that appears, then click **Connect**.

![The 'select micro:bit' dialog box showing a BBC micro:bit device.](images/select-microbit.png)

**Debug:** My micro:bit won't pair

If your micro:bit won't pair using the method above, it will download the program for you. 

**Windows:** Open **File Explorer** and check that you can see `MICROBIT` under `This PC` on the left hand side. If it is there, drag the downloaded `.HEX` file to it, your program will be saved to your micro:bit and you should be able to use it.

**MacOS:** Open **Finder** and check that you can see `MICROBIT` under `Locations` on the left hand side. If it is there, drag the downloaded `.HEX` file to it, your program will be saved to your micro:bit and you should be able to use it.

If your micro:bit isn't showing up, try unplugging it and plugging it back in. You can also try a different USB port or USB cable if they are available.


--- /task ---
