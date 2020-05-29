## Dodaj licznik czasu

Możesz uczynić swoją grę bardziej interesującą, dając graczowi 10 sekund na przebicie jak największej liczby balonów.

--- task ---

Możesz użyć innej zmiennej do przechowywania pozostałego czasu. Kliknij na scenie i utwórz nową zmienna nazwaną `czas`{:class="block3variables"}.

--- /task ---

Twój licznik czasu powinien działać następująco:

+ Licznik czasu powinien zaczynać od 10 sekund;
+ Licznik powinien zmniejszać się co sekundę;
+ Gra powinna się zatrzymać, gdy licznik czasu osiągnie 0.

--- task ---

Oto kod do zrobienia tego, który możesz dodać do swojej _sceny_:

![duszek balonu](images/stage-sprite.png)

```blocks3
when flag clicked
set [time v] to [10]
repeat until <(time) = [0]>
    wait (1) seconds
    change [time v] by (-1)
end
stop [all v]
```

--- /task ---

--- task ---

Przeciągnij swoją wyświetloną zmienną 'czas' na prawą stronę sceny. Możesz także kliknąć prawym przyciskiem myszy na wyświetlaną zmienną i wybrać "powiększony widok", aby zmienić sposób wyświetlania czasu.

![zrzut ekranu](images/balloons-readout.png)

--- /task ---

--- task ---

Przetestuj swoją grę. Ile punktów możesz zdobyć? Jeśli Twoja gra jest zbyt łatwa, możesz:

+ Dać graczowi mniej czasu;
+ Zwiększyć liczbę balonów;
+ Sprawić, aby balony poruszały się szybciej;
+ Sprawić aby balony były mniejsze.

Zagraj w grę kilka razy, aż będziesz zadowolony, że jest to odpowiedni poziom trudności.

--- /task ---

