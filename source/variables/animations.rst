==========
Animations
==========

Animations are simply shortcuts for creating multiple frames.

.. contents:: **Table of Contents**
   :depth: 2
   :local:
   
---------

----------
typewriter
----------
	Typewriter gives you nice writing effect.

	.. code-block:: html
	
		<typewriter pause="20" value="Text" delimiter=">>" frequency="3">
	
	.. glossary::
		pause
			Pause that occurs after type writing completes.
			
		value
			Text to typewrite.
			
		delimiter
			"Cursor" attached to the end of string while typewriting.
			
		frequency
			Blinking frequency of delimiter in intervals, giving real cursor feeling. 
			

	**Example:**
		//Image will be here

---------
		
--------
scroller
--------
	Scroller scrolls a text, imagine news bar when watching TV, it's exactly like that!
	
	.. code-block:: html
	
		<scroller value="text" spacing="10" width="30" direction="right">
	
	.. glossary::
		value
			Text to scroll.
		
		spacing
			Amount of spaces attached to the end of value.
		
		direction
			Direction to which text scrolls.
		
		width
			.. warning::
				Setting width too high may cause line glitches.
			
			Width of scroller in characters.
			
	**Example:**
		//Image will be here
		
---------
		
-----
for
-----
	For is basically loop or code executed x times. Our animation gives you access to index, so you can make countdowns for example.

	.. code-block:: html
		
		<for length="3" value="Counting $x">
		<for start="2" end="10" value="Counting $x">

	.. glossary::
		length
			.. warning::
				Specifying **length** precludes **start** and **end**.

			Specifying length causes animation to count from 0 to value length was set.
		
		start
		end
			.. warning::
				You have to specify both of these options in order to make it work correctly.
			
			Defines start and end index for animation.
			
	**Example:**
		//Image will be here
		