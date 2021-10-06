# Air:bit - tutorial

## Steg 1
Velg kategorien ``||variable:variabler||``. Lag en ny variabel som du kaller "Roll"

## Steg 2
Lag enda ``||variable:variabel||`` som du kaller "Pitch" 

## Steg 3

Hent ``||variable:sett Pitch||`` og plasser blokken i ``||basic:gjenta for alltid||`` Finn blokken ``||input:helningsvinkel () vinkel forover-bakover||`` fra kategorien ``||input:mer||`` under ``||input:inndata||`` og plasser den i ``||variable:sett Pitch||``.

```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
})
```
## Steg 4

Hent ``||variable:sett Roll||`` og plasser blokken i ``||basic:gjenta for alltid||`` Finn blokken ``||input:helningsvinkel () vinkel høyre-venstre||`` fra kategorien ``||input:mer||`` under ``||input:inndata||`` og plasser den i ``||variable:sett Roll||``. Du må endre i nedtrekksmenyen på ``||input:helningsvinkel () vinkel forover-bakover||`` for å få  ``||input:(høyre-venstre)||``.

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

Lag en ny ``||variable:variabel||`` som du kaller "Throttle". 

## Steg 7

Hent ``||variable:endre Throttle||`` og plasser den i ``||input:Når knapp B trykkes||``. Sett ``||variable:endre Throttle||`` til 5.

```blocks
input.onButtonPressed(Button.B, function () {
    Throttle += 5
})
```

## Steg 8

Hent ``||logic:Hvis <sann> så - ellers||``  fra ``||logic:logikk||`` og plasser den i ``||input:Når knapp B trykkes||``
```blocks
input.onButtonPressed(Button.B, function () {
    Throttle += 5
    if (true) {
    	
    } else {
    	
    }
})
```

## Steg 9

Hent ``||logic:0 < 0||`` fra ``||logic:logikk||`` og plasser den der det står ``||logic:sann||`` i ``||logic:Hvis <sann> så - ellers||``
```blocks
input.onButtonPressed(Button.B, function () {
    Throttle += 5
    if (0 < 0) {
    	
    } else {
    	
    }
})
```

## Steg 10

Hent en rund ``||variables:Throttle||`` blokk fra ``||variables:variabler||`` og sett den inn isteden for den første 0 i ``||logic:0 < 0||`` som du satte inn i  ``||logic:Hvis <sann> så - ellers||``
```blocks
input.onButtonPressed(Button.B, function () {
    Throttle += 5
    if (Throttle < 0) {
    	
    } else {
    	
    }
})
```
## Steg 11

Endre slik at det står ``||variables:Throttle||`` ``||logic:<||`` 40 i ``||logic:Hvis <sann> så - ellers||``
```blocks
input.onButtonPressed(Button.B, function () {
    Throttle += 5
    if (Throttle < 40) {
    	
    } else {
    	
    }
})
```
## Steg 12

Flytt blokken ``||variables:endre Throttle med 5||`` til den første åpningen i blokken ``||logic:Hvis <sann> så - ellers||`` 
```blocks
input.onButtonPressed(Button.B, function () {
    if (Throttle < 40) {
    Throttle += 5	
    } else {
    	
    }
})
```

## Steg 13

Hent en ny ``||variables:endre Throttle||`` og plasser den under ``||logic:ellers||`` i blokken ``||logic:Hvis <sann> så - ellers||``. Sett ``||variables:endre Throttle||`` som du nettopp hentet til 1
```blocks
input.onButtonPressed(Button.B, function () { 
    if (Throttle < 40) {
    Throttle += 5	
    } else {
    Throttle += 1	
    }
})
```

## Steg 14

Merk ``||input:Når knapp B trykkes||`` og høyreklikk med musepekeren. Velg "Lag kopi" for å lage en kopi av hele blokken. Når du har fått en kopi, endrer du den fra å være ``||input:Når knapp B trykkes||`` til ``||input:Når knapp A trykkes||``
```blocks
input.onButtonPressed(Button.A, function () { 
    if (Throttle < 40) {
    Throttle += 5	
    } else {
    Throttle += 1	
    }
})
input.onButtonPressed(Button.B, function () { 
    if (Throttle < 40) {
    Throttle += 5	
    } else {
    Throttle += 1	
    }
})
```

## Steg 15

Når vi trykker knapp A vil vi minske farten på rotorene. Derfor endrer vi verdien i ``||variables:endre Throttle med||`` fra 5 til -5 og ``||variables:endre Throttle med||` fra 1 til - 1 som står i ``||input:Når knapp A trykkes||``
```blocks
input.onButtonPressed(Button.A, function () { 
    if (Throttle < 40) {
    Throttle += -5	
    } else {
    Throttle += -1	
    }
})
```