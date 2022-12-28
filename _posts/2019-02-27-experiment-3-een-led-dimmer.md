---
id: 104
title: 'Experiment 3 Een LED dimmer'
date: '2019-02-27T20:12:57+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=104'
permalink: /experiment-3-een-led-dimmer/
image: /wp-content/uploads/2017/02/john-towner-154060-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# Een LED dimmen met een variable weerstand

*Maak een LED dimmer met behulp van een potentiometer of een variable weerstand.* Het is een traploos element. Met behulp van een schroevendraaier kun je de waarde van de weerstand aanpassen.

Doelen van dit experiment

- Leer hoe je een button gebruikt om een LED te laten branden
- Leer hoe je variabele weerstand gebruiken
- Leer hoe je een analoge voltage leest vanuit de variabele weerstand.

### Benodigdheden

- Push button 1 x
- male to female jumper draad 7
- Potentiometer (dimmer) 1 x
- LED 1x
- Weerstand 47Ω 1x
- breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

We gebruiken deze keer blokken uit Basic, Input, Logic, Math, Pins en Variables. Bouw met onderstaande afbeelding deze sketch na.

<div class="wp-caption alignnone" id="attachment_145" style="width: 310px">![Experiment 3 Een LED dimmer](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/02/Block_Editor_-_BBC_micro_bit-1.png?resize=300%2C256 "Experiment 3 Een LED dimmer")Experiment 3 Een LED dimmer

</div>Het experiment maakt gebruik van een ‘variabele’ om bij te houden wanneer een button ingedrukt is. Deze heet in bovenstaande voorbeeld ‘Light State’. Deze variabele heeft 2 standen. 0 = uit en 1 = aan. Er wordt geluisterd op pin P0. Zodra daarop een signaal komt krijgt ‘Light State’ de waarde 1. De LED mag dus aan. Met behulp van het ‘Forever’ block is er een continue proces dat kijkt naar de variabele ‘Light State’. Zodra deze 1 heeft gaat er iets bijzonders starten. Er wordt een analoge waarde geschreven van P1 naar P2. En de LED krijgt daarmee een variabele spanning. Des te lager de weerstand van de variabele weerstand, des te feller gaat de LED branden. De 47Ω weerstand zorgt ervoor dat de LED niet doorbrandt bij een te hoge spanning.

#### Uitkomsten

Met het draaien aan de variabele weerstand alleen gebeurt er niks. Eerst moet er op de button gedrukt worden. Daarna wordt de waarde van de variabele weerstand gemeten. Op basis van de gemeten waarde krijgt de LED een specifieke (maar analoge) hoeveelheid spanning.

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/U34NECojrcQ" width="560"></iframe>

##### Met de code hieronder kun je direct aan de slag!

<div class="wp-caption alignnone" id="attachment_146" style="width: 310px">![Experiment 3 programmacode](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/02/Experiment_3_Block_Editor_Code__converted__2_main_-_BBC_micro_bit.png?resize=300%2C265)Experiment 3 programmacode

</div>