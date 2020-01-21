## Alles willekeurig maken

Je kunt trouwens willekeurige getallen gebruiken om het hele programma steeds opnieuw uit te voeren, waarbij het patroon steeds verandert! Het lijkt een beetje op de screensavers uit de jaren '90...die jij waarschijnlijk niet kent, maar je ouders wel!

Je zult wat moeten aanpassen om dit mogelijk te maken. Als eerste moet je de `toename`{:class="block3variables"} en `graden`{:class="block3variables"} variabelen op willekeurig zetten in plaats van de speler erom te vragen. Dus je moet wat codeblokken aanpassen.

\--- task \---

Remove the questions from your code, and update it to use random numbers instead.

```blocks3
    wanneer groene vlag wordt aangeklikt
maak [stappen v] [0]
- vraag [Hoeveel stappen moet ik nemen?] en wacht
+ maak [toename v] (willekeurig getal tussen (1) en (10))
- vraag [Hoeveel graden moet ik draaien?] en wacht
+ maak [graden v] (willekeurig getal tussen (1) en (180))
pen op
```

\--- /task \---

If you run your program now, you’ll find that it does draw a random pattern, but only once. Why do you think that is?

It’s because the loop only runs until it reaches the edge of the Stage.

\--- task \---

You need another loop that runs forever (so a `forever`{:class="block3control"} block then!) outside the current one to keep it going over and over. Just drag one out of the **Control** section, and add all your other code into it.

```blocks3
    wanneer groene vlag wordt aangeklikt
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
herhaal tot <raak ik [rand v] ?>
neem (stappen) stappen
draai cw (graden) graden
verander [stappen v] met (toename)
end
end
```

\--- /task \---

Now you’ve really got something awesome to look at!

However, you may notice that, every now and then, the computer draws something that looks pretty...bad. This is because some numbers for some of those variables are just bad choices, and some **combinations of those numbers** are also bad choices.

On the next card, you'll help the computer to pick only good combinations!