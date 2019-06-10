npm explore
============================================================================================

SYNOPSIS
-------------------

.. program:: npm

.. option:: explore

   Browse an installed package

   .. code-block:: sh

      npm explore <pkg> [ -- <command>]

DESCRIPTION
-------------------

Spawn a subshell in the directory of the installed package specified.

If a command is specified, then it is run in the subshell, which then immediately terminates.

This is particularly handy in the case of git submodules in the node_modules folder:

npm explore some-dependency -- git pull origin master
Note that the package is not automatically rebuilt afterwards, so be sure to use npm rebuild <pkg> if you make any changes.

CONFIGURATION
-------------------

shell
Default: SHELL environment variable, or “bash” on Posix, or “cmd” on Windows
Type: path
The shell to run for the npm explore command.

SEE ALSO
-------------------

- :ref:`folders`
- :option:`npm edit`
- :option:`npm rebuild`
- :option:`npm build`
- :option:`npm install`
