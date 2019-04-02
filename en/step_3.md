## Random balloons

--- task ---

With the code you have now, your balloon will always start in the same place and move in the same path. 

Click the flag a few times to start your program, and you'll see it's the same every time.

--- /task ---

--- task ---

Instead of using the same x and y position each time, you can let Scratch choose a random number instead. Change your balloon's code, so that it looks like this:

```blocks
	when flag clicked
	go to x:(pick random (-150) to (150)) y:(pick random (-150) to (150))
	point in direction (45 v)
	forever
		move (1) steps
		if on edge, bounce
	end
```

If you click the green flag a few times, you should notice that your balloon starts in a different place each time.

--- /task ---

--- task ---

You could even use a random number to choose a random balloon colour each time:

```blocks
	change [colour v] effect by (pick random (0) to (200))
```

![red balloon sprite](images/balloons-colour.png)

--- /task ---

What happens if this code is put at the start of your program? Does anything different happen if you put this code _inside_ the `forever`{:class="blockcontrol"} loop? Which do you prefer?

