---
id: 164
title: 'Experiment 4 Met een transistor een motor schakelen'
date: '2019-03-02T19:11:55+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=164'
permalink: /microbit-en-transistor/
image: /wp-content/uploads/2017/03/rodion-kutsaev-24833-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# En nu wordt het leuk! Introductie van de transistor

*Maak een schakeling om een een hoge voltage te schakelen met een transistor.*

***UPDATE:** Klik [hier](#update) voor een update.*

Doelen van dit experiment. Leer je hoe

- Je hoe een transistor werkt
- Een schakeldraad te gebruiken (met een laag voltage)
- Je snelheid te reguleren met behulp van een PWM (Pulse Width Modulation)

### Benodigdheden

- transistor 1 x
- male to female jumper draad 3x
- Motor 1x
- Ventilatorblad 1x
- Terminal connector 1x
- Weerstand 2.2kΩ 1x
- breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

We gebruiken blokken uit <span style="color: #008080;">Basic</span>, <span style="color: #333399;">Logic</span>, <span style="color: #339966;">Loops</span>, <span style="color: #3366ff;">Math</span>, <span style="color: #993300;">Pins</span> en <span style="color: #993366;">Variables</span>. Bouw met onderstaande afbeelding deze sketch na. Met de bovenste set\[Duty\] to \[0\] geef je de sketch een beginwaarde mee. Daarna wordt deze variabele in de forever-loop veranderd.

!["Microbit](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Block_Editor_-_BBC_micro_bit_🔊.png?resize=300%2C296 "Experiment 3 Een LED dimmer")

De Mircobit kan alleen een lage hoeveelheid voltage leveren. Daarom gebruiken we een transistor om een schakelaar te maken tussen de 3 Volt en de motor. Je zou het kunnen vergelijken met een schakelaar zonder een knopje. Door op het meest linker pootje een lage spanning te zetten kun je schakelen.

#### Uitkomsten

De motor begint langzaam met draaien en gaat steeds sneller draaien totdat de maximale snelheid is bereikt. Op dat punt stopt de versnelling en gaat de motor terug naar stilstand. Zodra de motor stilstaat begint het proces weer vooraf aan. Wil je meer weten over de grootste revolutie in onze geschiedenis? [In deze YouTube video leer je er meer over in 8 minuten.](https://www.youtube.com/watch?v=OwS9aTE2Go4)

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/d49xyHy1KnA" width="560"></iframe>

##### UPDATE <a name="update"></a>

> Let goed op met het uitlijnen van de transistor en de terminal end connector. Door een foutje werkte de transistor niet en werd er direct 3 volt op de motor geschakeld. Gelukkig werkt de motor nog en is er geen schade. Nu werkt de sketch zoals de bedoeling was.

##### MET DE CODE HIERONDER KUN JE DIRECT AAN DE SLAG!

```
<pre class="lang:js decode:true " title="Experiment 4 programamcode">from microbit import *

Duty = 0

while True:
    while Duty < 1023:
        pin0.write_analog(Duty)
        Duty += 1

    while Duty > 0:
        pin0.write_analog(Duty)
        Duty -= 1
```