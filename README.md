# Loops-Demos
input.onGesture(Gesture.Shake, function () {
    while (!(input.buttonIsPressed(Button.A))) {
        for (let i = 0; i < 2; i++) {
            music.playTone(262, music.beat(BeatFraction.Half))
            music.playTone(523, music.beat(BeatFraction.Half))
        }
    }
})
let xindex = 0
basic.forever(function () {
    for (let yindex = 0; yindex <= 4; yindex++) {
        for (let xindex = 0; xindex <= 4; xindex++) {
            led.plot(xindex, yindex)
            basic.pause(100)
            led.unplot(xindex, yindex)
            basic.pause(100)
        }
    }
})
