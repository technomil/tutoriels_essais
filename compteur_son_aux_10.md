 ##Compteur musical
Programme le micro:bit pour que le nombre de pression s'affiche et qu'un son se fasse entendre chaque fois que ce nombre est un multiple de 10.

## @showdialog
## Avant de commencer
Supprime le bloc ``||basic:toujours||``.
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.


```blocks
basic.onStart(function ()
```

## Étape 1

Ajoute le bloc ``||basic:montrer le nombre zéro||`` dans le bloc ``||basic:au démarrage||``.

```blocks
basic.showNumber(0)
```
## Étape 2

Glisse le bloc ``||input:lorsque le bouton A est pressé||``.

```blocks
input.onButtonPressed(Button.A, function () {
   
```
## Étape 3

Clique sur ``||variables: variable||``
#### Clique ensuite sur créer une variable et donne-lui le nom "compter".

## Étape 4
Glisse le bloc ``||variables:modifier compter de||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.


```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    
```
## Étape 5
Glisse le bloc ``||basic:montrer nombre||`` sous le bloc ``||variables:modifier compter de||``.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(0)
   
    ```

 ## Étape 6  
Glisse le bloc ``||variables:compter||`` dans le bloc ``||basic:montrer nombre||``.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    ```

## Étape 7
Ajoute le bloc ``||logic:si vrai ... alors ||`` sous le bloc ``||basic:montrer nombre||``.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if ( true ) {

```

## Étape 8
Remplace le mot vrai par le bloc ``||logic:0 = 0 ||``.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if (0 == 0) {
    
```

## Étape 9
Remplace le nombre 0 par le bloc mauve ``||maths:remainer of 0/1 ||``.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if (0 % 1 == 0) {
    
```

## Étape 10

Remplace le chiffre premier chiffre 0 du  bloc mauve ``||maths:remainer of 0/1 ||`` par ``||variables:compter||`` .

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if (count % 10 == 0) {
   
```

## Étape 11
Remplace le chiffre 1 du  bloc mauve ``||maths:remainer of 0/1 ||`` par le nombre 10.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if (0 % 10 == 0) {
    ```

    
## Étape 12
Ajoute le bloc ``||music:jouer mélodie au tempo 120bpm jusqu'à la fin||`` dans le bloc ``||logic:si vrai ... alors ||``
### Compose une mélodie en cliquant sur la note de musique.

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if (count % 10 == 0) {
        music.playMelody("C D E F G A B C5 ", 120)
    }
})
```

```blocks
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
    if (count % 10 == 0) {
        music.play(music.stringPlayable("- - - - - - - - ", 120), music.PlaybackMode.UntilDone)
    }
})


## Bravo! Tu as terminé!
Tu sais maintenant comment créer un compteur musical!
