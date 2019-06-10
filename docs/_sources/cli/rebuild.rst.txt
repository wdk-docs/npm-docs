npm rebuild
============================================================================================

SYNOPSIS
-------------------

.. program:: npm

.. option:: rebuild

   Rebuild a package

   .. code-block:: sh

      npm rebuild [[<@scope>/<name>]...]

.. option:: rb

   rebuild alias

DESCRIPTION
-------------------

This command runs the npm build command on the matched folders. This is useful when you install a new version of node, and must recompile all your C++ addons with the new binary.

SEE ALSO
-------------------

- :option:`npm build`
- :option:`npm install`
