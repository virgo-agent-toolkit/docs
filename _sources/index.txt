Virgo Agent Toolkit Documentation
===============================================

A lightweight, open source, cross-platform agent written in C with an embedded
asynchronous LuaJit runtime.

Virgo works on most Linux distributions, Windows 2008+, and most other unicies.
We support the following architectures as well: ARM, i686, and x86_64. If LuaJit
supports a system, then Virgo does as well. Theoretically, Virgo will run on
MIPS and PPC as well, but we have not tested against these systems.

We aim to create a cross-platform agent that supports a low memory footprint.
The Rackspace Monitoring Agent uses this framework and runs in about 6 MB of
Resident Memory. On Windows, it runs in about 4.5 MB of memory.

.. toctree::
   :maxdepth: 3
   :glob:

   getting_started
