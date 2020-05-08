## Προσθήκη βαθμολογίας

Ας κάνουμε τα πράγματα πιο ενδιαφέροντα κρατώντας βαθμολογία.

--- task ---

Για να κρατάς τη βαθμολογία του παίκτη, χρειάζεσαι ένα μέρος για να την αποθηκεύσεις. Δημιούργησε μία νέα `μεταβλητή`{:class="block3variables"} με το όνομα `βαθμολογία`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Όταν ξεκινά ένα νέο παιχνίδι (κάνοντας κλικ στη σημαία), θα πρέπει να ορίζεις τη βαθμολογία του παίκτη στο 0. Πρόσθεσε αυτόν τον κώδικα στο πάνω μέρος του κώδικα `όταν γίνει κλικ στην πράσινη σημαία`{:class="block3events"}:

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
when flag clicked
+ set [score v] to [0]
show
switch costume to (balloon1-a v)
```

--- /task ---

--- task ---

Κάθε φορά που σκάει ένα μπαλόνι, θα προσθέτεις 1 στη βαθμολογία:

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
+change [score v] by (1)
hide
```

--- /task ---

--- task ---

Εκτέλεσε ξανά το πρόγραμμά σου και κάνε κλικ στο μπαλόνι. Αλλάζει το σκορ σου;

--- /task ---

