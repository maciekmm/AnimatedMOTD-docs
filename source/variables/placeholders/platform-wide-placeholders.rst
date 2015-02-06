.. _platform-wide-placeholders:

==========================
Platform wide placeholders
==========================

------------------
<server value="?">
------------------

justonemore
===========
	Adds 1 to player count.
	
	.. code-block:: html
	
		<server value="justonemore" arg="world/server">
		
	.. glossary::
		arg *(Optional)*
			World (Spigot) or server (BungeeCord) to take slots from.
			If not set, sums players online from worlds/servers.

---------
			
onlineplayers
=============
	Player count globally or on specific world/server.
	
	.. code-block:: html
	
		<server value="onlineplayers" arg="world/server">
		
	.. glossary::
		arg *(Optional)*
			World (Spigot) or server (BungeeCord) to take slots from.
			If not set, sums players online from worlds/servers.

---------		
	
maxplayers
==========
	Maximum player cap 
	
	.. code-block:: html
	
		<server value="maxplayers">

---------
		
ping
====
	Connection ping
	
	.. code-block:: html
	
		<server value="ping">