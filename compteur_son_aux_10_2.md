 ##Compteur musical
Programme le micro:bit pour que le nombre de pression s'affiche et qu'un son se fasse entendre chaque fois que ce nombre est un multiple de 10.

## @showdialog
## Avant de commencer
Supprime le bloc ``||basic:toujours||``.
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.


```blocks

let temps = 0
input.onButtonPressed(Button.A, function () {
    temps = 4
    for (let index = 0; index < 3; index++) {
        music.playTone(262, music.beat(BeatFraction.Quarter))
        basic.showNumber(temps - 1)
        basic.pause(100)
        temps += -1
    }
    music.playTone(392, music.beat(BeatFraction.Whole))
    basic.showString("Go")
})

```
