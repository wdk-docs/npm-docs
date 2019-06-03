npm-start
============================================================================================

Start a package

SYNOPSIS
-------------------

.. program:: npm

.. option:: start

npm start [-- <args>]

DESCRIPTION
-------------------

This runs an arbitrary command specified in the package’s "start" property of its "scripts" object. If no "start" property is specified on the "scripts" object, it will run node server.js.

As of npm@2.0.0, you can use custom arguments when executing scripts. Refer to npm-run-script for more details.

SEE ALSO
-------------------

- npm-run-script
- npm-scripts
- npm-test
- npm-restart
- npm-stop
