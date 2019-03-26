## Alles willekeurig maken

Je kunt trouwens willekeurige getallen gebruiken om het hele programma steeds opnieuw uit te voeren, waarbij het patroon steeds verandert! Het lijkt een beetje op de screensavers uit de jaren '90...die jij waarschijnlijk niet kent, maar je ouders wel!

Je zult wat moeten aanpassen om dit mogelijk te maken. Als eerste moet je de `toename`{:class="block3variables"} en `graden`{:class="block3variables"} variabelen op willekeurig zetten in plaats van de speler erom te vragen. Dus je moet wat codeblokken aanpassen.

--- task --- Verwijder de vragen uit je code, en voeg willekeurige getallen toe.

```blocks3
    wanneer op groene vlag wordt geklikt
maak [stappen v] [0]
- vraag [Hoeveel stappen moet ik nemen?] en wacht
+ maak [toename v] (willekeurig getal tussen (1) en (10))
- vraag [Hoeveel graden moet ik draaien?] en wacht
+ maak [graden v] (willekeurig getal tussen (1) en (180))
pen op
```

--- /task ---

Als je nu je programma uitvoert zul je zien dat het een willekeurig patroon tekent, maar slechts één keer. Waardoor komt dat?

Dat komt omdat de lus tekent totdat het de rand van het Speelveld raakt.

--- task --- Je hebt nog een lus nodig die eeuwig blijft herhalen (dus een `herhaal`{:class="block3control"} blok!) náást de huidige lus om continu het programma uit te voeren. Pak er een uit het **Besturen** gedeelte en zet al je code daarin.

```blocks3
    wanneer op groene vlag wordt geklikt
+ herhaal
maak [stappen v] [0]
maak [toename v] (willekeurig getal tussen (1) en (10))
maak [graden v] (willekeurig getal tussen (1) en (180))
pen op
verdwijn
wis alles
ga naar x: (0) y: (0)
maak penkleur [#4a6cd4]
pen neer
herhaal tot <touching [edge v] ?>
neem (stappen) stappen
draai cw (graden) graden
verander [stappen v] met (toename)
end
end
```

---/task ---

Nu heb je echt iets gaafs om naar te kijken!

Maar je zult zien dat de computer soms iets heel lelijks tekent. Dit is omdat sommige getallen voor een aantal variabelen slechte keuzes zijn, en sommige **combinaties van die getallen** ook.

Op de volgende kaart kun je de computer helpen om alleen goede combinaties te maken!