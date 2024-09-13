Beginners Guide 
===============
Setting Up Prefix
------------------
So the first thing after adding Crichub to your server you would like to do is check the prefix. Default prefix for Crichub is ``,`` and you can access it by mentioning it.

You can check the correct prefix by:

.. code-block:: console
  @CricHub#9872 prefix 

You can change the current prefix by:

.. code-block:: console
  @CricHub#9872 prefix .
  
Requirements
************

#. Manage Messages Permission.

.. _Creating your first game:

Debut 
------

This command is used to define your roleset in the game.
.. code-block:: console
  @CricHub#9872 debut
.. warning:: This can only be done once in your career so choose wisely.

Create
------

This command is used to create game.

.. code-block:: console
  @CricHub#9872 create
  
Aliases
*******

#. C

Join
----

This command is used to join a game.

.. code-block:: console
  @CricHub#9872 join

Aliases
*******

#. J

Shuffle 
-------

This command is used to shuffle the players list and is necessary to run before starting the game.

.. code-block:: console
  @CricHub#9872 shuffle

Aliases
*******

#. SF

Can only be run by:
*******************

#. Host 

Player_list
-----------

This command is used to view the Player List.

.. code-block:: console
  @CricHub#9872 player_list

Aliases
*******

#. PL

Change_host
-----------

This command is used to change the host.

.. code-block:: console
  @CricHub#9872 change_host @92.97

Aliases
*******

#. CH

Can only be run by:
*******************

#. Host 

Change_captain
-----------

This command is used to change captain of a team.

If used by Host:

.. code-block:: console
  @CricHub#9872 change_captain <new captain> <Team Number 1|2>

If used by captain:

.. code-block:: console
  @CricHub#9872 change_captain <new captain> 

Aliases
*******

#. CC

Can only be run by:
*******************

#. Host 
#. Captain 

Toss
----

This command is used to conduct toss.

.. code-block:: console
  @CricHub#9872 toss

Aliases
*******

#. T 

Can only be run by:
*******************

#. Host 

Set_overs
---------

This command is used to set the maximum overs for an inning.

.. code-block:: console
  @CricHub#9872 set_overs <Overs >1|<=20>

Aliases
*******

#. SO 

Can only be run by:
*******************

#. Host 

Start
-----

This command is used to initiate a game.

.. code-block:: console
  @CricHub#9872 start

Aliases
*******

#. S 

Can only be run by:
*******************

#. Host 

Yeet
-----

This command is used to delete a game.

.. code-block:: console
  @CricHub#9872 yeet

..NOTE::  This can only be used if both captains agree after the game has started.

Aliases
*******

#. S 

Can only be run by:
*******************

#. Host (Before the game commencement)
#. Captains (After the game commencement)