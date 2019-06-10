npm bugs
============================================================================================

SYNOPSIS
-------------------

.. program:: npm

.. option:: bugs

   Bugs for a package in a web browser maybe

   .. code-block::

      npm bugs [<pkgname>]

.. option:: issues

   bugs aliases

DESCRIPTION
-------------------

This command tries to guess at the likely location of a package’s bug tracker URL, and then tries to open it using the ``--browser`` config param. If no package name is provided, it will search for a :doc:`../files/package.json` in the current folder and use the **name** property.

CONFIGURATION
-------------------

browser
-------------------

- Default: OS X: **"open"**, Windows: **"start"**, Others: **"xdg-open"**
- Type: String

The browser that is called by the :option:`npm bugs` command to open websites.

registry
-------------------

- Default: https://registry.npmjs.org/
- Type: url

The base URL of the npm package registry.

SEE ALSO
-------------------

- :option:`npm docs`
- :option:`npm view`
- :option:`npm publish`
- :ref:`registry`
- :option:`npm config`
- :option:`npm config`
- :doc:`../files/npmrc`
- :doc:`../files/package.json`
