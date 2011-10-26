---
layout: post
title: WarioWare DIY action instructions
---

I couldn't find a comprehensive list of all of the actions that are available in warioware diy for programming your games, so I thought I would write one up for people that are interested in focused game scripting. Nintendo did some really clever things here that both make the types of games that you can do really small, and make those types of games really easy to make. The mechanics that you can have in your game are pretty straight forward, and it allows you to make ghosts of familiar genres, but not the genres themselves.

Trigger Conditions
---------
tap
	this object
	anywhere on stage
contact
	touch
		object
		area
	overlap
		object
		area
art
	specific art (when a specific art for this object is being displayed)
	art finishes (when the art animation reaches the end of a loop)
time
	exactly (triggered when a particular time is reached)
	randomly (triggered when a random time within a selected range is reached)
		this one gives you the timeline with range controls. this is also the way to make random things happen at the beginning of the game.
switch
	gives you an object selector.
		switch turns  on
		switch is on
		switch turns off
		switch is off
win/loss
	win
	has been won
	not yet won
	loss
	has been lost
	not yet lost

All conditions when combined are && operations. To do things sometimes, on the first frame set a condition that says "when time == 1-1 and time randomly == 1-1 .. 1-8". The range of the second clause gives you the possibility of that happening. This can be used for shuffling objects on the stage.

Actions
-------

*Travel*

- Go Straight
	- Takes two Parameters:

        * starting at

		-	current location
		- 	another location
			point
			another object - gives you an offset from the other object editor
		direction
			specific
			random
	jump to
		location
			point
			area - random location within
		another object (jumps near another object then stays attached to that object)
			select object, select offset
	roam
		param 1 roam type
			wiggle - drunk walk
			reflect - pong
			insect - drunk walk, but with a larger step... or maybe just changing direction slightly 
			bounce - has acceleration due to gravity, doesn't but no energy loss from bounce
		param 2
			anywhere
			try not to overlap - not really sure how this works, perhaps it bounces off of other objects
	stop
		stops the current travel
	swap
		trades location with another object
	target - moves towards another object
		param 1
			offset from other object
		param 2
			speed2
Lose
	ends the game with a loss
Sound Effect
	plays one of 64 sound effects
Switch
	turns the switch either on or off
Art
	Change
		animation style
			hold
			play once
			loop
	Stop playing
Stage Effect
	flash
	shake
	confetti
	freeze