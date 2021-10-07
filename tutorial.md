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
TIPS: Hold inne CTRL tasten for å flytte en blokk midt i koden.
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

Når vi trykker knapp A vil vi minske farten på rotorene. I ``||input:Når knapp A trykkes||`` endrer vi derfor verdien i ``||variables:endre Throttle med||`` fra 5 til -5 og ``||variables:endre Throttle med||`` fra 1 til - 1.
```blocks
input.onButtonPressed(Button.A, function () { 
    if (Throttle < 40) {
    Throttle += -5	
    } else {
    Throttle += -1	
    }
})
```

## Steg 16

For å armere dronen skal vi trykke A og B knappene samtidig. Hent inn ``||input:Når knapp A trykkes||`` og endre den til ``||input:Når knapp A+B trykkes||``.

```blocks
input.onButtonPressed(Button.AB, function () {
	
})
```

## Steg 17

Lag en ny ``||variables:variabel||`` som du kaller "Arm"

## Steg 18

Hent blokken ``||logic:Hvis <sann> - så ellers||`` fra ``||logic:logikk||`` og plasser den i ``||input:Når knapp A+B trykkes||``
```blocks
input.onButtonPressed(Button.AB, function () {
	if (true) {
    	
    } else {
    }
})
```


## Steg 19

Hent den runde blokken ``||variables:Arm||`` fra ``||variables:variabler||`` og plasser den der det står "sann" i ``||logic:Hvis <sann> - så||``
```blocks
input.onButtonPressed(Button.AB, function () {
	if (Arm) {
    	
    } else {
    }
})
```

## Steg 20

Hent inn en ``||variables:sett Arm til||`` og plasser den under ``||logic:Hvis Arm så||``. Sett ``||variables:sett Arm til||`` til 0. Hent inn en ny ``||variables:sett Arm til||``, plasser den under ``||logic:ellers||`` og sett den til 1.
```blocks
input.onButtonPressed(Button.AB, function () {
	if (Arm) {
    	Arm = 0
    } else {
        Arm = 1
    }
})
```

## Steg 21

Når vi trykker A + B vil vi også at Throttle skal settes til 0. Hent derfor inn ``||variables:sett Throttle til||`` og plasser den under ``||logic:Hvis <sann> - så ellers||`` i ``||input:Når knapp A+B trykkes||``
```blocks
input.onButtonPressed(Button.AB, function () {
	if (Arm) {
    	Arm = 0
    } else {
        Arm = 1
    }
    Throttle = 0
})
```

## Steg 22

For å lage en nødstopp skal vi bruke blokken ``||input:Når ristes||`` fra ``||input:inndata||``
I den skal vi legge ``||variables:sett Arm til||`` og ``||variables:sett Throttle til||``. Begge disse settes til 0.

```blocks
input.onGesture(Gesture.Shake, function () {
    Arm = 0
    Throttle = 0
})
```

## Steg 23

For å vise om dronen er på eller av skal vi bruker skjermen. Først må vi undersøke om Arm = 1 (drone på) eller om Arm = 0 (drone av).
Vi skal da hente blokken ``||logic:Hvis <sann> - så||`` og sette den inn i ``||basic:gjenta for alltid||``.

```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    if (true) {
    }
})
```
## Steg 24

Hent en rund ``||variables:Arm||`` fra ``||variables:variabler||`` og plasser den inn der det står "sann" i ``||logic:Hvis <sann> - så||`` blokken du satte inn i ``||basic:gjenta for alltid||``.

```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    if (Arm) {
    }
})
```

## Steg 25

Hent blokken ``||led:tenn x <0> y <0>||`` fra kategorien ``||led:skjerm||`` og plasser den i ``||logic:Hvis <sann> - så||``.

```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    if (Arm) {
        led.plot(0, 0)
    }
})
```

## Steg 26

Hent blokken ``||basic:tøm skjerm||`` og plasser den under ``||variables:sett Roll til||`` i ``||basic:gjenta for alltid||``
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
})
```
## Steg 27

Hent en ny ``||led:tenn x <0> y <0>||`` og plasser den nederst i ``||basic:gjenta for alltid||``. 
For å vise Throttle på skjermen må vi bruke en spesiell blokk fra matematikk som heter "regn om". 
Hent ``||math:regn om <0> fra lav <0> til høy <1023> til lav <0> til høy <4>||`` fra ``||math:matematikk||`` og plasser den i ``||led:tenn x <0> y<0>||`` slik at det står ``||led:tenn x (0) y (regn om...)||``
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(0,0,1023,0,4))
})
```

## Steg 28

Hent en rund ``||variables:Throttle||`` blokk og plasser den først i "regn om" blokken slik at det står ``||led:tenn x (0) y (regn om ||`` ``||variables:Throttle||`` ``||led:fra lav <0> fra høy <1023> til lav <0> til høy<4>)||``
Endre tallene i "regn om" blokken slik at det står ``||led:tenn x (0) y (regn om ||`` ``||variables:Throttle||`` ``||led:fra lav <0> fra høy <100> til lav <4> til høy<0>)||``
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(Throttle, 0, 100, 4, 0))
})
```

## Steg 29

Hent en ny ``||led:tenn x <0> y <0>||`` og plasser den nederst i ``||basic:gjenta for alltid||``. 
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(Throttle, 0, 100, 4, 0))
    led.plot(0,0)
})
```

## Steg 30

Hent inn ``||math:regn om <0> fra lav <0> til høy <1023> til lav <0> til høy <4>||`` og plasser den i ``||led:tenn x <0> y <0>||`` slik at det står: ``||led:tenn x <regn om..> y<0>||`` 
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(Throttle, 0, 100, 4, 0))
    led.plot(Math.map(0,0,1023,0,4),0)
})
```

## Steg 31

Hent en rund ``||variables:Roll||`` blokk og plasser den først i "regn om" blokken slik at det står ``||led:tenn x (regn om ||`` ``||variables:Roll||`` ``||led:fra lav <0> fra høy <1023> til lav <0> til høy<4>) y(0)||``
Endre tallene i "regn om" blokken slik at det står ``||led:tenn x (regn om ||`` ``||variables:Roll||`` ``||led:fra lav <-45> fra høy <45> til lav <0> til høy<0>) y(0)||``
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(Throttle, 0, 100, 4, 0))
    led.plot(Math.map(Roll,-45,45,0,4),0)
    })
```
## Steg 32

Hent inn ``||math:regn om <0> fra lav <0> til høy <1023> til lav <0> til høy <4>||`` og plasser den i ``||led:tenn x <0> y <0>||`` slik at det står: ``||led:tenn x <regn om Roll ..> y<regn om ..>||`` 
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(Throttle, 0, 100, 4, 0))
    led.plot(Math.map(Roll,-45,45,0,4),Math.map(0,0,1023,0,4))
    })
```

## Steg 33
Hent en rund ``||variables:Pitch||`` blokk og plasser den først i den siste "regn om" blokken slik at det står ``||led:tenn x (regn om ||`` ``||variables:Roll||`` ``||led:fra lav <0> fra høy <1023> til lav <0> til høy<4>) y(regn om ||`` ``||variables:Pitch||`` ``||led:fra lav <0> fra høy <1023> til lav <0> til høy<4>)||``
Endre tallene i "regn om" blokken slik at det står ``||led:tenn x (regn om ||`` ``||variables:Roll||`` ``||led:.. ) y(regn om ``||variables:Pitch||`` ``||led:fra lav <-45> fra høy <45> til lav <0> til høy<4>))||``
```blocks
basic.forever(function () {
    Pitch = input.rotation(Rotation.Pitch)
    Roll = input.rotation(Rotation.Roll)
    basic.clearScreen()
    if (Arm) {
        led.plot(0, 0)
    }
    led.plot(0, Math.map(Throttle, 0, 100, 4, 0))
    led.plot(Math.map(Roll,-45,45,0,4),Math.map(Pitch,-45,45,0,4))
    })
```
