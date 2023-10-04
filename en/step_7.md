## Upgrade your project

Great work! You have created your micro:bit music player. Here are some ideas to upgrade your project and create a more advanced music player app:

+ Add more melodies and increase the range on the shuffle
+ Use the Logo button (or button A+B on the V1) to stop all sounds, leaving Shake to just control the shuffle
+ Use the Logo button (or button A+B on the V1) to play a favourite melody

### Play ▶️

+ Use the logo at the top to select a favourite song 
+ How many tunes are there?
+ What happens if you press the logo after registering a favourite and changing the tune?

```microbit
input.onLogoEvent(TouchButtonEvent.LongPressed, function () {
    favourite = tune
})
input.onButtonPressed(Button.A, function () {
    music.stopAllSounds()
    tune += -1
    if (tune < 1) {
        tune = 7
    }
})
input.onButtonPressed(Button.B, function () {
    music.stopAllSounds()
    tune += 1
    if (tune > 7) {
        tune = 1
    }
})
input.onGesture(Gesture.Shake, function () {
    if (0 != 0) {
        music.stopAllSounds()
        tune = 0
    } else {
        tune = randint(1, 7)
    }
})
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    if (favourite == 0) {
        favourite = tune
    } else {
        tune = favourite
    }
})
let favourite = 0
let tune = 0
tune = 1
favourite = 0
basic.forever(function () {
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
    } else if (tune == 5) {
        basic.showIcon(IconNames.Heart)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Ode), music.PlaybackMode.UntilDone)
    } else if (tune == 6) {
        basic.showIcon(IconNames.Ghost)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Funk), music.PlaybackMode.UntilDone)
    } else if (tune == 7) {
        basic.showLeds(`
            # . # . #
            . # # # .
            . . # . .
            . # . # .
            # . . . #
            `)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Entertainer), music.PlaybackMode.UntilDone)
    }
})
```

<div>
<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
 <span style="color: #0faeb0">Mental Health Awareness week</span> is a campaign to raise understanding of mental health issues, promote good well-being, and break down stigma surrounding mental illness. This event has been recognised in various countries and is celebrated in May in the UK.
</p>
</div> 

[[[download-to-microbit]]]

[[[microbit-share]]]

Next, it is time to check what you have learnt!

--- collapse ---

---
title: Completed project
---

You can view the [completed project here](https://makecode.microbit.org/_5bFMMXWwjL6W){:target="_blank"}.

--- /collapse ---
