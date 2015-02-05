.. _animation:

=================
animations/\*.yml
=================

You can create as many animation configurations as you like, resulting in possibility to hot-swap them or create animation per forced host.

.. contents:: **Table of Contents**
   :depth: 2
   :local:
   
----------

------------
Example file
------------

.. literalinclude:: ../__files/animations/generic_static.yml
   :language: yaml

----------

type
====
	.. literalinclude:: ../__files/animations/generic_static.yml
	   :language: yaml
	   :lines: 1-1
	
	There are two types of animation:
	
	- STATIC - Does not support player-based variables, is mostly used for players for which player data has not been collected yet. You can use STATIC animation in dynamic as stated in :doc:`../main_config`
	- DYNAMIC- Does support player-based variables, but is limited to players that have already been on server (counting from plugin installation). You cannot use DYNAMIC in static field as stated in :doc:`../main_config`
	
settings
========
	.. literalinclude:: ../__files/animations/generic_static.yml
		:language: yaml
		:lines: 2-5
	
	.. glossary::
		interval
			.. warning::
				Lowering interval might cause performance issues
				
			Interval is represented in milliseconds (1 second = 1000 milliseconds), value 100 means that motd will be updated 10 times a second.
			
		delay
			Delay after animation will start.
		
		duration
			Amount of intervals after which animation stops.

favicon
=======
	.. literalinclude:: ../__files/animations/generic_static.yml
		:language: yaml
		:lines: 6-9
	
	.. glossary::
		animation
			Favicon files used in animation. Using .gif will result in animated icon, .png will result in static one. Files have to be placed in main plugin folder.
		
		style
			There are two styles **normal** and **optimized**, you have to choose one that corresponds to process how your .gif was built. If your icon does not animate properly switch to other mode.
			
		intervals-per-frame
			Defines how fast gif will update, as we can't rely on .gif frames properties you have to specify fixed framerate here, setting it to 1 with interval in `settings`_ set to 100 results in 10fps.

section
=======
	.. literalinclude:: ../__files/animations/generic_static.yml
		:language: yaml
		:lines: 23-26
	
	Every animation part has a section where you can specify how animation looks like.
	
	.. glossary::
		intervals-per-frame
			Defines how fast text line will update, setting it to 2 will result in update every second interval.
		
		text
			Defines what text will show, you can use placeholders, animation tags and own text here, you are only limited by your imagination.
		
		enabled
			.. note::
				Enabled option does not work in motd lines.
			
			Specify whether or not change default value at all.
	
motd
====
	.. literalinclude:: ../__files/animations/generic_static.yml
		:language: yaml
		:lines: 10-21
	
	Motd divides in two similar sections **first** and **second** corresponding to lines. See `section`_.

status-bar
==========
	.. literalinclude:: ../__files/animations/generic_static.yml
		:language: yaml
		:lines: 22-26
		
	Status bar is the place where normally player count is shown, you can put whatever you want there! See `section`_.

player-data:
============
	.. literalinclude:: ../__files/animations/generic_static.yml
		:language: yaml
		:lines: 27-48
	
	Player data divides into sections enumerated by line number, See `section`_.
		
	
	