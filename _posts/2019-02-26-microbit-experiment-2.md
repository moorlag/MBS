---
id: 68
title: 'Experiment 2 LDR &#038; Analoge input'
date: '2019-02-26T11:28:31+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=68'
permalink: /microbit-experiment-2/
primer_layout:
    - one-column-wide
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# Gebruik lichtgevoelige sensor en analoge input.

*Met een Light Dependent Resistors of licht gevoelige weerstand is de weerstand afhankelijk van de hoeveelheid licht dat op de sensor valt. In dit experiment gaan we het testen met de Micro:Bit*

*Meer licht is minder weerstand. Met een LDR kun je dus de omgeving meten. Daarom heet het een sensor. Weerstand is een term uit de electronica. Energie door een kabel kun je vergelijken met een beekje. Het kan hard stromen, langzaam stromen en zelfs in pulsen stromen. Weerstand is de breedte van een beekje. Kan er veel of weinig water doorheen stromen.*

*Ook kijken we naar analoge input. Het omgekeerde van analoog is digitaal. Digitaal kent twee waarden; aan of uit. (1 of 0). Zoals met een lichtschakelaar. Het licht is aan of uit. Analoog kun je vergelijken met een dimmer. Een draai aan de dimmer en het licht gaat feller of zwakker branden. [Hoe werkt een LDR?](https://www.kitronik.co.uk/blog/how-an-ldr-light-dependent-resistor-works/)*

## Doelen van dit experiment op Micro:Bit

- Een LDR gebruiken als sensor
- Een LDR gebruiken als analoge input
- Een ’threshold’ (kantelpunt) gebruiken om een zon of maan te laten schijnen

### Benodigdheden

- LDR 1x
- 10kΩ weerstand 1x
- Male to female jumper wire 3x
- breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

We gebruiken bij dit experiment meer blokken. Met behulp van de afbeelding onderaan deze paragraaf kun je zien hoe se sketch eruit komt te zien. We gebruiken de volgende blokken; op basis van de kleur kun je in de gereedschapskist zien in welk blok de commando’s zitten

- <span style="color: #008080;">Basic</span>
    - forever en show LEDs
- <span style="color: #333399;">Logic</span>
    - If do en \[\]=\[\]
- <span style="color: #0000ff;">Math</span>
    - 0 (getal)
- <span style="color: #993300;">Pins (kijk bij Advance!)</span>
    - Analog read pins
- <span style="color: #800080;">Variables</span>
    - Set item to en item

**Let op!** Zorg ervoor dat je bij ‘on button A pressed’ **niet** twee keer gebruikt. Natuurkijk kies je bij de string voor ‘on button B pressed’. De afbeelding bij button A is natuurlijk helemaal vrij. Net zoals de tekst in de string bij button B.

<div class="wp-caption alignleft" id="attachment_72" style="width: 200px">![Experiment 2 Micro:Bit en LDR](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/02/Block_Editor_-_BBC_micro_bit.png?resize=190%2C300 "Experiment 2 Micro:Bit en LDR")Experiment 2 Micro:Bit en LDR

</div>#### Uitkomsten

Na het uploaden van de programmacode via een .hex bestand kon de Micro:Bit een analoge input lezen. Door de weerstand en de LDR in serie te schakelen wordt de 3 volt verdeeld. De verdeling is afhankelijk van de relatieve weerstand. Als de weerstand gelijk is (weerstand en de LDR) dan wordt het voltage ook gelijk verdeeld. Als er meer licht op de LDR valt gaat de weerstand naar beneden. Met andere woorden dan krijgt de P0 meer vermogen tot zijn beschikking en gaat er een zonnetje branden. De analoge variabele kan een input verwerken van 0 tot 1023. Met een variabele weerstand op de LDR ingesteld op 512 zal er +/- 1.5 Volt op P0 terecht komen. ❤️️ LDR

##### Hieronder tref je de gebruikte code.

<div class="wp-caption alignnone" id="attachment_73" style="width: 310px">![Programmacode Micro:Bit experiment 2](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/02/Experiment_2_Block_Editor_Code__converted__2_main_-_BBC_micro_bit.png?resize=300%2C272 "Programmacode Micro:Bit experiment 2")Programmacode Micro:Bit experiment 2

</div><iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/M2n-2Q2N6xk" width="560"></iframe>