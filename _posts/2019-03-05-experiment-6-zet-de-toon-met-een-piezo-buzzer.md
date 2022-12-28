---
id: 179
title: 'Experiment 6 Zet de toon met een Piezo buzzer'
date: '2019-03-05T07:24:19+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=179'
permalink: /experiment-6-zet-de-toon-met-een-piezo-buzzer/
image: /wp-content/uploads/2017/03/matt-botsford-197870-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# *Met behulp van een Piezo buzzer muziek maken met je Microbit!* 

<div class="wp-caption alignleft" id="attachment_235" style="width: 160px">![Zet de toon met de Buzzer!](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/matt-botsford-197870.jpg?resize=150%2C150)Zet de toon met de Buzzer!

</div>De buzzer zet een elektrisch signaal om in een geluid. Beperkt tot een aantal muzieknoten; sommige zelfs maar tot een noot.

Doelen van dit experiment. Je leert hoe je

- Een buzzer werkt
- Muziek maakt met
- Een proces start met de druk van een button

### Benodigdheden

- Male to female jumper draad 2x
- Buzzer 1 x
- Terminal connector 1x
- Breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

Dit is al het tweede experiment dat we maken met het Touch develop script. Ik vind het een mooie uitdaging om vanuit een idee rechtstreeks naar programmacode te gaan. De interface is wel even wennen, maar daarna kun je ‘gewoon’ doorwerken.

<div class="wp-caption alignnone" id="attachment_212" style="width: 310px">![Experiment 6 de Buzzer](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Experiment_6_Touch_Develop_Code_main_-_BBC_micro_bit_🔊.png?resize=300%2C153 "Experiment 5 versnellingsmeter")Experiment 6

</div>#### Uitkomsten

Met behulp van bovenstaande code kunnen we een geluid produceren uit de Buzzer. Veel van de code is te begrijpen door het te lezen. Het begin met het aanmaken van een functie (main). Binnen deze functie wordt een output pin gedefinieerd. Op de regel erna wordt gekeken naar een input signaal van button A. Zodra button A is ingedrukt wordt er een DO uitgevoerd. Er komt een signaal op de button (P0).

De getallen 400 en 500 gaan respectievelijk over de toonhoogte (frequentie) en de lengte van het geluid. In dit geval zal er een beep te horen zijn voor 500 miliseconde (een 1/2 seconde).

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/V8Iw2upnw8w" width="560"></iframe>

## Meer informatie

Met onderstaande link kun je in 15 minuten [Starwars muziek uit je ](https://www.youtube.com/watch?v=Y32FhgOVZnM&t=122s)Microbit laten klinken. Het kan met de onderdelen die bovenin genoemd worden gebouwd worden. Alleen je eigen Dark Father toevoegen. Vader en dochter hebben veel plezier met het maken van deze video. Kijk de video en leer ook nog iets over de muziektheorie.

<div class="wp-caption alignnone" id="attachment_213" style="width: 310px">[![Microbit Monsters. Starwars muziek met een buzzer](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Episode_4_-_playing_Star_Wars_music_on_your_BBC_MicroBit_-_YouTube_🔊.png?resize=300%2C48)](https://www.youtube.com/watch?v=Y32FhgOVZnM&t=122s)[Microbit Monsters. Starwars muziek met een ](https://www.youtube.com/watch?v=Y32FhgOVZnM&t=122s)

</div>Je omgeving niet storen met gebeep? Met deze[ handleiding sluit je oordopjes ](https://www.microbit.co.uk/blocks/lessons/hack-your-headphones/activity)aan op je Microbit.

<div class="wp-caption alignnone" id="attachment_214" style="width: 160px">[![Microbit en oordopjes](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/lekeqjzq.png?resize=150%2C150)](https://www.microbit.co.uk/blocks/lessons/hack-your-headphones/activity)[Microbit en oordopjes](https://www.microbit.co.uk/blocks/lessons/hack-your-headphones/activity)

</div>##### MET DE CODE HIERONDER KUN JE DIRECT AAN DE SLAG!

```
<pre class="lang:js decode:true " title="Experiment 5 programmacode">from microbit import *

import music

while True:
    if button_a.is_pressed():
        music.pitch(400,500)
```