Virgo
=====

Virgo is split into a core component and a derived project. This allows for
better code reuse.

Compiling Virgo Hello World
---------------------------

In this example, we are going to start out with the most basic agent: Hello
World. Virgo expects to find an 'init.lua' file and a function called 'run'
exported from lua.  Start by running the following commands::

    git clone git@github.com:virgo-agent-toolkit/virgo-example-agent.git
    cd virgo-example-agent
    git submodule update --init --recursive
    ./configure
    make

If everything has built correctly try running::

    out/Debut/virgo

init.lua
--------

Virgo and Luvit modules closely resemble Node.JS modules. Typically there is an
exports table that is returned from the module::

    local exports = {}

    -- Main entry
    exports.run = function()
      print('Hello World')
      process.exit(0)
    end

    return exports

.. note:: 
   Please remember that everything in lua is defaulted to the global namespace. The
   Lua keyword `local` is needed for practically every variable or function
   instantiation.

bundle.list
-----------

This file in the project adds files to a zip file embedded within the
executable. You start out with one file::

    ./init.lua

You can add more files to this list and use any subdirectory layout that you like.

