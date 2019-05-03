## Gavere lijnen

Hoog tijd om kleur toe te voegen! Nu is je lijn één kleur, maar de **Pen** heeft blokken die de kleur kunnen veranderen. En met het juiste **Functie** blok kun je de kleur zelfs willekeurig veranderen!

Het blok voor het veranderen van de **Pen** kleur is `verander pen kleur met`{:class="block3extensions"}:

```blocks3
    verander penkleur met (10)
```

--- task --- Sleep een van deze blokken naar je `herhaal tot`{:class="block3control"} lus, zoals dit:

```blocks3
    herhaal tot <raak ik [edge v] ?>
+ verander penkleur met (10)
neem (stappen) stappen
draai (graden :: variables) graden naar rechts
verander [stappen v] met (toename ::variables)
end
```

--- /task ---

Gaaf, maar een beetje voorspelbaar. Je kunt het leuker maken door er een willekeurig getal in te zetten, zodat de kleur willekeurig verandert.

--- task --- Zet het willekeurig getal **Functie** blok in het `verander pen kleur met`{:class="block3extensions"} blok en zet er een paar getallen in. Begin eens met `1` en `100`.

```blocks3
    herhaal tot <raak ik [edge v] ?>
+ verander penkleur met (willekeurig getal tussen (1) en (100))
neem (stappen) stappen
draai (graden :: variables) graden naar rechts
verander [stappen v] met (toename ::variables)
end
```

--- /task ---

--- task --- Voer je programma weer uit en bekijk de willekeurige regenboog! --- /task ---