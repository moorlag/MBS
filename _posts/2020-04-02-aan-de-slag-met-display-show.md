---
id: 652
title: 'Plaatjes met Python'
date: '2020-04-02T11:17:46+00:00'
last_modified_at: '2022-12-28T00:00:00+00:00'
categories:
    - Experimenten
    - μPython
---

Plaatjes weergeven op je Microbit met Python, zou dat moeilijk zijn? We aan aan de slag met display.show! Er zijn een aantal beperkingen die je moet weten; er zijn maar 25 LEDjes.. dus een plaatje zal altijd bestaan uit grote pixels. Niet zoals op een iPhone met miljoenen pixels, de Microbit heeft er 25. De resolutie is 5×5 LEDs.

Met MicroPython kun je ‘eenvoudig’ plaatjes oproepen. Deze zitten al in de code. Door een code op te roepen wordt dat ene plaatje naar de Microbit gestuurd. Met onderstaande code maken we een smiley op de Microbit.

```
<pre class="wp-block-verse">from microbit import *
display.show(Image.HAPPY)
```

## Hoe werkt Display.show? 

Met display.show(waarde) zeggen we dat het object display iets moet laten zien (show). Door het gebruik van de haakjes laten we niet alles zien, maar alleen waarde ‘HAPPY’. Er is een hele lijst met onderdelen. Die laten ik hieronder zien, zoals je hieronder ziet zijn veel plaatjes voor de hand liggend.

- `Image.HEART`
- `Image.HEART_SMALL`
- `Image.HAPPY`
- `Image.SMILE`
- `Image.SAD`
- `Image.CONFUSED`
- `Image.ANGRY`
- `Image.ASLEEP`
- `Image.SURPRISED`
- `Image.SILLY`
- `Image.FABULOUS`
- `Image.MEH`
- `Image.YES`
- `Image.NO`
- Tijdstippen met een klok
    - `Image.CLOCK12`
    - `Image.CLOCK11`
    - `Image.CLOCK10`
    - `Image.CLOCK9`
    - `Image.CLOCK8`
    - `Image.CLOCK7`
    - `Image.CLOCK6`
    - `Image.CLOCK5`
    - `Image.CLOCK4`
    - `Image.CLOCK3`
    - `Image.CLOCK2`
    - `Image.CLOCK1`
- Richtingen voor een kompas
    - `Image.ARROW_N`
    - `Image.ARROW_NE`
    - `Image.ARROW_E`
    - `Image.ARROW_SE`
    - `Image.ARROW_S`
    - `Image.ARROW_SW`
    - `Image.ARROW_W`
    - `Image.ARROW_NW`
- `Image.TRIANGLE`
- `Image.TRIANGLE_LEFT`
- `Image.CHESSBOARD`
- `Image.DIAMOND`
- `Image.DIAMOND_SMALL`
- `Image.SQUARE`
- `Image.SQUARE_SMALL`
- `Image.RABBIT`
- `Image.COW`
- `Image.MUSIC_CROTCHET`
- `Image.MUSIC_QUAVER`
- `Image.MUSIC_QUAVERS`
- `Image.PITCHFORK`
- `Image.XMAS`
- `Image.PACMAN`
- `Image.TARGET`
- `Image.TSHIRT`
- `Image.ROLLERSKATE`
- `Image.DUCK`
- `Image.HOUSE`
- `Image.TORTOISE`
- `Image.BUTTERFLY`
- `Image.STICKFIGURE`
- `Image.GHOST`
- `Image.SWORD`
- `Image.GIRAFFE`
- `Image.SKULL`
- `Image.UMBRELLA`
- `Image.SNAKE`