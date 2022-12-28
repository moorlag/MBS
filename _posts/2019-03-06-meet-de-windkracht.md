---
id: 181
title: 'Experiment 7 Meet de windkracht'
date: '2019-03-06T09:00:10+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=181'
permalink: /meet-de-windkracht/
image: /wp-content/uploads/2017/03/karsten-wurth-104653-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# *Windkracht meten*

Met de Microbit en een motor kun je ook de windkracht meten. Met dit experiment leer je hoe dit eenvoudig zelf te bouwen is.

<div class="wp-caption alignleft" id="attachment_233" style="width: 160px">![Windkracht. Met de Microbit gaan we het meten](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/karsten-wurth-104653.jpg?resize=150%2C150)Windkracht. Met de Microbit gaan we het meten

</div>De motor en ventilatorbladen kunnen ook ingezet worden als een windsnelheidsmeter. Hiermee kunnen we de windkracht meten. Wind turbines zetten kinetische energie om in elektrische energie. In dit experiment zorgt de motor voor de energie. Het opgewekte vermogen kunnen we inzichtelijk maken met behulp van het LED scherm. Hoe hard kun jij blazen? Meet je windkracht!

Doelen van dit experiment. Je leert hoe je

- Een motor energie kan opwekken
- Het opgewekte vermogen kunt meten
- Hoe je een variabele in Toch Develop script kunt uitlezen

### Benodigdheden

- Male to female jumper draad 2x
- Male to male jumper draad 1x
- Motor 1 x
- Ventilator blad 1x
- 22kΩ weerstand 1x
- Terminal connector 1x
- Breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

Dit is het derde experiment dat we gaan maken met Touch Develop. Zoals je hieronder in de afbeelding ziet maken we een functie Main(). Daarbinnen wordt een variable (var) vastgelegd; Highest. In Highest wordt straks de waarde van het vermogen opgeslagen. De hoogste waarde wel te verstaan.

In een forever loop lezen we pin P0 uit. Als de waarde (&gt;) hoger is dan de vorige gemeten waarde dan wordt dat de nieuwe Highest. Als dat (else) niet het geval is dan wordt de vorige waarde opgeslagen. Zodra Button A ingedrukt wordt wordt de variable uitgelezen in het LED scherm.

#### Uitkomsten

Zodra de programmacode op de Microbit staat kun je beginnen te blazen. Nadat je op Button A drukt laat de Microbit de hoogst gemeten waarde zien. Nadat je op reset drukt begint het meten weer opnieuw. **Let op!** Pin P0 is erg gevoelig en zal altijd een waarde laten zien tussen de 1 en 5. Dat komt omdat het de motor al snel een heel klein beetje spanning opwekt. Hoe hard moet je blazen voor 500? En voor 1000? Wat zal de maximale waarde zijn?

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/7u9MpORLgx0" width="560"></iframe>

## Meer informatie

##### MET DE CODE HIERONDER KUN JE DIRECT AAN DE SLAG!

```
<pre class="lang:js decode:true" title="Experiment 7 programmacode">from microbit import *

Value = 0
Highest = 0

while True:
    Value = pin0.read_analog()
    if Value > Highest:
        Highest = Value

    if button_a.is_pressed():
        display.scroll(str(Highest))
```