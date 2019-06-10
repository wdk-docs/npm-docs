npm build
============================================================================================

SYNOPSIS
-------------------

.. program:: npm

.. option:: build

   Build a package

   .. code-block::

      npm build [<package-folder>]

   <package-folder>: A folder containing a package.json file in its root.

DESCRIPTION
-------------------

This is the plumbing command called by npm link and npm install.

It should generally be called during installation, but if you need to run it directly, run:

.. code:: sh

   npm run-script build

SEE ALSO
-------------------

- :option:`npm install`
- :option:`npm link`
- :option:`npm scripts`
- :ref:`package.json`
