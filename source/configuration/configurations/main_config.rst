.. _main_config:

==========
config.yml
==========

config.yml represents basic configuration of plugin. Player caching, database management and fallback motd are here.

.. contents:: **Table of Contents**
   :depth: 2
   :local:
   
---------- 

--------
settings
--------
.. literalinclude:: __files/config.yml
   :language: yaml
   :lines: 9-33

----------
   
animations
==========
	.. warning::
		Do not remove default key
		You can assign STATIC variable to dynamic field, but never DYNAMIC to static.
		
	This section holds list of animations assigned to forced hosts.
	
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 11-16
		
caching
=======
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 17-20
		
	.. glossary::
		
		time
			Specify time after which cache files will be regenerated for certain players
		
		parts
			.. note::
				Removing parts will result in no caching, so your best bet if you are not using player parts is just to remove it.
			
			Key is used for file name and <player> variable in animation

fallback
========
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 21-28
	
	This section holds fallback motd that is being sent to clients under specific circumstances:
	
	- Animation passes duration threshold
	- Connection exceeds see `max-connection-per-ip`_
	- Connection address is specified in blacklist.yml
	
	.. glossary::
		motd
			It is basically a description, it contains two lines (they have to be separated with \n though)
		
		favicon
			.. warning::
				Don't put animated icon, it will not work.
				
			Favicon that will be displayed next to fallback motd.
		
		status-bar
			.. warning::
				Uncommenting status-bar will result in red cross in fallback motd.
				
			Status bar is a line displayed on player count slot.
		
		player-sample
			.. warning::
				Player sample will display *x and more..* if status-bar is disabled
				
			Holds list of strings displayed when client hovers over status-bar.

debug
=====
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 29-29
		
	This boolean will help you determinate what ips are pinging your server. It's especially helpful for looking for server list's ips.

max-connection-per-ip
=====================
	.. warning::
		Don't go lower than 1, it will cause your animatedmotd to stop working.
		
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 30-30
		
	This variable prevents abuse regarding bandwidth usage, connections exceeding this limit will be given see `fallback`_ motd.

formatting
==========
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 31-33
		
	Formatting is used for formatting countdowns and some bukkit sided variables.
	
	.. glossary::
		time-format
			Is used for countdowns where {0} are days, {1} hours, {2} minutes and {3} seconds
			
		date-format
			Is used for bukkit variables: first-played and last-played
			
----------
			
--------
database
--------
	Database is used for storing player data for DYNAMIC animations. Currently AnimatedMOTD supports sqlite, flatfile and mysql.
	
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 35-44
	
type
====
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 36-36
		
	There are three options available:
	
	- sqlite (default)
	- mysql
	- flatfile - May be the fastest
	- none - Completely disables database, if you are not using DYNAMIC animations it will speed up things for you.
		
	Plugin will automatically create tables for your database.
	
mysql
=====
	.. warning::
		Specyfing wrong connection details may cause lag or unexpected breakage.

	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 37-42
		
	If you want to use mysql you probably know how to set this up.
	
sqlite
======
	.. literalinclude:: __files/config.yml
		:language: yaml
		:lines: 43-44
	
	Sqlite is a reliable and fast flat-file database.
	
	.. glossary::
		file
			If for whatever reason you want to change file where player data is stored you can change it here.
			

