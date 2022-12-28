---
id: 177
title: 'Experiment 5 de versnellingsmeter en motor controle'
date: '2019-03-04T08:16:47+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=177'
permalink: /de-versnellingsmeter/
image: /wp-content/uploads/2017/03/tom-eversley-86446-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# Een motor aansturen met een versnellingsmeter.

*De Microbit heeft een ingebouwde versnellingsmeter. Een magisch elektronisch onderdeel zo groot als een korrel rijst.*

<div class="wp-caption alignnone" id="attachment_244" style="width: 160px">![The need for speed](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/tom-eversley-86446.jpg?resize=150%2C150)The need for speed

</div>Een versnellingsmeter werkt dankzij kristalstructuren in die reageren op de versnelling. Deze kristallen krijgen bij beweging een miniscule elektrische lading die daarna gemeten kan worden.

Doelen van dit experiment. Je leert hoe je

- Een button gebruikt om een LED te laten branden
- Variabele weerstand gebruiken
- Een analoge voltage leest vanuit de variabele weerstand.

### Benodigdheden

- Male to female jumper draad 3x
- Transistor 1x
- Weerstand 2.2kΩ 1x
- Motor 1x
- Fan blade 1x
- Terminal connector 1x
- Breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

Na intensief te hebben gewerkt met de block editor maken we nu de overstap naar touch develop. Een vergelijkbare taal, nog steeds met blokken, maar nu meer op een geschreven taal gebaseerd. Het is even omschakelen, maar de taal is sneller te gebruiken door de combinatie van het toetsenbord en de muis.

<div class="wp-caption alignnone" id="attachment_195" style="width: 310px">![Experiment 5 versnellingsmeter](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Experiment_5_Touch_Develop_Code_main_-_BBC_micro_bit_🔊.png?resize=300%2C119 "Experiment 5 versnellingsmeter")Experiment 5 versnellingsmeter

</div>In de Microbit zit een versnellingsmeter (ook wel een accelerometer genoemd). Deze sensor kan de drie assen in een 3 dimensionale omgeving meten. Of beter gezegd, de relatieve verplaatsing. De versnelling en vertraging op de assen X, Y en Z worden gemeten met een -40% en + 40% op basis van -4G en -4G. Een G is een versnelling van 9,81 meter per seconde per seconden. Dit is de versnelling van een object dat naar de Aarde valt. Een nauwkeurige sensor! De X as is de lange zijde, de Y as de korte zijde. De Z as gaat omhoog/omlaag

Als de je sensor meet als de Microbit met het LED display naar boven ligt zul je het volgende meten.

- X = 0
- Y = 0
- Z = -1023

Dat komt doordat de op de assen X en Y er geen beweging of kracht uitgeoefend wordt. Op de Z as is een negatieve waarde te meten. De sensor zit achterop de Microbit gemonteerd. Hierdoor ligt de sensor omgekeerd.

#### Uitkomsten

De motor gaat uit als de Microbit plat op tafel ligt. (dat zie je ook goed in de video). Zodra de versnellingsmeter een verandering registreert zal de motor gaan draaien. Zoals je ziet beweegt de Microbit over de Y as.[ In deze YouTube over accelerometer kun je hier vinden](https://www.youtube.com/watch?v=i2U49usFo10)

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/83wtnIg1NZ8" width="560"></iframe>

##### MET DE CODE HIERONDER KUN JE DIRECT AAN DE SLAG!

```
<pre class="lang:js decode:true " title="Experiment 5 programmacode">from microbit import *

YTilt = 0

while True:
    YTilt = accelerometer.get_y()
    if YTilt <= 0:
        YTilt = 0
        pin0.write_analog(YTilt)
    else:
        pin0.write_analog(YTilt)
```