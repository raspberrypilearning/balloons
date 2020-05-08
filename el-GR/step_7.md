## Πολλά μπαλόνια

Το σκάσιμο ενός μπαλονιού δεν είναι και κανένα σοβαρό παιχνίδι, οπότε ας προσθέσουμε πολλά περισσότερα!

Ένας απλός τρόπος για να πάρεις πολλά μπαλόνια είναι απλώς να κάνεις δεξί κλικ στο αντικείμενο του μπαλονιού και να κάνεις κλικ στο **διπλασιασμό**. Αυτό είναι εντάξει εάν θέλεις λίγα, αλλά τι γίνεται αν χρειάζεσαι 20; ή 100; Πρόκειται πραγματικά να κάνεις κλικ στο **διπλασιασμό** τόσες πολλές φορές;

Ένας πολύ καλύτερος τρόπος για να πάρεις πολλά μπαλόνια είναι να _κλωνοποιήσεις_ το αντικείμενο μπαλόνι.

--- task ---

Σύρε τον κώδικα του μπαλονιού σου στο `όταν γίνει κλικ στην πράσινη σημαία`{:class="block3events"} σε ένα νέο μπλοκ ελέγχου `όταν ξεκινήσω ως κλώνος`{:class= "block3control"}.

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
when flag clicked
set [score v] to [0]
-show
-switch costume to (balloon1-a v)
-point in direction (pick random (-90) to (180))
-go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
-change [color v] effect by (pick random (0) to (200))
-forever
-   move (1) steps
-   if on edge, bounce
-end

+when I start as a clone
show
switch costume to (balloon1-a v)
point in direction (pick random (-90) to (180))
go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
change [color v] effect by (pick random (0) to (200))
forever
    move (1) steps
    if on edge, bounce
end
```

--- /task ---

--- task ---

Πρόσθεσε κώδικα για να δημιουργήσεις 20 κλώνους μπαλονιού στο πάνω μέρος του κώδικα `όταν γίνει κλικ στην πράσινη σημαία`{:class="block3events"}.

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
when flag clicked
set [score v] to [0]
+hide
+repeat (20)
create clone of (myself v)
end
```

--- /task ---

--- task ---

Θα πρέπει επίσης να αντικαταστήσεις το μπλοκ `εξαφανίσου`{:class="block3looks"} στον κώδικα όπου γίνεται κλικ το μπαλόνι με το μπλοκ `διέγραψε αυτό τον κλώνο`{:class="block3control"}.

![αντικείμενο μπαλόνι](images/balloon-sprite.png)

```blocks3
when this sprite clicked
switch costume to (burst v)
start sound (pop v)
wait (0.3) seconds
change [score v] by (1)
-hide
+delete this clone
```

--- /task ---


--- task ---

Δοκίμασε το έργο σου! Τώρα, όταν γίνει κλικ στη σημαία, το κύριο αντικείμενο του μπαλονιού σου θα εξαφανιστεί και στη συνέχεια θα κλωνοποιηθεί 20 φορές. Όταν ξεκινά καθένας από αυτούς τους 20 κλώνους, θα αναπηδά τυχαία στην οθόνη, όπως και πριν. Δες αν μπορείς να σκάσεις τα 20 μπαλόνια!

--- /task ---

