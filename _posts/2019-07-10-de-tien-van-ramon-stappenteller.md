---

title: 'De tien van Ramon: <br> Stappenteller!'
date: '2019-07-10T09:34:10+00:00'
last_modified_at: '2022-12-30T00:00:00+00:00'
categories:
    - 'De tien van Ramon'
    - Experimenten
---

# Hoe werkt een stappenteller?

<span style="color: #808080;">*Ook wel een podometer genoemd*</span>

![](/assets/images/wp-content/uploads/2017/07/accelerometer_xyz.png)Een stappenteller werkt op basis van een accelerometersensor. Deze sensor (formaat halve rijstkorrel) kan twee dingen meten. Behalve de richting kan ook de snelheid in die richting bepaald worden. Voor dit experiment maken we alleen gebruik van [shake](https://www.microbit.co.uk/functions/on-shake). In Micro Python heet het [gesture](http://microbit-micropython.readthedocs.io/en/latest/tutorials/gestures.html). In een vervolgbericht ga ik dieper in op Gestures. Behalve shake kan Micro Python ook de kracht meten van een beweging veel meer meten; `<span class="pre">up</span>`, `<span class="pre">down</span>`, `<span class="pre">left</span>`, `<span class="pre">right</span>`, `<span class="pre">face</span> <span class="pre">up</span>`, `<span class="pre">face</span> <span class="pre">down</span>`, `<span class="pre">freefall</span>`, `<span class="pre">3g</span>`, `<span class="pre">6g</span>`, `<span class="pre">8g</span>`, `<span class="pre">shake</span>`. Een behoorlijke lijst voor zo’n kleine sensor. Daarom later meer. Nu gaan we eerst een eenvoudige stappenteller maken!

## Hoe werkt de programmacode?

In dit experiment gebruik van een functie. Binnen in deze functie wordt het getal step opgeteld met deze formule: step=step+1. Met andere woorden; tellen is het vorige getal met één erbij. Dit is een formule die je voor veel meer kunt gebruiken dan alleen voor een stappenteller.

### **Programmacode**

Met deze programmacode kun je direct aan de slag! Je kunt deze rechtstreeks overnemen. Aan het einde van de functioneren main () zie je wat er gebeurd als je op A drukt. het laat het nummer zien dat in steps zit; voor 1,5 seconde. Daarna gaat de functie weer verder met tellen.

<div class="wp-caption alignnone" id="attachment_526" style="width: 310px">![Programmacode stappenteller](https:///assets/images//wp-content/uploads/2017/07/Step_Counter___Make_and_code_activities__projects_and_apps_to_learn_about_technology___Technology_Will_Save_Us.png)Programmacode stappenteller

</div>## Uitdagingen

Kun je een stappenteller maken die bij iedere stap laat zien hoeveel stappen je hebt gezet? Kun je een doel stellen en bij het behalen van het doel een signaaltje geven ‘doel bereikt’? Zou je het doel ook met een variabele kunnen invoeren via button B? Hoe zou je de goals vaststellen? Wat is een gezonde levensstijl en hoe kun je met beweging deze verbeteren? Kun je behuizing ontwerpen om de Microbit aan je kleding vast te maken? Wat zou de beste plek zijn, aan je been, arm of borst? Kun je dat meten?