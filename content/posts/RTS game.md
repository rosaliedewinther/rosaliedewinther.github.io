---
title: "Real time strategy game @HU"
date: 2019-02-01
draft: false
featured_image: '/images/Real_time_strategy_game_town.png'
---

During the 2nd year of my bachelor, me and five others made a real time strategy (RTS) game. The assignment was to make a game (without the use of a full game engine), and as we all enjoyed Age of Empires, we decided to make an RTS. We thought this would be an interesting challenge as it required an enemy who would autonomously control their units. Furthermore, it required additional path finding AI for all units. Some gameplay can be seen below. Resources are being collected, units being trained, buildings being built and enemies being defeated, with some speedups in between.

{{< youtube UaVAjuyEBRU >}}

The game was written in C++ and used [SFML](https://www.sfml-dev.org/) for the rendering. Unfortunately, we had no artists in the team, so we used freely available sprite sheets. The biggest issue with our implementation was performance (as it often is in games). Notably, the performance of A* and rendering was not great. However, these issues were later fixed by using culling and general optimizations. In the end, we got a very smooth game with quite a lot of bugs, but at least it is fun to play (in my opinion).