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

.. _`luvit-stream`: https://github.com/virgo-agent-toolkit/luvit-stream
.. _`luvit-async`: https://github.com/virgo-agent-toolkit/luvit-async
