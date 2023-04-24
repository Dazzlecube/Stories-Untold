---
title: The best racing board game is a puzzle game
date: 2023-02-25
description: "Many games are actually racing games in disguise, and often fail in the same ways."
tags:
   - designpatterns
---

Kids love racing games. *Mille Bornes* is a classic game for a reason.
Adults play them as well, if in slightly more complex forms. *Heat: Pedal to the Medal* is a modern example.
 
At their core, racing games boils down to this: Be the fastest to reach a certain stage or accumulate a resource, while preventing the other players to outpace you.
 
All of that sounds great in theory. In practice, however, most racing games fall into one of two traps.

 The problem lies in how you block your opponent's progress. 
In *Mille Bornes* for example you give them an 'accident' card that completely stops them, unless you have the right counter.
The problem with this approach is that you might end up doing nothing for multiple (sometimes 10+) turns before your get lucky and get the right card to start again.
Games in which a player is stuck until luck strikes are frustrating and will not captivate any player for long.
 
The alternative then is to be able to interfere with your opponent, but only lightly or indirectly so that you cannot really block it significantly.
Most implementation of these type of design philosophy end up with games where each player play pretty much independently.
While all players look at the same board, their decisions are the vast majority of the time independent of what the other players are doing.
This is what happens in games such as *New Frontiers: Race for the Galaxy*, for example [^1].
 
> Many games are actually racing games in disguise, and often fail in the same ways
 
How to solve this then?
You need to have meaningful interactions between players, preventing them to progress, while always giving them meaningful actions to play at their turn.
 
The other issue that often occurs is that, if a player fall behind for some reason (maybe she lost 5 turns trying to pick the right card), they are pretty much done, with very low chance to come back ahead.
Again, we end up with disengaged players when that happens.
 
In my opinion, the perfect balance was achieved by a game that is categorized as a puzzle game: *Labyrinth*.
In *Labyrinth*, each player need to collect a series of objects across a moving board.
At each turn, the player displaces one area of the labyrinth to create new - and importantly - block passages.

Another great design choice is to have a 2D map.
This creates engaging and meaningful decisions at each turn where you can progress while blocking your opponents, but they are never stuck or left so far behind that they cannot come back 'in the race'.
And as a result, both kids and adults will enjoy be able to it.
 
 
[^1]: While marketed as an empire building type of game, *New Frontiers* is actually racing game at its core (hint: Read its full title again). 

