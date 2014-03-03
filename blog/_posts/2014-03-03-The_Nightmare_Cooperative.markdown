---
layout: post
title: The Nightmare Cooperative
---

A new game.

[Play The Nightmare Cooperative here](http://jonbro.itch.io/the-nightmare-cooperative).

I have been attempting to make a roguelike, and more specifically a [broughlike](http://mightyvision.blogspot.co.uk/2013/08/868-hack-ios.html) for the past year or so. You can play some of my earlier attempts [here](https://dl.dropboxusercontent.com/u/43672/asmallrogue/asmallrogue.html) and [here](https://dl.dropboxusercontent.com/u/43672/taxi/t_a_xi/t_a_xi.html), but I would not recommend it. They are largely directionless, I was attempting to cargo cult design my way into the correct space, without understanding what a roguelike is or what makes them interesting. There were two breakthroughs in my understanding.

Both of the breakthroughs came through making games in puzzlescript, and they both happened in the same week, on sequential days. The first was [All Together](http://www.puzzlescript.net/play.html?p=8524611). This helped me to understand what makes a grid and turn based game function. Largely, it is about positioning, and engines to manipulate that positioning in reaction to enviromental factors. This is tightly constrained in the early levels of all together, but by the last level, there are multiple solutions. In my initial idea for this game, it was a prototype for a roguelike. Having a prototype that ignores all but the most core mechanical elements of the roguelike allowed me to not get caught up in [the parts of the definition that concern replayability](http://www.roguebasin.com/index.php?title=Berlin_Interpretation).

All Together stopped at the point where it had only had 4 objects to work with (characters, enemies, goals and walls). With [Candy Bomb](http://jonbro.itch.io/candy-bomb) I started to allow new objects to bleed in as I came up with ideas for them. It only started to explore the cross section between these objects. The breakthrough here was in having minor modifications to object definitions that had large consequences. In prior games that I have made with a large number of objects, they tend to exist very far away from each other in their definitions. In Candy Bomb, changing the number of bombs required to explode a candy is a HUGE change to the way that puzzles are solved. The fact that minor changes make such a huge difference is freeing in that you can populate the space of the game with tons of variety without too much work. This is something I have shyed away from, because there seems to be an implicit rule that games with a bulk of rules are worse than games with only a few rules. I am no longer sure.

Moving from the puzzle games to the roguelike was not the hardest problem. I knew the core mechanic that I wanted to implement. The obvious and first step was to soften up the penalty for encountering enemies in the game. A less obvious jump was something that was pointed out by [smestorp](https://twitter.com/smestorp).

My original note:
_roguelikes need to have ways that you can spend your way past blocks in the level... even if it is always solvable, have alternate solutions that don't require as much thought, but you can spend a commdity (bombs or ropes in spelunky) to get past them._

I am going to fail to perfectly communicate his suggestion, but hopefully I will get close. He suggested that roguelikes need to have consumable items that allow later levels which might be impossible without the consumables to be beaten. On the early levels, you can always beat them without using consumables, but it is easier with them. This is where the ideas for the characters special moves came from. From there, having different specials for each character was an obvious jump.

I have plenty more ideas for how to expand this game, but I am trying to keep it within the [7DRL limits](7drl.org), so please enjoy.