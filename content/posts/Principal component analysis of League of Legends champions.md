---
title: "Principal component analysis of League of Legends Champions"
date: 2021-10-10
draft: false
---


League of Legends is a popular 5 vs 5 game where matches last between 20 and 40 minutes (usually) and you can choose to play any out of 150+ champions, each differing in play style, strengths and weaknesses. Most players have a certain play style or champion which they prefer, while some just play whatever they feel like playing. Since I regularly play League with my friends and was stuck deciding which champion I should play next, I did a principal component analysis based on data scraped from a popular League statistics website named [lolalytics](https://lolalytics.com/). Below, you can see a visualization of the first two principal components. If you find your favorite champion, you can see which champions are similar and maybe give them a try as well. For me, as a fiddlesticks player, I should try Elise for example. (I know it's completely unreadable on this page, but the resolution is quite high, so you can zoom in)

![PCA](/images/PCA_LOL_result.png)

The following stats were considered in the PCA:

* Win rate by game duration timespans
* Game duration
* Play rate by top players (best at the champion)
* Win rate of top players
* Average rank of top players, whether they are top 1% or top 0.001%
* Play rate
* Dedication of one trick's, whether they only play the same champion
* Win rate
* Play rate per role
* Physical damage
* Magic damage
* True damage
* Total damage
* Damage taken
* Healing done
* Kills
* Deaths
* Assists
* Killing spree
* Gold collected
* Minions killed
* Jungle monsters killed
* Ban rate
* The win rate in a champion's best role