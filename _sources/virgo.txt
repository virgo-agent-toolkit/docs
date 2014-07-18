Virgo
=====

Virgo is split into a core component and a derived project. This allows for
better code reuse.

Compiling Virgo Hello World
===========================

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

