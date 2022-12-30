---
id: 644
title: 'MU &#8211; Python &#8211; Accelerometer'
date: '2020-04-01T19:02:09+00:00'
last_modified_at: '2022-12-30T00:00:00+00:00'
categories:
    - Experimenten
    - μPython
---

Vandaag ben ik begonnen met een dagelijkse challenge. Iedere dag iets nieuws voor Microbit schrijven. Of een bestaand project herontdekken en hergebruiken. Om makkelijk te beginnen heb ik gekozen om een nieuwe editor te gebruiken. De MU editor; met een handig voorbeeldscript om Accelerometer te gebruiken. En dat alles offline 🙂

Met dit script kun je de XYZ-sensor (ook wel accelerometer) uitlezen en op een grafiek laten zien. De code hiervoor staat onderaan de pagina. Met de knop ‘Plotter’ kun je live zien hoe de x-as van de Microbit bekeken wordt en hoe deze door de Microbit te draaien kunt beïnvloeden.

Op een Mac met OS Catalina is het nog wel even prutsen om het direct aan de praat te krijgen. Een snelle work-around is de code eerst op te slaan als HEX en daarna met de hand naar de Microbit te slepen. Met [deze uitleg op GitHub ](https://github.com/mu-editor/mu/issues/998) kan het ook rechtstreeks uit de MU Editor.

Via [Codewith.MU](https://codewith.mu/en/tutorials/1.0/microbit). (CC BY-NC-SA 4.0)

```
<pre class="wp-block-verse">from microbit import *
flag = True
while True:
sleep (20)
if button_a.was_pressed():
flag = not flag
if flag:
print ((accelerometer.get_x(),))
else:
print (accelerometer.get_values())
```

<figure class="wp-block-image size-large">![](/assets/images/wp-content/uploads/2020/04/microbit_plotter.gif)</figure>