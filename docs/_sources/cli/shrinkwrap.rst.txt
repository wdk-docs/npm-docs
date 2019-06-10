npm shrinkwrap
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

This command repurposes :ref:`package-lock.json` into a publishable :ref:`shrinkwrap.json` or simply creates a new one.

The file created and updated by this command will then take precedence over any other existing or future :ref:`package-lock.json` files.

For a detailed explanation of the design and purpose of package locks in npm, see :ref:`package-locks`.

SEE ALSO
-------------------

- :option:`npm install`
- :option:`npm run-script`
- :ref:`scripts`
- :ref:`package.json`
- :ref:`package-locks`
- :ref:`package-lock.json`
- :ref:`shrinkwrap.json`
- :option:`npm ls`
