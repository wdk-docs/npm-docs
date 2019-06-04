npm-shrinkwrap
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: shrinkwrap

   Lock down dependency versions for publication

   .. code-block:: sh

      npm shrinkwrap

DESCRIPTION
-------------------

This command repurposes package-lock.json into a publishable npm-shrinkwrap.json or simply creates a new one. The file created and updated by this command will then take precedence over any other existing or future package-lock.json files. For a detailed explanation of the design and purpose of package locks in npm, see npm-package-locks.

SEE ALSO
-------------------

- :option:`npm install`
- :option:`npm run-script`
- :option:`npm scripts`
- :ref:`package.json`
- :option:`npm package-locks`
- :option:`package-lock.json`
- :option:`npm shrinkwrap.json`
- :option:`npm ls`
