## Play a tune

### Opening MakeCode

To start creating your micro:bit project, you need to open the MakeCode editor.

--- task ---

Open the MakeCode editor at [makecode.microbit.org](https://makecode.microbit.org){:target="_blank"}

--- collapse ---

---
title: Offline version of the editor
---

There is also a [downloadable version of the MakeCode editor](https://makecode.microbit.org/offline-app){:target="_blank"}.

--- /collapse ---

--- /task ---

Once the editor is open, you will need to create a New Project and give your project a name. 

--- task ---

Click on the **New Project** button.

<img src="images/new-project-button.png" alt="The New Project button inside MakeCode." width="250"/>

--- /task ---

--- task ---

Give your new project the name `music player` and click **Create**.

<img src="images/music-player.png" alt="The name 'music player' written in the Create a Project dialogue box." width="400"/>

**Tip:** Give your project a helpful name that relates to the activity you’re creating. This will make it easier to find if you create other projects on MakeCode.

--- /task ---

[[[makecode-tour]]]

### Play melody


You are going to use the <code style="background-color: #1E90FF">forever</code> block to make use of the speaker output on the micro:bit (V2 users only).

--- collapse ---
---
title: V1 micro:bit users
---

The speaker output is only available on the V2 of the micro:bit. You will need to connect external headphones/speakers to play sound on the V1. You will still be able to play the sound on the simulator.

There is also a [guide to connecting headphones/speakers to the V1 micro:bit](https://makecode.microbit.org/projects/hack-your-headphones/make#:~:text=The%20tip%20of%20your%20headphone,headphone%20jack%20to%20play%20sounds.){:target="_blank"}.

--- /collapse ---


--- task ---

From the <code style="background-color: #E63022">Music</code> menu, drag the <code style="background-color: #E63022">play melody dadadum</code> block and place it inside the <code style="background-color: #1E90FF">forever</code> block.

<img src="images/play-melody.png" alt="The Music menu open with the 'play melody dadadum' block highlighted" width="400"/>

--- /task ---

--- task ---

On the <code style="background-color: #E63022">play melody dadadum</code> block, click on the down arrow next to <code style="background-color: #E63022">in background</code>. Choose 'until done' (for how long the melody will play).


<img src="images/melody-untildone.gif" alt="The melody drop down menu, open with the 'until done' button selected" width="300"/>

<div style="position:relative;height:calc(200px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:75%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_Tr00PpKK07YM" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

--- /task ---

--- task ---

**Test** 

When you make a change to a code block in the code editor panel, the simulator will restart.

You should now hear the melody playing until it's done (and then looping because of the forever loop).

--- /task ---    

Well done, you have created your first music program on a micro:bit!
