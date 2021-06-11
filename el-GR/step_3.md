## Τυχαία μπαλόνια

--- task ---

Με τον κώδικα που έχεις τώρα, το μπαλόνι σου θα ξεκινά πάντα στο ίδιο μέρος και θα κινείται στην ίδια διαδρομή.

Κάνε κλικ στη σημαία μερικές φορές για να ξεκινήσεις το πρόγραμμά σου και θα δεις ότι είναι το ίδιο κάθε φορά.

--- /task ---

--- task ---

Αντί να χρησιμοποιείς την ίδια θέση x και y κάθε φορά, μπορείς αντίθετα να αφήσεις το Scratch `να επιλέξει έναν τυχαίο αριθμό`{:class="blockoperators"}. Άλλαξε τον κώδικα του μπαλονιού σου, έτσι ώστε να μοιάζει με αυτό:

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    forever
        move (1) steps
        if on edge, bounce
    end
```

Εάν κάνεις κλικ στην πράσινη σημαία μερικές φορές, θα παρατηρήσεις ότι το μπαλόνι σου ξεκινά από διαφορετικό μέρος κάθε φορά.

--- /task ---

--- task ---

Θα μπορούσες ακόμη και να χρησιμοποιήσεις έναν τυχαίο αριθμό για να επιλέξεις ένα τυχαίο χρώμα μπαλονιού κάθε φορά:

![κόκκινο αντικείμενο μπαλόνι](images/balloons-colour.png)

--- hints ---

--- hint ---

`Άλλαξε το εφέ χρώματος κατά `{:class="block3looks"}κατά έναν `τυχαίο αριθμό`{:class="block3operators"} όταν γίνει κλικ στην `πράσινη σημαία`{:class="block3events"}.

--- /hint ---

--- hint ---

Θα πρέπει να προσθέσεις αυτά τα μπλοκ στον κώδικά σου.

```blocks3
(pick random (0) to (200)

change [colour v] effect by (25)
```

--- /hint ---

--- hint ---

Your code should look like this:

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
    when flag clicked
    go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
    point in direction (45 v)
    change [colour v] effect by (pick random (0) to (200))
    forever
        move (1) steps
        if on edge, bounce
    end
```

--- /hint ---


--- /hints ---

--- /task ---

Τι θα συμβεί εάν αυτός ο κώδικας τοποθετηθεί στην αρχή του προγράμματός σου; Συμβαίνει κάτι διαφορετικό αν βάλεις αυτόν τον κώδικα _μέσα_ στο βρόχο `για πάντα`{:class="block3control"}; Ποιο προτιμάς;
