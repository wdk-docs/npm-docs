npm pack
============================================================================================


SYNOPSIS
-------------------

.. program:: npm

.. option:: pack

   Create a tarball from a package

   .. code-block:: sh

      npm pack [[<@scope>/]<pkg>...] [--dry-run]

DESCRIPTION
-------------------

For anything that’s installable (that is, a package folder, tarball, tarball url, name@tag, name@version, name, or scoped name), this command will fetch it to the cache, and then copy the tarball to the current working directory as <name>-<version>.tgz, and then write the filenames out to stdout.

If the same package is specified multiple times, then the file will be overwritten the second time.

If no arguments are supplied, then npm packs the current package folder.

The --dry-run argument will do everything that pack usually does without actually packing anything. Reports on what would have gone into the tarball.

SEE ALSO
-------------------

- :option:`npm cache`
- :option:`npm publish`
- :option:`npm config`
- :option:`npm config`
- :ref:`npmrc`
