.. _commands:

========
Commands
========

There's not many commands at the moment, we plan on introducing commands changing motd on the fly, but making them user-friendly with current setup is challenging. 
We only provide admin commands, all of them can be used from console.

.. contents:: **Commands**
   :depth: 2
   :local:

-------------
   
--------------------
/animatedmotd reload
--------------------
	**Permission:** animatedmotd.reload
	
	Reload command is used for reloading:
	
	- :doc:`configuration/configurations/animations/animation`
	- :doc:`configuration/configurations/blacklist`
	- :doc:`configuration/configurations/main_config`
	
	**Output:**
		[AnimatedMOTD] Config reloaded

-------------

-------------------
/animatedmotd debug
-------------------
	**Permission:** animatedmotd.debug
	
	The command is used for debugging, it's **required** to use this command and provide it's outcome in order to ask for help.
	It scans your logs and looks for exceptions, it also includes your current plugin version as well as configuration.
	
	**Example output:**
		http://paste.ubuntu.com/9956527/

-------------
		
--------------------------
/animatedmotd troubleshoot
--------------------------
	.. warning::
		This command is experimental
		
	**Permission:** animatedmotd.troubleshoot
	
	This command helps you troubleshoot your errors based on frequent mistakes people make when configuring our plugin.