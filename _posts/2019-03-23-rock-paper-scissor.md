---
id: 430
title: 'De tien van Ramon: <br>Rock, Paper &#038; Scissor met score module.'
date: '2019-03-23T10:26:42+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=430'
permalink: /rock-paper-scissor/
twitterCardType:
    - summary_large_image
image: /wp-content/uploads/2017/03/maarten-van-den-heuvel-73124-88x88.jpg
categories:
    - 'Aan de slag'
    - 'De tien van Ramon'
    - Experimenten
---

# Hoe werkt een rock, paper &amp; scissor?

<span style="color: #808080;">*One player versie*</span>

![](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/rock-paper-scissors-156171_640.png?resize=150%2C150)Rock, paper &amp; scissor is een eenvoudig spelletje met een kleine waarheidstabel. Met behulp van drie keuzemogelijkheiden, altijd 1-1, kun je winnen, verliezen of een gelijkstand krijgen. De gelijkstand zie je in de tabel hieronder met een kruisje. Ook zie je in de tabel hieronder wat de score is met een winnaar/verliezer. De winnaar zie je in de tabel hieronder.

[Bewerken](http://microbit.studio/wp-admin/tools.php?page=tablepress&action=edit&table_id=2)
|  | Schaar | Steen | Papier |
|---|---|---|---|
| Schaar | x | Steen | Schaar |
| Steen | Steen | x | Papier |
| Papier | Schaar | Papier | x |

## Hoe werkt de programmacode van rock, paper, scissor?

In dit experiment maken we weer gebruik van een variabele. Deze noemen we keuze. In deze variabele kunnen drie waardes voorkomen. 0, 1 en 2. Valt de random keuze op een van deze drie getallen dan wordt er een bijpassend plaatje getoond. Met behulp van de A button kun je een score bijhouden. Met behulp van button A+B wordt de score weer op nul teruggezet.

### **Stap 1 – vormgeven iconen**

We beginnen met het maken van een steen. Maak met SHOW LEDS deze steen na. Daarna maken we ook papier en schaar.

<div class="wp-caption alignleft" id="attachment_444" style="width: 133px">![](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊-2.png?resize=123%2C102)Schaar

</div><div class="wp-caption alignleft" id="attachment_443" style="width: 127px">![](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊-1.png?resize=117%2C100)Papier

</div><div class="wp-caption alignleft" id="attachment_441" style="width: 127px">![](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊.png?resize=117%2C96)Steen

</div>### **Stap 2 – If then keuzes**

Na het maken van de bovenstaande figuren maken we nu de keuzemogelijkheid om na een willekeurig getal tussen de 0-2 (dus nul-één-twee) een figuur te laten zien. Bouw daarom onderstaande figuur na. Het werkt als volgt;

- On shake 
    - Hiermee gaat een proces starten bij het schudden van de Microbit.
- <span style="color: #ff0000;">Set KEUZE</span> to <span style="color: #993366;">Pick random 0 to 2</span>
    - Met deze regel zetten we de variabele Keuze open voor drie verschillende mogelijkheden. Tussen de 0-2
- <span style="color: #339966;">If Keuze = 0 then</span>
    - Met deze regel wordt een keuze gemaakt. Bij het getal 0 uit de variabele keuze wordt hieronder de steen zichtbaar.

<div class="wp-caption alignleft" id="attachment_448" style="width: 240px">![Stap 2 RPS](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊-3.png?resize=230%2C172)Stap 2 RPS

</div>### **Stap 3 – een compleet programma** 

We maken met behulp van onderstaande de basis van rock, paper, scissor af. Bij een random waarde in de variabele KEUZE van 1 laat de Microbit papier zien. Bij het getal 2 een schaar.

<div class="wp-caption alignleft" id="attachment_449" style="width: 186px">![RPS - stap 3](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊-4.png?resize=176%2C300)RPS – stap 3

</div>### **Stap 4 – score toevoegen**

We hebben het nu een basisspelletje gemaakt. Nu volgt de verdieping. De score van het spel gaan we bijhouden. Bij het indrukken van Button A gaat de score met 1 omhoog. Button A+B tegelijkertijd ingedrukt geeft een score reset.

<div class="wp-caption alignleft" id="attachment_450" style="width: 182px">![Rock, paper & scissor. Stap 4](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊-5.png?resize=172%2C84)Rock, paper &amp; scissor. Stap 4

</div><div class="wp-caption alignleft" id="attachment_451" style="width: 160px">![Rock, paper & scissor. Stap 4 score reset](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/RPS_-_pxt_microbit_org_🔊-6.png?resize=150%2C48)Rock, paper &amp; scissor. Stap 4 score reset

</div>## Uitdagingen Rock, paper &amp; scissor

We hebben nu een 1 player game gemaakt. Compleet met score module! Kun je een score module maken voor een 2 player game? Hoe laat je zien dat een speler heeft gewonnen bij 5 punten? **Dubbele uitdaging;** kun je twee Microbits met elkaar laten communiceren? Volledige 2 player mode 🙂

### Met onderstaande programmacode kun je direct aan de slag!

```
<pre class="theme:1c-kod lang:js decode:true" title="De tien van Ramon: rock, paper & scissor">let Score = 0
let keuze = 0
input.onGesture(Gesture.Shake, () => {
    keuze = Math.random(3)
    if (keuze == 0) {
        basic.showLeds(`
            . . . . .
            . # # # .
            . # # # .
            . # # # .
            . . . . .
            `)
    }
    if (keuze == 1) {
        basic.showLeds(`
            # # # # #
            # . . . #
            # . . . #
            # . . . #
            # # # # #
            `)
    }
    if (keuze == 2) {
        basic.showLeds(`
            # # . . #
            # # . . .
            . . # . .
            # # . # .
            # # . . #
            `)
    }
})
input.onButtonPressed(Button.AB, () => {
    Score = 0
})
input.onButtonPressed(Button.A, () => {
    Score += 1
    basic.showNumber(Score)
})
```