Rating System 
==============

Crichub uses `Elo Rating System <https://en.m.wikipedia.org/wiki/Elo_rating_system>`_ Which is more famously used in chess.

  The Elo rating system is a method for calculating the relative skill levels of players in competitive games. 
  Players gain points for wins and lose points for losses, with the amount depending on the difference in ratings between opponents. 
  If a lower-rated player wins, they gain more points; if a higher-rated player wins, they gain fewer points.

How This Works
--------------

First of all we need an expected score which is calculated:

.. math::

   E_A = \frac{1}{1 + 10^{(R_B - R_A)/400}}

**Where**
  - :math:`R_A` is the new rating for Player A,
  - :math:`R_B` is the rating of Player B.

Then we just update the rating after a outcome. Outcome is 1 for win, 0.5 For Draw, 0 for a loss.

.. math::

   R_A' = R_A + K \times (S_A - E_A)
   
**Where**
  - :math: `R_A'` is the new rating for Player A,
  - :math: `K'` is a constant that controls how much the ratings change (This is very important in Crichub, we will later explore it)
  - :math: `S_A` is the actual result for Player A (1 for a win, 0 for a loss, 0.5 for a draw),
  - :math: `E_A` is the expected score for Player A.
  
  
Let's explore an example let's assume that Player A has the rating of 1500 and Player B has the rating of 3000.

So let's first calculate the expected score for Player A: 

.. math::

   E_A = \frac{1}{1 + 10^{(3000 - 1500)/400}} = 0.0001777963
   
Since Player A has less rating so it assumes that Player A has a very low chance of winning.

Now let's calculate the new rating for Player if he wins with K value of 30 

.. math::

   R_A' = 1500 + 30 \times (1 - 0.0001777963) = 1529.9818638749 
   
.. note:: This is the reason you see All-rounders getting a steep jump in comparison to proper bowler or batter

How This Works in Crichub
--------------------------

I take the same system but with modification since I have to update it ball by ball, I have different K for each of the outcome for both batter and bowler.

Let's explore K values First:

.. list-table:: K Values
   :widths: 40 30 30
   :header-rows: 1
   
   - * Outcome 
     * K Value for Batter
     * K Value for Bowler
     
   - * Wicket 
     * 1
     * 6
   - * 1,2,3
     * 2
     * 0.03
   - * Boundaries 
     * 3
     * 0.06
   - * Dots
     * 0.0001
     * 0.3
     