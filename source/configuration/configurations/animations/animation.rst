.. _animation:
================
animations/*.yml
================

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
	
	
	