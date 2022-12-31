---
title: 'De tien van Ramon: Stappenteller!'
date: '2019-03-14T21:49:04+00:00'
last_modified_at: '2022-12-31T00:00:00+00:00'

categories:
    - 'Aan de slag'
    - Experimenten
---

# Wat is een stappenteller?

Een stappenteller, of pedometer, telt het aantal stappen van degene die hem draagt. Het is een klein apparaatje, dat je aan je broek of riem bevestigt. Een stappenteller telt in eerste instantie alleen voetstappen, geen afstanden. Elke stap wordt geteld, zowel grote als kleine stappen. Pas als je je weet hoe lang je gemiddelde staplengte is, kun je uitrekenen met welke afstand een bepaald aantal voetstappen ongeveer overeenkomt.

## Waarom zou je stappen tellen?

Met een stappenteller of pedometer kun je niet alleen de afstand van een afgelegde wandeltocht schatten, bij dagelijks gebruik is het ook een graadmeter voor lichamelijke activiteit. In Japan is ‘10.000 stappen per dag’ al tientallen jaren een begrip. Om je een indruk te geven: bij de meeste mensen komt dit overeen met pakweg 7-8 km lopen – en dat dus elke dag! Grofweg gelden de  
volgende gradaties:

- tot 5000 stappen: zittende leefstijl,
- 5000-7500 stappen: licht actieve leefstijl,
- 7500-10.000 stappen: matig actieve leefstijl,
- vanaf 10.000 stappen: actieve gezonde leefstijl,
- vanaf 12.500 stappen: zeer actieve leefstijl.

Met een stappenteller zie je vrij snel of je te weinig beweegt. Deze confrontatie met objectieve cijfers stimuleert ook om meer te gaan bewegen.

**Opdracht** We gaan een stappenteller maken! In de Micro:bit zit een versnellingssensor. In code is de conditie “shake”.

### Programmacode met PXT

Er zijn drie blokken nodig om het programma iets te laten doen. Deze drie blokken zijn, ON START, FOREVER en ON SHAKE. Alle drie blokken hebben een eigen rol en worden dus **niet** met elkaar verbonden. Hieronder zie je de instellingen voor ieder blokje.

Met het blokje ON START wordt een beginwaarde van het programma vastgelegd. Deze beginwaarde noem je variabele. In een variabele kan een getal (een zonder een komma! of een woord staan. In dit geval wordt er een getal opgeslagen.

<div class="wp-caption alignnone" id="attachment_341" style="width: 222px">![De tien van Ramon - On start](/assets/images/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-1.png)De tien van Ramon – On start

</div>Door het blokje FOREVER kunnen we iets altijd laten zien. In dit blok staat een subblokje. Show number laat een getal zien.

<div class="wp-caption alignnone" id="attachment_342" style="width: 278px">![De tien van Ramon - Forever](/assets/images/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-2.png)De tien van Ramon – Forever

</div>Het laatste blokje is het veranderen van een variabele. ON SHAKE telt +1 op bij de waarde van de variabele. Hieronder zie je hoe een variabele vastgelegd wordt.

<div class="wp-caption alignnone" id="attachment_343" style="width: 259px">![De tien van Ramon - On shake](/assets/images/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-3.png)De tien van Ramon – On shake

</div>Hieronder zie je hoe een variabele vastgesteld wordt.

<div class="wp-caption alignnone" id="attachment_344" style="width: 310px">![De tien van Ramon - variabele](/assets/images/wp-content/uploads/2017/03/Untitled_-_pxt_microbit_org-4.png)De tien van Ramon – variabele

</div>## Extra opdracht

Probeer met behulp van een if/then een succeservaring voor de gebruiker te maken! Een smiley bij 10.000 stappen. En 1.000 stappen ‘Go go go’!

```
<pre class="theme:1c-kod lang:js decode:true" title="De tien van Ramon: Stappenteller">let stap = 0
basic.forever(() => {
    basic.showNumber(stap)
})
input.onGesture(Gesture.Shake, () => {
    stap += 1
})
stap = 0
```