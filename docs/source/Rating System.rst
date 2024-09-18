Rating System 
==============

Crichub uses `Elo Rating System <https://en.m.wikipedia.org/wiki/Elo_rating_system>`_ Which is more famously used in chess.

>>> The Elo rating system is a method for calculating the relative skill levels of players in competitive games. Players gain points for wins and lose points for losses, with the amount depending on the difference in ratings between opponents. If a lower-rated player wins, they gain more points; if a higher-rated player wins, they gain fewer points.

How This Works
--------------

First of all we need an expected score for each delivery, let's take an example of Bowler against an All-Rounder:

:math:  `\[E_A = \frac{1}{1 + 10^{(R_B - R_A)/400}}\]`