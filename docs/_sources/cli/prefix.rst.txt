npm prefix
============================================================================================

SYNOPSIS
-------------------

.. program:: npm

.. option:: prefix

   Display prefix

   .. code-block:: sh

      npm prefix [-g]

DESCRIPTION
-------------------

Print the local prefix to standard out. This is the closest parent directory to contain a package.json file or node_modules directory, unless -g is also specified.

If -g is specified, this will be the value of the global prefix. See npm-config for more detail.

SEE ALSO
-------------------

- :option:`npm root`
- :option:`npm bin`
- :ref:`folders`
- :option:`npm config`
- :option:`npm config`
- :ref:`npmrc`
