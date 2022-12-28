---
id: 32
title: 'Experiment 1 Hallo Wereld'
date: '2019-02-25T06:21:18+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=32'
permalink: /microbit-experiment-1/
primer_layout:
    - one-column-wide
image: /wp-content/uploads/2017/02/marcelo-quinan-78447-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
    - Kitronik
---

# Say ‘HALLO’ to the Micro:Bit.

*Met ‘Hello World’ wordt bijna iedere programeerlessenserie gestart. Met deze eenvoudige oefening kun je laten zien dat de computer luistert naar instructies en deze tot op de letter uitvoert. En nu gaan we dat proberen met de Micro:Bit. Aan het einde van dit experiment kun je zelf ook een Hello World maken. Kijk daarvoor verder in dit experiment.*

<div class="wp-caption alignleft" id="attachment_268" style="width: 160px">![Hallo Wereld!](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/02/marcelo-quinan-78447.jpg?resize=150%2C150)Hallo Wereld!

</div> *[Hier zie je in 35 verschillende talen hoe ‘hello world’ wordt geschreven. ](https://www.youtube.com/watch?v=zecueq-mo4M)*

## In dit experiment leer je

- Leer hoe je een afbeelding laat zien met behulp van de [Microsoft PXT.](https://pxt.microbit.org/?lang=en)
- Leer hoe je een string maakt met het ‘show string’ commando
- Leer hoe de een input kunt gebruiken.
- Leer hoe je een .hex file kunt downloaden
- Leer hoe je een .hex file upload naar de Micro:Bit

### Benodigdheden

- Push switch 2 x
- male to female jumper draad 4x
- breadboard 1x
- Edge connector breakout board for Micro:Bit 1x

### Aan de slag

We beginnen met twee twee basis elementen uit <span style="color: #0000ff;">Basic</span> en <span style="color: #993366;">Input. </span>Hiermee kun je de sketch maken zoals hieronder beschreven.

Zoals je ziet bij twee zitten alle blokken in de gereedschapskist. Deze kun je plaatsen bij drie. Ik heb gebruik gemaakt van twee verschillende blokken. Een uit het paarse deel en een uit het blauwe deel. Heb je alle stappen uitgevoerd? Klik op Download (1).. Een .hex file. Mocht het niet werken, hier kun je mijn versie downloaden. [Experiment 1.hex](https://drive.google.com/file/d/0B8QRT1GQejO5d2hMVktycVhEajA/view?usp=sharing). Verder werken met deze sketch? [Dat kan hier via de PXT editor](https://pxt.microbit.org/12213-58173-70847-52099).

**Let op!** Zorg ervoor dat je bij ‘on button A pressed’ **niet** twee keer gebruikt. Natuurkijk kies je bij de string voor ‘on button B pressed’. De afbeelding bij button A is natuurlijk helemaal vrij. Net zoals de tekst in de string bij button B.

<div class="wp-caption alignnone" id="attachment_38" style="width: 535px">![Experiment 1 Micro:Bit.studio](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/02/Experiment_1_-_pxt_microbit_org.png?resize=525%2C226 "Experiment 1 Micro:Bit.studio")Experiment 1 Micro:Bit.studio

</div>#### Uitkomsten

Na het uploaden van de programmacode kun je onderstaande functies gebruiken. Het is eenvoudig te gebruiken. Met weinig materiaal kon ik een smiley en een tekst in beeld krijgen. Ook heb ik gebruik gemaakt van twee extra buttons.  
<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/KwRaRZ3sgwc" width="560"></iframe>

##### Hieronder tref je de gebruikte code.

```
<pre class="lang:js decode:true " title="Experiment 2 broncode">input.onButtonPressed(Button.A, () => {
basic.showLeds(`
. # . # .
. # . # .
# . . . #
# . . . 
. # # # .
`)
})
input.onButtonPressed(Button.B, () => {
basic.showString("Hallo wereld!")
})

```