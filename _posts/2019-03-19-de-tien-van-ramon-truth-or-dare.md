---
id: 388
title: 'De tien van Ramon: Truth or dare'
date: '2019-03-19T13:50:06+00:00'
last_modified_at: '2022-12-30T00:00:00+00:00'
categories:
    - 'De tien van Ramon'
    - Experimenten
---

In deze ‘Tien van Ramon’ maken we een **‘Truth or Dare**‘ machine. In eenvoudig Nederlands maken we een apparaat dat iemand kan aanwijzen en ook nog zegt of het een truth of een dare moet beantwoorden!

# Wat is toevalsgenerator?

Een ‘Truth or dare’-machine werkt op basis van toeval. Computers (en ook de micro:bit) vinden toeval moeilijk. Een computer kan perfect dezelfde (exact dezelfde!) taak uitvoeren. Of het 1, 10 of 100 keer hetzelfde gebeurd, een computer kan met zekerheid dezelfde handeling uitvoeren.

Toeval is iets anders. Dat is (en moet) iedere keer iets anders zijn. Wil je weten [hoe Lava Lampen het internet hebben gered](https://www.wired.com/story/cloudflare-lava-lamps-protect-from-hackers/)? Wired heeft er een mooi artikel over geschreven. Lava Lampen smelten een type was dat dan begint te drijven door de warmte. Als de was afkoelt zakt het weer terug naar beneden en wordt weer opgewarmd. De was is hydrofobe en zal in bolletjes bewegen in het water. Tussen het helemaal koud en helemaal warm bewegen deze bolletjes. Een computer kan niet voorspellen hoe groot de bolletjes worden en kan ook de ‘route’ niet vooraf voorspellen. Op basis daarvan werkt de toevalsgenerator van o.a. [CloudFlare](http://www.cloudflare.com). CloudFlare doet veel voor het internet en beschermd ook dit blog tegen aanvallers. Ik schreef er ook al eens eerder over; [This blog is now protected](https://microbit.studio/this-blog-is-now-protected-with-cloudflare-soon-in-dutch/)

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

We gaan een Truth or Dare machine maken. Er zijn twee keuzes, ‘De waarheid’ of ‘een uitdaging’.

### Programmacode met PXT

Het bekende ‘on shake’ blokje gaan we gebruiken. Zodra er een schudding waargenomen wordt zal het programma starten. We kiezen een random getal tussen de 0 en 1. Met een waarde 0 vertel je een *waarheid*. Met ‘alle andere waarden dus ook 1’ vertel je een *dare*.

<figure class="wp-block-image alignnone size-large wp-image-364 size-medium is-style-default">![](/assets/images/wp-content/uploads/2021/01/Screenshot-2021-01-21-at-14.07.45-413x339.png)<figcaption>On Shake</figcaption></figure>Je ziet een if else blok staan. Hiermee heb je twee keuzes. Als waarde is 0 dan wordt het eerste segement uitgevoegd. Bij alle andere waarden het tweede segment.

Onderstaande Javascript code is hetzelfde als hierboven. Zie je op regel 1 dat er staat **‘let Random = o’**? Hiermee wordt een **variable** gemaakt. De naam variable zegt al wat het doet… zonder het uit te leggen. **Het is een woord dat een waarde kan bevatten**. In dit voorbeeld wordt Random de waarde 0 gegeven. Erna zie je dat Random = randint(0, 1). De variable krijgt daarmee een waarde die random is, een int (dus een getal is) en een waarde tussen de 0,1 heeft. Heel veel complexe concepten in een keer uitgelegd en **allemaal in een (rood) blokje** in de blokken editor.

```
<pre class="wp-block-preformatted theme:1c-kod lang:js decode:true">let Random = 0
input.onButtonPressed(Button.A, function () {
    basic.showString("Ready?")
})
input.onGesture(Gesture.Shake, function () {
    Random = randint(0, 1)
    if (Random == 0) {
        basic.showString("Truth!")
    } else {
        basic.showString("Dare!")
    }
})
basic.forever(function () {
    basic.showString("Ready?")
})

```