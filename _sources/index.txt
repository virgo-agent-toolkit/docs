Virgo Agent Toolkit Documentation
===============================================

A lightweight, open source, cross-platform agent toolkit written in C with an
embedded asynchronous LuaJit runtime.

Virgo works on most Linux distributions, Windows 2008+, and OSX.  We support the
following architectures as well: ARM, i686, and x86_64. If LuaJit supports a
system, then Virgo does as well. Theoretically, Virgo will run on MIPS and PPC ,
but we have not tested against these systems.

We aim to create a cross-platform agent that supports a low memory and CPU
footprint.  The Rackspace Monitoring Agent uses this framework and runs in about
6 MB of Resident Memory. On Windows, it runs in about 4.5 MB of memory.

.. toctree::
   :maxdepth: 3
   :glob:

   getting_started

Luvit
-----

.. toctree::
   :glob:
   :maxdepth: 1

   luvit_about
   luvit_modules

Developer Information
---------------------

.. toctree::
   :glob:
   :maxdepth: 1

   developer_resources

.. note::

    Unless noted otherwise, all of the examples and code snippets in the
    documentation are licensed under the `Apache 2.0 license`_.

.. _`Apache 2.0 license`: https://www.apache.org/licenses/LICENSE-2.0.html
