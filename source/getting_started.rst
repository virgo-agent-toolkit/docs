Getting Started
===============

Virgo is split into a core component and a derived project. This allows for
better code reuse. The core component is located in the
`virgo-agent-toolkit/virgo-base-agent`_ repository.

Overview
--------

Compiling Hello World Agent on Linux/OSX
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this derived project `example`_, we are going to start out with the most basic
agent: Hello World. Virgo expects to find an 'init.lua' file and a function
called 'run' exported from Lua.  Start by running the following commands.

.. sourcecode:: bash

    git clone git@github.com:virgo-agent-toolkit/virgo-example-agent.git
    cd virgo-example-agent
    git submodule update --init --recursive
    ./configure
    make

If everything has built correctly try running.

.. sourcecode:: bash

    out/Debut/virgo

init.lua
^^^^^^^^

Virgo and Luvit modules closely resemble Node.JS modules. Typically there is an
exports table that is returned from the module.

.. code-block:: lua

   local exports = {}

   -- Main entry
   exports.run = function()
     print('Hello World')
     process.exit(0)
   end

   return exports

.. note:: 
   Please remember that everything in Lua is defaulted to the global namespace. The
   Lua keyword `local` is needed for practically every variable or function
   declaration.

bundle.list
^^^^^^^^^^^

This file in the project adds files to a zip file embedded within the
executable. You start out with one file::

    ./init.lua

You can add more files to this list and use any subdirectory layout that you like.


.. _`virgo-agent-toolkit/virgo-base-agent`: https://github.com/virgo-agent-toolkit/virgo-base-agent
.. _`example`: https://github.com/virgo-agent-toolkit/virgo-example-agent
