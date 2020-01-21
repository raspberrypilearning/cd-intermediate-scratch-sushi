## Gavere lijnen

Hoog tijd om kleur toe te voegen! Nu is je lijn één kleur, maar de **Pen** heeft blokken die de kleur kunnen veranderen. En met het juiste **Functie** blok kun je de kleur zelfs willekeurig veranderen!

Het blok voor het veranderen van de **Pen** kleur is `verander pen kleur met`{:class="block3extensions"}:

```blocks3
    verander pen kleur met (10)
```

\--- task \---

Grab one of those blocks and put it into your `repeat until`{:class="block3control"} loop, like this:

```blocks3
    herhaal tot <raak ik [rand v] ?>
+ verander pen kleur met (10)
neem (stappen) stappen
draai cw (graden ::variables) graden
verander [stappen v] met (toename ::variables)
end
```

\--- /task \---

That’s cool, but a bit predictable. You can make it a bit more fun if you add a random number into it, so the colour changes randomly.

\--- task \---

Put the random number **Operator** block into the `change pen color by`{:class="block3extensions"} block and pick some values to go in it. I'd try `1` and `100` to start.

```blocks3
    herhaal tot <raak ik [rand v] ?>
+ verander pen kleur met (willekeurig getal tussen (1) en (100))
neem (stappen) stappen
draai cw (graden ::variables) graden
verander [stappen v] met (toename ::variables)
end
```

\--- /task \---

\--- task \---

Try running it again, and watch the random rainbow!

\--- /task \---