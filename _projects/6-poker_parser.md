---
layout: post
title:  "Poker Parser"
tags: poker stats visualisation
sidebar: true
text: true
description: Plot poker winnings and various statistics, persistent across multiple sessions. 
image: /assets/images/projects/poker_parser/lifetime_bankroll.png
---
<a href="https://github.com/ScottVinay/Poker-Parser">View source on Github</a>


Every Thursday, I play a game of cash buy-in No-Limit Texas Hold-Em poker with some friends from university. To get better at poker, like in anything in life, it is necessary to understand what you are doing right and wrong, and so understand how to improve.

This project is a series of functions for analysing and plotting the data from those games (downloaded as a CSV from PokerNow). Here, I can plot cash reserves over the course of a game, show the kinds of hands that people won and lost on, the part of the round on which people usually win, and more. The script also plots these over a whole history of a play group. By matching names across different game, we can see total wins and losses over a year or more.

<figure>
<img src="/assets/images/projects/poker_parser/lifetime_bankroll.png" />
<figcaption>Total bankroll over time. The flatline is not an error, one member just quit the group.</figcaption>
</figure>

<figure>
<img src="/assets/images/projects/poker_parser/winnings.png" />
<figcaption>Wins and losses over a game. We can see who won from whom. Lifetime stats are shown.</figcaption>
</figure>

<figure>
<img src="/assets/images/projects/poker_parser/showdown_nofold.png" />
<figcaption>The hands that people won on (not including folding). Lifetime stats are shown.</figcaption>
</figure>