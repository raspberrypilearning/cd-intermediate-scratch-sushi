## Vragen om input

Ok, dit wordt best gaaf, maar het is wel een beetje saai om elke keer je code aan te passen als je een ander patroon wilt tekenen. Zou het niet handig zijn om het programma om input te laten vragen? Dat kun je!

--- task --- Ga eerst naar het **Variabelen** gedeelte en maak variabelen die `graden`{:class="block3variables"} en `toename`{:class="block3variables"} heten. --- /task ---

--- task --- Voeg nu de nieuwe variabelen als volgt aan je code toe:

```blocks3
    herhaal tot <raak ik [edge v] ?>
neem (stappen) stappen
draai (graden ::variables) graden naar rechts
verander [stappen v] met (toename :: variables)
end
```

--- /task ---

Nu moet je vragen naar waarden voor deze variabelen en ze opslaan. Hiervoor kun je een **Waarnemen** blok gebruiken dat `Vraag en wacht`{:class="block3sensing"} heet, en waarin je een vraag kunt stellen.

--- task --- Sleep het `Vraag en wacht`{:class="block3sensing"} blok naar je script en verander de vraag naar `Hoeveel stappen moet ik nemen?`{:class="block3sensing"}

Plaats het dan in de code, net na het `maak stappen 0`{:class="block3variables"} blok, zoals dit:

```blocks3
   wanneer groene vlag wordt aangeklikt
maak [stappen v] [0]
+ vraag [Hoeveel stappen moet ik nemen?] en wacht
pen op
```

--- /task ---

Nu je programma een vraag kan stellen, moet het ook het antwoord kunnen onthouden! Scratch heeft een speciale variable die `antwoord`{:class="block3sensing"} heet, waar het het laatste antwoord in opslaat. Deze variabele vind je bij de **Waarnemen** blokken.

--- task --- Gebruik een `maak`{:class="block3variables"} blok uit de **Variabelen**, en sleep het `antwoord`{:class="block3sensing"} blok in het `toename`{:class="block3variables"} blok, zoals dit:

```blocks3
    vraag [Hoeveel stappen  moet ik nemen?] en wacht
+ maak [toename v] (antwoord)
```

--- /task ---

--- task --- Doe nu hetzelfde met `graden`{:class="block3variables"}, vraag `Hoeveel graden moet ik draaien?`{:class="block3sensing"} en sla het `antwoord`{:class="block3sensing"} op in `graden`{:class="block3variables"}:

```blocks3
    maak [toename v] (antwoord)
+ vraag [Hoeveel graden moet ik draaien?] en wacht
+ maak [graden v] (antwoord)
```

--- /task ---

--- task --- Kijk of jouw programma er zo uit ziet als hieronder en voer het een paar keer uit met verschillende getallen. Schrijf die getallen op die de mooiste tekeningen maken. Je hebt ze straks nog nodig!

```blocks3
   wanneer groene vlag wordt aangeklikt
maak [stappen v] [0]
vraag [Hoeveel stappen moet ik nemen?] en wacht
maak [toename v] (antwoord)
vraag [Hoeveel graden moet ik draaien?] en wacht
maak [graden v] (antwoord)
pen op
verdwijn
wis alles
ga naar x: (0) y: (0)
maak penkleur [#4a6cd4]
pen neer
herhaal tot <raak ik [edge v] ?>
neem (stappen) stappen
draai (graden :: variables) graden naar rechts
verander [stappen v] met (toename :: variables)
end
```

--- /task ---