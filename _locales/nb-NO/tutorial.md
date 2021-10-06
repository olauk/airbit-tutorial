# Air:bit - tutorial

## Steg 1
Velg kategorien ``||variable:variabler||``. Lag en ny variabel som heter "Roll"

## Steg 2
Lag enda variabel som heter "Pitch" 

## Steg 3

Hent ``||variable:sett Pitch||`` og plasser blokken i ``||basic:gjenta for alltid||`` Finn blokken ``||input:helningsvinkel () vinkel forover-bakover||`` fra kategorien ``||input:mer||`` under ``||input:inndata||`` og plasser den i ``||variable:sett Pitch||``.

```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
})
```
## Steg 4

Hent ``||variable:sett Roll||`` og plasser blokken i ``||basic:gjenta for alltid||`` Finn blokken ``||input:helningsvinkel () vinkel venstre-høyre||`` fra kategorien ``||input:mer||`` under ``||input:inndata||`` og plasser den i ``||variable:sett Roll||``. Du må endre i nedtrekksmenyen på ``||input:helningsvinkel () vinkel forover-bakover||`` for å få  ``||input:(venstre-høyre)||``.

```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
})
```
## Steg 5

Hent inn blokken ``||input:Når knapp A trykkes||`` og plasser den ved siden av ``||basic:gjenta for alltid||`` Endre ``||input:Når knapp A trykkes||`` til knapp B

```blocks
input.onButtonPressed(Button.B, function () {

})
```

## Steg 6

Lag en ny variabel som heter "Throttle". 

## Steg 7

Hent ``||variable:endre Throttle||`` og plasser den i ``||input:Når knapp B trykkes||``. Sett ``||variable:endre Throttle||`` til 5.

```blocks
input.onButtonPressed(Button.B, function () {
    Throttle += 5
})
```