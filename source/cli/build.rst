npm-build
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

- npm-install
- npm-link
- npm-scripts
- package.json
