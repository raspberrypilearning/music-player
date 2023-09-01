## Allowing Choices

### Creating a variable

Throughout creating your music player, you will need to use variables. 

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
What is a <span style="color: #0faeb0">variable?</span>

A variable is a way of labelling and storing data in your programs. Your program can use and change the data stored in a variable when it runs.

Data stored in a variable might be a number like `10` or a word like `dinosaur`.

</p>

--- task ---

Open the <code style="background-color: #DC143C">Variables</code> menu, and click **Make a Variable**.

![The Variables menu, open with the 'Make a Variable' button highlighted](images/variable-menu.png)

--- /task ---

--- task ---

Name the new variable `tune`, then click the `Ok` button.

<img src="images/variable-tune.png" alt="The 'New variable name' window, with the name 'tune' written in the box" width="450"/>

--- /task ---

There will now be new blocks available that you can use to set, change or use the value stored in the <code style="background-color: #DC143C">tune</code> variable. 

<img src="images/variableblocks-tune.png" alt="The Variables menu - with new blocks to set, change and use the value of the tune variable." width="350"/>

--- task ---

Drag out the <code style="background-color: #DC143C">set</code>block and place it inside the <code style="background-color: #1E90FF">on start</code> block.

Change the `0` to `1`.

<div style="position:relative;height:calc(120px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_MHwLMFgh3Duz" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

### Using if... then

In order for your music player to play different melody choices, you will need to make use of a logic block for each melody.

--- task ---

From the <code style="background-color: #00A4A6">Logic</code> menu, grab an <code style="background-color: #00A4A6">if</code> block.

<img src="images/if-block-location.png" alt="The Logic menu with the `if` block highlighted" width="350"/>

--- /task ---

--- task ---

Place it above the <code style="background-color: #E63022">play melody dadadum</code> block.
 
Click on the <code style="background-color: #00A4A6">Logic</code> menu and drag out a comparison <code style="background-color: #00A4A6">0 = 0</code> block. 

Place this in the <code style="background-color: #00A4A6">true</code> area of the <code style="background-color: #00A4A6">if</code> block.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_WrzDXU4KKeRY" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

From the <code style="background-color: #DC143C">Variables</code> menu, drag out a <code style="background-color: #DC143C">tune</code> block. 

Place it into the first `0` in the <code style="background-color: #00A4A6">0 = 0</code> block.

Change the second `0` to `1`.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_HyH5uA1iA80o" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

Move the <code style="background-color: #E63022">play melody dadadum</code> block inside the <code style="background-color: #00A4A6">if</code> block.

<div style="position:relative;height:calc(150px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_40uahb1ahe5k" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

To add more melody choices, you need to create more conditions in the <code style="background-color: #00A4A6">if</code> block.

--- task ---

Click on the `+` symbol on the bottom left of the <code style="background-color: #00A4A6">if</code> block. This will create an <code style="background-color: #00A4A6">else</code> section. 

--- /task ---

--- task ---

Click on the `+` symbol below the <code style="background-color: #00A4A6">else</code> section. 

This will create an <code style="background-color: #00A4A6">else if</code> section. 

Repeat this twice, so you have three <code style="background-color: #00A4A6">else if</code> sections and an <code style="background-color: #00A4A6">else</code> section.

--- /task ---

--- task ---

Click on the `-` symbol next to the <code style="background-color: #00A4A6">else</code> section to remove the <code style="background-color: #00A4A6">else</code> section.

<img src="images/elseif-blocks.gif" alt="An animation showing the + symbol used to add three 'else if' sections. Finally, the 'else' is removed from the end by clicking the '-' symbol next to it" width="350"/>

--- /task ---

--- task ---

Right click on the <code style="background-color: #DC143C">tune</code> <code style="background-color: #00A4A6">=</code> `1` block and duplicate it.

<img src="images/duplicate-comparison.png" alt="The '=' comparison block highlighted, with the right click menu expanded showing options including 'Duplicate'" width="350"/>

--- /task ---

--- task ---

Place the duplicated <code style="background-color: #DC143C">tune</code> <code style="background-color: #00A4A6">=</code> `1` block between the first <code style="background-color: #00A4A6">else if</code> and <code style="background-color: #00A4A6">then</code>. 

Duplicate two more comparison blocks and place them between the other <code style="background-color: #00A4A6">else if</code> and <code style="background-color: #00A4A6">then</code> parts.

<img src="images/elseif-tune.gif" alt="A duplicated comparison block showing the 'tune' variable is dragged into an empty shaped space on an 'else..if' condition block. This is repeated twice until all condition blocks have comparison blocks in them" width="350"/>

--- /task ---

--- task ---

Inside the first <code style="background-color: #00A4A6">else if</code> section, change the `1` to `2`.

For the second <code style="background-color: #00A4A6">else if</code> section, change the `1` to `3`. 

For the third <code style="background-color: #00A4A6">else if</code> section, change the `1` to `4`

<div style="position:relative;height:calc(250px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_HM28gkfiieR4" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

You will now need to select a different melody for each <code style="background-color: #00A4A6">else if</code> section. 

Each time the variable value is changed, a different melody will play.

--- task ---

Duplicate the <code style="background-color: #E63022">play melody dadadum</code> block. 

Place the duplicated block inside the first <code style="background-color: #00A4A6">else if</code> section. 

Click on the arrow next to <code style="background-color: #E63022">melody dadadum</code> to see more melody options. 

Scroll to view all the melodies and choose one. 

Repeat these steps for the second and third <code style="background-color: #00A4A6">else if</code> sections. 

You should now have four melodies, one for each of the four conditions.

<div style="position:relative;height:calc(250px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_f5DefxebuH6c" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

**Debug:** Ensure you have changed all the numbers in the comparisons after duplicating them. 

You should have `1` in the <code style="background-color: #00A4A6">if</code> section and then `2,3,4` in the <code style="background-color: #00A4A6">else if</code> sections.

--- /task ---

--- task ---

When you make a change to a code block in the code editor panel, the simulator will restart.

**Test:** your program.

+ Change the <code style="background-color: #DC143C">set tune</code>  from `1` to `2` on the <code style="background-color: #1E90FF">on start/code>  block. 
The simulator will restart and play the melody for 2.

+ Repeat the same steps for melodies 3 and 4.

+ Ensure you change the <code style="background-color: #DC143C">set tune</code> back to `1` at the end of your tests.

Well done, you have chosen different melodies for your music player!

--- /task ---