## Εισαγωγή τιμών από το χρήστη

Εντάξει, αυτό γίνεται πολύ εντυπωσιακό, αλλά είναι λίγο βαρετό να πρέπει να επεξεργάζεσαι τον κώδικά σου κάθε φορά που θέλεις να σχεδιάσεις ένα διαφορετικό μοτίβο. Δεν θα ήταν ωραίο να σου ζητάει το πρόγραμμα ποιες τιμές να χρησιμοποιήσει; Μπορείς να τα καταφέρεις!

\--- task \---

Αρχικά, πήγαινε στις **Μεταβλητές** και δημιουργήστε δύο μεταβλητές που ονομάζονται `μοίρες`{:class="block3variables"} και `αύξηση`{:class="block3variables"}.

\--- /task \---

\--- task \---

Τώρα πρόσθεσε τις νέες μεταβλητές στον κώδικά σου ως εξής:

```blocks3
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees ::variables) degrees
        change [steps v] by (increase ::variables)
    end
```

\--- /task \---

Τώρα πρέπει να ζητήσεις τιμές για αυτές τις δύο μεταβλητές και να τις αποθηκεύσεις. Αυτό το κάνεις χρησιμοποιώντας από τους **Αισθητήρες** το μπλοκ που ονομάζεται `Ρώτησε και περίμενε`{:class="block3sensing"}, στο οποίο μπορείς να πληκτρολογήσεις μια ερώτηση.

\--- task \---

Σύρε το μπλοκ `Ρώτησε και περίμενε`{:class="block3sensing"} στην περιοχή του αντικειμένου σου και άλλαξε την ερώτηση σε `Κατά πόσα βήματα πρέπει να μεγαλώνω;`{:class="block3sensing"}

Στη συνέχεια, πρόσθεσε το στο πρόγραμμά σου, αμέσως μόλις ορίσεις τα `βήματα`{:class="block3variables"} σε `0`, ως εξής:

```blocks3
    when green flag clicked
    set [steps v] to [0]
+    ask [How many steps should I grow by?] and wait
    pen up
```

\--- /task \---

Τώρα που έχεις κάνει το πρόγραμμά σου να ρωτάει κάτι, πρέπει να θυμάται την απάντηση! Ευτυχώς, το Scratch έχει μια ειδική μεταβλητή που ονομάζεται `απάντηση`{:class="block3sensing"}, όπου αποθηκεύει την πιο πρόσφατη απάντηση που έλαβε. Μπορείς να βρεις αυτήν τη μεταβλητή ανάμεσα στις εντολές των **Αισθητήρων**.

\--- task \---

Χρησιμοποιώντας ένα μπλοκ `όρισε σε`{:class="block3variables"} από τις **Μεταβλητές**, πάρε την τιμή της `απάντησης`{:class="block3sensing"} και αποθήκευσέ τη στη μεταβλητή `αύξηση`{:class="block3variables"} όπως:

```blocks3
    ask [How many steps should I grow by?] and wait
+    set [increase v] to (answer)
```

\--- /task \---

\--- task \---

Τώρα, κάνε το ίδιο με τις `μοίρες`{:class="block3variables"}, ρωτώντας `Πόσες μοίρες πρέπει να στρίψω;`{:class="block3sensing"} και αποθήκευσε την τιμή της `απάντησης`{:class="block3sensing"} στις `μοίρες`{:class="block3variables"}:

```blocks3
    set [increase v] to (answer)
+    ask [How many degrees should I turn?] and wait
+    set [degrees v] to (answer)
```

\--- /task \---

\--- task \---

Έλεγξε ότι το πρόγραμμά σου μοιάζει τώρα με το παρακάτω και εκτέλεσέ το μερικές φορές με διαφορετικούς αριθμούς. Κατάγραψε τις απαντήσεις που δημιουργούν τα πιο εντυπωσιακά σχέδια. Θα τα χρειαστείς αργότερα!

```blocks3
    when green flag clicked
    set [steps v] to [0]
    ask [How many steps should I grow by?] and wait
    set [increase v] to (answer)
    ask [How many degrees should I turn?] and wait
    set [degrees v] to (answer)
    pen up
    hide
    clear
    go to x: (0) y: (0)
    set pen color to [#4a6cd4]
    pen down
    repeat until <touching [edge v] ?> 
        move (steps) steps
        turn cw (degrees) degrees
        change [steps v] by (increase)
    end
```

\--- /task \---