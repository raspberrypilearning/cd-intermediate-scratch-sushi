## Patronen tekenen

Nu heb je een programma dat een lijn tekent, maar het is slechts één lijn. Wat saai! Je kunt de `herhaal`{:class="block3control"} lus gebruiken om iets continu te tekenen, maar dan verdwijnt je tekening van het Speelveld!

Dus je hebt een andere lus nodig die `herhaal tot`{:class="block3control"} heet, die je in het **Besturen** gedeelte vindt. Deze lus doet continu iets, **totdat** voldaan is aan een True/False voorwaarde.

\--- task \--- Neem een `herhaal tot`{:class="block3control"} blok uit het **Besturen** gedeelte, en zet de `neem stappen`{:class="block3motion"} en `draai graden`{:class="block3motion"} blokken er als volgt in:

```blocks3
+ herhaal tot <>
neem (50) stappen
draai cw (15) graden
end
```

\--- /task \---

\--- task \--- Klik nu een paar keer op de groene vlag en kijk wat er gebeurt. Er vallen twee dingen op: de pen begint altijd met een rechte lijn naar het midden van het Speelveld, en het stopt niet bij de rand. \--- /task \---

## \--- collapse \---

## title: Waarom doet de pen dit?

De pen begint altijd met een lijn naar het midden, omdat het eerste **Beweging** blok dat na het `pen neer`{:class="block3extensions"} blok komt het `ga naar x: 0 y:0`{:class="block3motion"} is. Dus zal de pen een lijn tekenen als het naar het midden van het Speelveld gaat.

De pen stopt niet aan de rand van het Speelveld, omdat je nog niet gezegd hebt tegen de `herhaal tot`{:class="block3control"} lus welke voorwaarde het controleert. Dat betekent dat er nooit aan die voorwaarde voldaan kan worden, en dus blijft de lus doorgaan. Dat houdt in dat deze lus werkt als een `herhaal`{:class="block3control"} lus.

\--- /collapse \---

\--- task \--- Sleep het `ga naar x: 0 y: 0`{:class="block3motion"} blok vóór het `pen neer`.{:class="block3extensions"} blok en voeg, uit het **Pen** gedeelte, een `pen op`{:class="block3extensions"} blok toe aan het begin van je code. \--- /task \---

Tijd om je `herhaal tot`{:class="block3control"} lus aan te passen zodat het stopt wanneer jij dat wilt. Je wilt weten of de (onzichtbare) sprite de rand van het Speelveld raakt, dus heb je een **Waarnemen** blok nodig - in dit geval, het `raak ik`{:class="block3sensing"} blok.

\--- task \--- Voeg een `raak ik ?`{:class="block3sensing"} blok toe aan je `herhaal tot`{:class+"block3control"} lus, en selecteer `rand`{:class="block3sensing"}. Dan wordt de lus uitgevoerd **totdat** de (onzichtbare) sprite de rand van het Speelveld raakt.

```blocks3
    pen neer
+   herhaal tot <touching [edge v] ?>
neem (50) stappen
draai cw (15) graden
end
```

\--- /task \---

\--- task \--- Verander het aantal stappen in het `beweging`{:class="block3motion"} blok naar `5` en controleer of je programma er zo uit ziet:

```blocks3
    wanneer op groene vlag wordt geklikt
pen op
verdwijn
wis alles
ga naar x: (0) y: (0)
maak penkleur [#4a6cd4]
pen neer
herhaal tot <touching [edge v] ?>
neem (5) stappen
draai cw (15) graden
end
```

\--- /task \---

Als je nu je programma uitvoert, zul je zien dat de tekening die door de pen gemaakt wordt op het Speelveld blijft.

Dat niet alleen, je programma is verandert in een programma dat alleen maar cirkels tekent! Wat er gebeurt is dat de 15-graden draai oploopt tot 360 graden, dus je pen tekent een volledige cirkel. Je gaat de manier waarop het beweegt zo aanpassen dat het elke stap groter maakt zodat het een spiraal gaat tekenen. Hiervoor heb je een **variabele** nodig.

Variabelen zijn plekken met labels waarin je getallen of andere belangrijke informatie in opslaat. Je maakt ze in het **Variabelen** blok gedeelte.

\--- task \--- Maak een variabele genaamd `stappen`{:class="block3variables"} en voeg dan een `maak stappen 0`{:class="block3variables"} blok toe aan het begin van je programma.

```blocks3
    wanneer op groene vlag wordt geklikt
+ maak [stappen v] [0]
pen op
```

\--- /task \---

\--- task \--- Gebruik dan de waarde van `stappen`{:class="block3variables"} in plaats van de `5` in het `bewegen`{:class="block3motion"} blok, en voeg `verander stappen met 1`{:class="block3variables"] toe aan je lus:

```blocks3
    pen neer
herhaal tot <touching [edge v] ?>
+ neem (stappen) stappen
draai cw (76) graden
+ verander [stappen v] met (1)
end
```

\--- /task \---

Denk je dat het uitmaakt waar je het `verander stappen met 1`{:class="block3variables"} blok in je lus zet?

## \--- collapse \---

## title: Code in de juiste volgorde zetten

Als je gaat bepalen in welke volgorde je de blokken gaat zetten, bedenk dan wat elk blok doet en wat jij wilt dat je code doet.

In dit geval wil je dat de pen beweegt en dan draait, steeds opnieuw. Elke keer dat het dit doet, wil je dat het een extra stap neemt.

Dus het is logisch om het `verander stappen met 1`{:class="block3variables"} blok **na** het `beweging`{:class="block3motion"} blok te plaatsen. Maar ná het bewegen maakt het niet echt uit of de pen eerst draait en dan het aantal stappen verandert, of dat het eerst het aantal stappen verandert en daarna draait.

\--- /collapse \---

\--- task \--- Voer de code uit en verander ook eens het aantal graden dat de pen draait (probeer `76` en `120`)! \--- /task \---