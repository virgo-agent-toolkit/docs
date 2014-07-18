Modules
=======

`luvit-async`_
--------------

Coalan McMahon's `async <https://github.com/caolan/async>` library.

.. code-block:: lua

    local stream = require('async')

    async.forEach({1,3,2}, function(x, callback)
      timer.setTimeout(x*25, function()
        table.insert(args, x)
        callback()
      end)
    end, function(err)
      asserts.array_equals(args, {1,2,3})
      test.done()
    end)

`luvit-stream`_
---------------

Stream interface in Luvit.

.. code-block:: lua

    local stream = require('stream')

    local Numbers = stream.Readable:extend()

    function Numbers:initialize(count, options)
      local opt = options or {}
      stream.Readable.initialize(self, opt)
      self.current = 1
      self.count = count
    end

    function Numbers:_read()
      if self.current > self.count then
        self:push(nil)
        return
      else
        self:push(tostring(self.current))
        self.current = self.current + 1
      end
    end

    Numbers:new(9):pipe(process.stdout)

`luvit-stream-fs`_
------------------

Filesystem Stream Library

`luvit-resolve`_
----------------

Pure luvit implementation of the luvit require() path logic

`luvit-tape`_
-------------

Test Suite for Luvit using stream2 interface

`luvit-bourbon`_
----------------

Older test framework based on Node.JS Whiskey.

`luvit-keystone`_
-----------------

Openstack Keystone Client for Luvit

.. _`luvit-stream`: https://github.com/virgo-agent-toolkit/luvit-stream
.. _`luvit-async`: https://github.com/virgo-agent-toolkit/luvit-async
.. _`luvit-resolve`: https://github.com/virgo-agent-toolkit/luvit-resolve
.. _`luvit-stream-fs`: https://github.com/virgo-agent-toolkit/luvit-stream-fs
.. _`luvit-template-stream`: https://github.com/virgo-agent-toolkit/luvit-template-stream
.. _`luvit-tape`: https://github.com/virgo-agent-toolkit/luvit-tape
.. _`luvit-bourbon`: https://github.com/virgo-agent-toolkit/luvit-bourbon
.. _`luvit-keystone`: https://github.com/virgo-agent-toolkit/luvit-keystone
