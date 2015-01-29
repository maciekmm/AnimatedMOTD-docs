.. _blacklist:

=============
blacklist.yml
=============

blacklist.yml holds ip addresses that animation is disabled for, they will receive fallback motd specified in :doc:`main_config`
This is useful for some server listing sites that wait for proper protocol or pong packet.

It's really hard to keep track of all ip changes those sites make, if it's not working on your web-listing use :doc:`main_config` debug.

---------------------
Example blacklist.yml
---------------------
.. literalinclude:: __files/blacklist.yml
   :language: yaml