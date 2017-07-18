## Adding a score

Let's make things more interesting by keeping score.



+ To keep the player's score, you need a place to put it. A _variable_ is a place to store data that can change, like a score.

	To create a new variable, click on the 'Scripts' tab, select `Data`{:class="blockdata"} and then click 'Make a Variable'.

	![screenshot](images/balloons-score.png)

	Type 'score' as the name of the variable, make sure that it is available for all sprites, and click 'OK' to create it. You'll then see lots of code blocks that can be used with your `score`{:class="blockdata"} variable.

	![screenshot](images/balloons-variable.png)

	You'll also see the score in the top-left of the stage.

	![screenshot](images/balloons-stage-score.png)

+ When a new game is started (by clicking the flag), you want to set the player's score to 0. Add this code to the top of the balloon's `when flag clicked`{:class="blockevents"} code:

	```blocks
	set [score v] to [0]
	```

+ Whenever a balloon is popped, you need to add 1 to the score:

	```blocks
		when this sprite clicked
		switch costume to [burst v]
		play sound [pop v]
		wait (0.3) secs
		change [score v] by (1)
		hide
	```

+ Run your program again and click the balloon. Does your score change?



