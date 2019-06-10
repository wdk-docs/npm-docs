npm restart
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: restart

   Restart a package

   .. code-block:: sh

      npm restart [-- <args>]

DESCRIPTION
-------------------

This restarts a package.

This runs a package’s “stop”, “restart”, and “start” scripts, and associated pre- and post- scripts, in the order given below:

prerestart
prestop
stop
poststop
restart
prestart
start
poststart
postrestart

NOTE
-------------------

Note that the “restart” script is run in addition to the “stop” and “start” scripts, not instead of them.

This is the behavior as of npm major version 2. A change in this behavior will be accompanied by an increase in major version number

SEE ALSO
-------------------

- :option:`npm run-script`
- :option:`npm scripts`
- :option:`npm test`
- :option:`npm start`
- :option:`npm stop`
- :option:`npm restart`
