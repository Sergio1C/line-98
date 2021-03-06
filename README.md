# Table of Contents
* [What is this](#what-is-this---)
* [How to use](#how-to-use-σ)
    * [Run as a browser game](#run-as-a-browser-game)
    * [Run as a desktop app](#run-as-a-desktop-app)
* [How to play](#how-to-play-)
    * [Scoring](#scoring)
* [Implementation](#implementation)
    * [Why Javascript?](#why-javascript)
    * [Algorithm](#algorithm)
    * [Programming pattern](#programming-pattern)
* [Future features](#future-features-which-may-never-got-implemented)
* [Reference](#reference)

# What is this? (・・ ) ?
This is a random repository on github in which contains a lot of random nonsense, broken English grammar, an dozen of kaomoji and among that maybe you can find a mini match-3 puzzle game implementation using plain javascript.

This repo make use of [p5.js](https://p5js.org/), which provide a minimum game loop and a rich set of API to work with HTML canvas.
![Game preview](/images/image.png)
# How to use σ(￣、￣〃)
### Run as a browser game
Simply clone this repo through git
```
git clone https://github.com/Kspade224/line-98.git
```
And open the file game.html using a browser
### Run as a desktop app
The game can also be run as a desktop app using [Electron](https://electron.atom.io/). Please change to the [electron branch](https://github.com/Kspade224/line-98/tree/electron) to learn more.
# How to play (￣～￣;)
### Scoring
The player select a ball in the play field and move it to a new location in an attempt to make a horizontally or vertically matching group of 3 or more balls with the same color.

The player gains point after said group was demolished from the screen 	←~(Ψ▼ｰ▼)∈

After each turn, a few new ball will appear to fill up the board, and the game is over if the board is full.

... well ... actually the gameover mechanic has not been implemented yet ⊂(￣▽￣)⊃
# Implementation
### Why Javascript?
The HTML canvas + Javascript combination is very suitable for making short, simple mechanic puzzle game, and is a very short way to see exactly what you just implemented.

Its also required very little preparation (the use of external libraries is entirely optional) compare to using a standard game engine.
### Algorithm
The backbone of this game is the A-star path-finding algorithm, which is an "extension" of the Dijkstra's algorithm.

In this implementation, we consider each grid on the play field is a node in a graph and every connection between 2 node has the weight of 1.

These are very good explainations of [Dijkstra's algorithm](https://www.youtube.com/watch?v=GazC3A4OQTE) and [A-star algorithm](https://www.youtube.com/watch?v=ySN5Wnu88nE) in case you are not familiar with them.
### Programming pattern
The game make use of the "State design pattern" to ensure its performance. You can learn more about it [here](http://gameprogrammingpatterns.com/state.html).
# Future features (which may never got implemented)
Better UI

Gameover mechanic

A separate config view
# Reference
[Computerphile](https://www.youtube.com/user/Computerphile) - My savior and daily entertainment source during college days ╰(▔∀▔)╯

[The Coding Train](https://www.youtube.com/user/shiffman) - Where I discover [p5.js](https://p5js.org/) and a ton of great mini-game implementations 
(ﾉ´ з `)ノ

[Game Programming Pattern](http://gameprogrammingpatterns.com/contents.html) - The first book that I read about game programming, and it is free w(°ｏ°)w