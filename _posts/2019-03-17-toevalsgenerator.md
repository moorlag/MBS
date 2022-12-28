---
id: 363
title: 'De tien van Ramon: Toevalsgenerator'
date: '2019-03-17T13:15:43+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=363'
permalink: /toevalsgenerator/
twitterCardType:
    - summary_large_image
image: /wp-content/uploads/2017/03/mohammad-faruque-190945_jpg-88x88.png
categories:
    - 'Aan de slag'
    - 'De tien van Ramon'
    - Experimenten
---

In deze ‘Tien van Ramon’ maken we een toevalsgenerator. In eenvoudig Nederlands maken we een dobbelsteen! Eerst wat uitleg over een dobbelsteen, daarna uitleg over een toevalsgenerator. Als laatste bouwen we in PXT een toevalsgenerator en maken we dit zichtbaar met het LED-scherm.

# Hoe werkt een dobbelsteen?

Een dobbelsteen is in de meestal gevallen een kubusvormig object met op elk van de zijden een van de ogenaantallen 1 tot en met 6 maar daar zijn ook uitzonderingen op. Het kan ook zijn dat een dobbelsteen rond is of meerdere vlakken heeft. Net zoals met een ‘gewone’ dobbelsteen is de willekeur van groot belang.

Het woord dobbelsteen verwijst naar het oude spel dobbelen. De dobbelsteen kun je vergelijken met een toevalsgenerator die met gelijke kansen van 1/6 de getallen 1 t/m 6 voortbrengt.

## Hoe werkt een toevalsgenerator?

Een toevalsgenerator of randomfunctie zorgt voor een keuze uit een vooraf vastgesteld bereik. Een keuze die ‘per toeval’ tot stand komt. Waarbij ieder getal tussen die grenzen een evengrote kans maakt om te worden getrokken. Een toevalsgetal is dus onvoorspelbaar en in een lange reeks toevalsgetallen bestaat geen regelmaat of patroon en komt elk mogelijk getal ongeveer even vaak voor.

Het blijkt in de praktijk moeilijk een reeks toevalsgetallen te laten maken door een proefpersoon. Mensen hebben de neiging zich te laten leiden door ideeën over regelmaat en willekeur. Als gevolg daarvan worden reeksen als ‘2 2 2 2’ en ‘1 2 3 4’ al snel vermeden, terwijl in een reeks werkelijke toevalsgetallen ook dergelijke opeenvolgingen voorkomen. Een toevalsgenerator is een mechanisme of een algoritme dat zich niet door subjectieve overwegingen zoals willekeur laat leiden.

### Methoden

Er zijn meerdere methoden om een willekeurige keuze te maken. We bespreken er drie;

- Hogehoed 
    - De hoge hoed met lootjes is het klassieke voorbeeld van een eerlijke lotingsmethode. Er wordt een lootje uit de hoed gehaald zonder te kijken of te wisselen.
- Dobbelsteen 
    - Een goede mechanische toevalsgenerator is het gooien met een exact zuivere dobbelsteen: het resultaat van elke worp is onafhankelijk van de vorige worpen. Er is dus niets anders te voorspellen dan dat het nieuwe getal opnieuw zal liggen tussen de grenzen (1 en 6). Varianten zijn het werpen met een munt en het gebruik van “dobbelstenen” met andere aantallen zijden.
- Toeval met behulp van effecten uit de natuurkunde 
    - De genoemde methoden zijn lastig te gebruiken in apparaten en systemen. Daarom wordt er bij het werken met toevalsprocessen in wetenschappelijk onderzoek wel gebruikgemaakt van het verval van (licht)radioactief materiaal of kwantum effecten, zoals witte ruis, waarvan de theorie zegt dat deze volslagen aselect (at random) zijn. Een sensor meet deze effecten en genereert hiermee aselecte (random) getallen.

# **Opdracht**

We gaan een dobbelsteen maken! In de Micro:bit zit een versnellingssensor. In code is de conditie “shake”. Ook maken we kennis met ‘Pick random 0 to ..’.

### Programmacode met PXT

Er is een groot aantal blokken nodig om deze dobbelsteen te maken. We beginnen met <span style="color: #ff00ff;">ON SHAKE</span>. Deze kun je vinden in het menu <span style="color: #ff00ff;">INPUT</span>. Daarnaast moeten we nog een variabele maken. Zoals je hieronder kunt zien zit er een <span style="color: #ff0000;">functie</span> in. Daarna wordt er aan deze variabele een random variable toegevoegd. Variabelen vind je in het menu onder <span style="color: #ff0000;">VARIABELE</span>. In het menu <span style="color: #993366;">MATH</span> vind je <span style="color: #993366;">‘Pick random 0 to 0’. <span style="color: #000000;">Daarna hoef je alleen nog maar de laatste nul te vervangen door 5.</span></span> Waarom 0 tot 5? Dat lees je hieronder!

<div class="wp-caption alignnone" id="attachment_364" style="width: 310px">![Dobbelsteen stap 1](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/dice_roll_activity_-_Microsoft_MakeCode.png?resize=300%2C71)Dobbelsteen toevalsgenerator stap 1

</div>Met bovenstaande blokken wordt er al een willekeurig getal tussen in het bereik van nul tot vijf gekozen. Wij vinden dat tellen start bij één. Een computer begint te tellen bij nul. Vandaar dat het bereik nul tot vijf heeft.

We gebruiken een aantal <span style="color: #339966;">IF THEN ELSE</span> blokken. Deze kun je vinden in het menu onder <span style="color: #339966;">LOGIC</span>. Zoals je zit in de afbeelding hieronder ‘If Gooi = 5’ zie je in het LED scherm 6 ogen. Dit gaan we ook doen voor ‘If Gooi = 4’.

<div class="wp-caption alignnone" id="attachment_365" style="width: 267px">![Dobbelsteen stap 2](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-5.png?resize=257%2C300)Dobbelsteen stap 2

</div>Met bovenstaand instructie maak je ook de ‘If Gooi = 3’, ‘If Gooi = 2’ en ‘If Gooi = 1’. Voor de nul gebruiken we de ‘If then Else’.

![](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-6.png?resize=94%2C300 "De tien van Ramon - Forever")

Het laatste blokje om de één te gooien kun je maken met onderstaande afbeelding.

<div class="wp-caption alignnone" id="attachment_367" style="width: 232px">![Dobbelsteen stap 4](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-7.png?resize=222%2C275 "De tien van Ramon - On shake")Dobbelsteen stap 4

</div>Hieronder zie je hoe een variabele vastgesteld wordt.

<div class="wp-caption alignnone" id="attachment_344" style="width: 310px">![De tien van Ramon - variabele](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-4.png?resize=300%2C247 "De tien van Ramon - variabele")De tien van Ramon – variabele

</div>## Extra opdracht

Kun je ook een dobbelsteen maken die de woorden van de telling laat zien? (een, twee, drie)? Welke toepassing kun je nog extra bedenken voor een ‘dobbelsteen’?

Met onderstaande programmacode kun je direct aan de slag!

```
<pre class="theme:1c-kod lang:js decode:true" title="De tien van Ramon: Dobbelsteen">let gooi = 0
input.onGesture(Gesture.Shake, () => {
    gooi = Math.random(6)
    if (gooi == 5) {
        basic.showLeds(`
            . # . # .
            . . . . .
            . # . # .
            . . . . .
            . # . # .
            `)
    } else if (gooi == 4) {
        basic.showLeds(`
            . . . . .
            . # . # .
            . . # . .
            . # . # .
            . . . . .
            `)
    } else if (gooi == 3) {
        basic.showLeds(`
            . . . . .
            . # . # .
            . . . . .
            . # . # .
            . . . . .
            `)
    } else if (gooi == 2) {
        basic.showLeds(`
            # . . . .
            . . . . .
            . . # . .
            . . . . .
            . . . . #
            `)
    } else if (gooi == 1) {
        basic.showLeds(`
            . . . . .
            . # . . .
            . . . . .
            . . . # .
            . . . . .
            `)
    } else {
        basic.showLeds(`
            . . . . .
            . . . . .
            . . # . .
            . . . . .
            . . . . .
            `)
    }
})
```