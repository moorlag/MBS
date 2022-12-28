---
id: 309
title: 'Experiment 9 Let&#8217;s play a game'
date: '2019-03-10T19:05:25+00:00'
author: ramon
layout: post
guid: 'http://microbit.studio/?p=309'
permalink: /experiment-9/
twitterCardType:
    - summary_large_image
cardImage:
    - 'http://microbit.studio/wp-content/uploads/2017/03/john-sting-112628.jpg'
image: /wp-content/uploads/2017/03/john-sting-112628-88x88.jpg
categories:
    - 'Aan de slag'
    - Experimenten
---

# Bluetooth Low energy en spelletjes spelen

*Het vorige experiment is even geleden. Ik moest mijn energie even goed verdelen tussen beter worden, verkouden en het plots wegvallen van René Franquinet. Ik probeer vanaf nu weer iedere dag een experiment uit te voeren. René deze is voor jou.*

<div class="wp-caption alignnone" id="attachment_313" style="width: 310px">![René Franquinet, Aad van der Drift en ik. Utrecht oktober 2016](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/Rene.jpeg?resize=300%2C225)René Franquinet, Aad van der Drift en ik. Utrecht oktober 2016

</div>We gaan een gamen maken. Aan de slag met Pong. Het[ kwam op 28 september 1972 op de Markt onder het merk Atari. ](https://en.wikipedia.org/wiki/Pong) Gameplay van Pong kun je in deze [YouTube video](https://www.youtube.com/watch?v=it0sf4CMDeM&t=60s) terugvinden.

<div class="wp-caption alignnone" id="attachment_310" style="width: 310px">![Pong Mod by halo4evergamer.tumblr.com](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/giphy-1.gif?resize=300%2C300)Pong Mod by halo4evergamer.tumblr.com

</div>Sinds ik door toeval twee Microbits heb gekregen wilde ik direct beginnen met dit experiment. Met behulp van een draadloos signaal worden beide Microbits met elkaar verbonden. Met wat hulp van een voorbeeld heb ik een werkend spelletje aan de praat gekregen. Pong.

Benodigdheden

- Twee Microbits
- Twee batterypacks
- Twee audiojacks met krokodillenklemmen (niet noodzakelijk).

Met de programmacode die je hieronder kunt vinden kun je direct aan de slag. Juist door de programmacode van Pong voor Microbit te delen met de MIT-licentie kun je deze vrij gebruiken. Ga vooral je gang en probeer eens een variable aan te passen. Kun je ontdekken welke variable de snelheid bepaald van een bal? Zou je een loop kunnen maken waarin het na een keer winnen moeilijker wordt (door de bal te versnellen na iedere beurt). Met het aansluiten van de audiojack via krokodillenklemmen kun je geluid horen. Je krijgt directe audiofeedback en een overwinnersgmuziekje. De verliezer krijgt natuurlijk een gepast geluid te horen.

Wil je iets hacken? Denk dan eens aan deze suggesties

- Laat het spel een ronde duren
- Laat na een ronde de snelheid oplopen
- Maak twee ballen
- Bestuur met de versnellingssensor

<div class="wp-caption alignnone" id="attachment_314" style="width: 310px">[![Aansluiten Audiojack. http://www.suppertime.co.uk/](https://i0.wp.com/microbit.studio/wp-content/uploads/2017/03/687474703a2f2f7777772e73757070657274696d652e636f2e756b2f626c6f676d7977696b692f77702d636f6e74656e742f75706c6f6164732f323031362f31322f4453434638353838332e6a7067.jpeg?resize=300%2C225)](http://www.suppertime.co.uk/)Aansluiten Audiojack. http://www.suppertime.co.uk/

</div>[Suppertime](https://github.com/blogmywiki/pongo)

**Update** Er zijn meer spelletjes te spelen met Bluetooth! [Micromonsters](https://gist.github.com/gingemonster/89f4eb986609ef477559d762765a4ebd)!