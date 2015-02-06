===================
Bukkit placeholders
===================

.. contents:: **Table of Contents**
   :depth: 2
   :local:

------------------
<player value="?">
------------------

.. warning::
	You can only use these placeholders in DYNAMIC animations.
	
name
===========
	Name (IGN) of player.
	
	.. code-block:: html

		<player value="name">

---------

displayname
===========
	Displayname (set by permission plugin or essentials) of player.
	
	.. code-block:: html

		<player value="displayname">

---------

listname
===========
	Name of player shown in tab.
	
	.. code-block:: html

		<player value="listname">

---------

world
===========
	World in which player currently is or is about to respawn in.
	
	.. code-block:: html

		<player value="world">

---------


x
===========
	X axi of location player has logged off from.
	
	.. code-block:: html

		<player value="x">

---------


y
===========
	Y axi of location player has logged off from.
	
	.. code-block:: html

		<player value="y">

---------

z
===========
	Z axi of location player has logged off from.
	
	.. code-block:: html

		<player value="z">

---------


yaw
===========
	yaw of location player has logged off from.
	
	.. code-block:: html

		<player value="yaw">

---------

pitch
===========
	pitch of location player has logged off from.
	
	.. code-block:: html

		<player value="pitch">

---------

firstplayed
===========
	Date when place has logged on to the server for the first time, uses :doc:`../../configuration/configurations/main_config` formatting for style formatting.
	
	.. code-block:: html

		<player value="firstplayed">

---------

lastplayed
===========
	Date when place has logged on to the server lately, uses :doc:`../../configuration/configurations/main_config` for style formatting.
	
	.. code-block:: html

		<player value="lastplayed">

---------

health
===========
	Current health of player's character.
	
	.. code-block:: html

		<player value="health">

---------

hunger
===========
	Current hunger of player's character.
	
	.. code-block:: html

		<player value="hunger">

---------

totalxp
===========
	Total experience amount of player's character.
	
	.. code-block:: html

		<player value="totalxp">

---------

levelxp
===========
	Current level experience of player's character.
	
	.. code-block:: html

		<player value="levelxp">

---------

ip
===========
	IP address of current connection.
	
	.. code-block:: html

	    <player value="ip">

---------

gamemode
===========
	Current gamemode of player's character.
	
	.. code-block:: html

	    <player value="gamemode">

--------		

------------------
<stats value="?">
------------------

.. warning::
	You can only use these placeholders in DYNAMIC animations.
	
If you are interested in using these placeholders take a look at `Statistic <http://jd.bukkit.org/dev/apidocs/org/bukkit/Statistic.html>`_ and simply lowercase them.

Example
=======

	.. code-block:: html
		
		<stats value="leave_game">
			
	Gives you number of rage quits.