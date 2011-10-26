---
layout: post
title: WarioWare DIY action instructions
comments: true
---

![wario](http://dl.dropbox.com/u/43672/blog_static/images/wario.jpg)

I couldn't find a comprehensive list of all of the actions that are available in warioware diy for programming your games, so I thought I would write one up for people that are interested in focused game scripting. Nintendo did some really clever things here that both make the types of games that you can do really small, and make those types of games really easy to make. The mechanics that you can have in your game are pretty straight forward, and it allows you to make ghosts of familiar genres, but not the genres themselves.

Trigger Conditions
---------
## Tap ##

Reacts to the stylus coming down. Can react to either:

* _This object_
* _Anywhere on stage_

## Contact ##

This is the collision detection. The main types are either _touch_ or _overlap_, but I am not sure what the difference is. Perhaps with overlap, the object in question needs to be fully enclosed or enclosing the other object. In either case you can define one following parameters.
* _Object_: The object to check for collision with.
* _Area_: The area to check for collision with.

## Art ##

Allows you to check conditions on the art for _this object_. Can be one of two conditions.

* _Specific art_: when a specific art for this object is being displayed.
* _Art finishes_: when any art animation reaches the end of a loop.

## Time ##

Can be one of two types.

* _Exactly_: Triggered when a particular time is reached.
* _Randomly_: triggered when a random time within a selected range is reached. This gives you the timeline with range controls. It is the way to make random things happen at the beginning of the game.

## Switch ##
Allows you to check the switch state on any object. The switch state can be one of four.

* Switch turns on.
* Switch is on
* Switch turns off
* Switch is off

## Win/Loss ##

You can check for game conditions.

* Win
* Has been won
* Not yet won
* Loss
* Has been lost
* Not yet lost

All conditions when combined are && operations. To do things sometimes, on the first frame set a condition that says "when time == 1-1 and time randomly == 1-1 .. 1-8". The range of the second clause gives you the possibility of that happening. This can be used for shuffling objects on the stage.

_Actions_
-------

## Travel ##

**Go Straight**

*  _Starting at_: 
   This can be the _current location_ or _another location_. In the case of another location, it can be a point on the stage or another object, with the offset from the other object.
*  _Direction_:
	This can be a _specific direction_ or a _random direction_. In the case of specific direction, it gives you an 8 point compass to set. In both cases, it allows you to set the speed of travel.

**Jump To**

Takes one of the following two types:

*  _Location_:
	Can be a _point_ on the stage, or a random location within an _area_.
* _Another Object_:
	Jumps near another object then stays attached to that object. This brings up the object selector, and then an offset editor.

**Roam**

Takes four parameters. The first parameter is one of the following movement types:

*  _Wiggle_: Appears to be a drunk walk that can change its direction wildly, and moves in short steps.
*  _Reflect_: Bounces off the area that you define for the movement in a pong style.
*  _Insect_: Drunk walk, just like wiggle but with a larger step and changes the movement direction less.
*  _Bounce_: Same as pong, but accelerates due to gravity. Seems to have enough energy at the end of the bounce to make it to the top of the area that you define.

The second parameter is one of the following:

*  _Anywhere_: Moves anywhere within the area you define.
*  _Try not to overlap_: Not really sure how this works, perhaps it bounces off of other objects.

The last parameters are an area on the stage that the object will roam within, and a speed of roaming.

**Stop**

Stops the current travel.

**Swap**

Trades location with another object.

**Target**

Moves towards another object. Takes three parameters:

* _Object_: The object to move towards.
* _Offset_: The offset from other object.
* _Speed_

## Lose ##

Ends the game with a loss

## Sound Effect ##

Plays one of 64 sound effects. These are arranged in 8 banks of 8.

## Switch ##

Turns the switch either on or off.

## Art ##

**Change**

Can change the _animation style_ to one of three styles. It also allows you to select the art for the object. There can be 1 - 4 arts per object.

* _Hold_: Stay on the current frame.
* _Play once_
* _Loop_

**Stop**

Stops the currently playing art.

## Stage Effect ##

These are effects that play over the whole stage.
* _Flash_
* _Shake_
* _Confetti_
* _Freeze_: Stops everything, including all further object actions.

I think this list is more or less complete. If you notice any errors or corrections that you would like to make, please tell me in the comments.

